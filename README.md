# How to run
Simply type:
```
docker compose up -d
```
The setup requires a running Traefik reverse proxy on your system.
In case you don't use it, then uncomment lines with 8080 and 8081 ports mapping -> your leshan server will be exposed directly instead of via reverse proxy providing HTTPS.

# Important
- Every time you re-build the images, the latest build of leshan is fetched from https://ci.eclipse.org/leshan/job/leshan-ci/job/master/lastSuccessfulBuild/artifact/leshan-server-demo.jar
- Check https://github.com/eclipse-leshan/ for more info.
