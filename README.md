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

4. Run the pipeline.


```
oc create -f run/run-build.yaml
```

5. Once the Pipeline finishes running, deploy the app:


```
oc apply -f app
```
