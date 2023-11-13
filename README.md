# Build and deploy Quarkus JVM

## Run build without run test

``` shell script
quarkus build --no-tests
```
## Run SAM deploy

``` shell script
sam deploy -g -t .\sam.jvm.yaml
```

# Build and deploy Quarkus Native
## Fix the issue fork/exec /var/task/bootstrap: exce format error Runtime.InvalidEntryPoint

``` shell script
mvn package -Pnative --define quarkus.native.container-build=true
```
Note: You need to run the linux docker before run this command

## Deploy with specific path

You can run this command in terminal:
```shell script
sam deploy -g -t .\sam.native.yaml
```
