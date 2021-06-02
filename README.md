# Basic Pipeline (Tekton) for Spring Boot with Maven and Buildah

To try this out for yourself, simply:

1. Clone this repository and change into the root directory.

2. Create a new project:

```
oc new-project springboot
```

3. Create the Pipeline and the ImageStream

```
oc apply -f build
```

4. Create the application resources

```
oc apply -f app
```

5. Run the pipeline.

```
oc create -f run/run-build.yaml -n springboot
```


When the pipeline completes, it should rollout the new image and your app should be ready!
