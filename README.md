# What's it?
A Freemarker adapter for simpler framework's templating rendering.
# how to install
It's not on the repo engines, so just clone it in your project PARENT folder.
In your project's settings.graddle add:
```groovy
include ':simpler-freemarker-adapter'  
project(':simpler-freemarker-adapter').projectDir = new File(settingsDir, "../simpler-freemarker-adapter")
```
In build.graddle:
```groovy
compile project(':simpler-freemarker-adapter')
```
# How to use with simpler
When building `SimplerDependenciesProvider`:

```kotlin
SimplerDependencyManager.provider = SimplerDependenciesProvider(
            //servletRequestParametersWrapper =  ServletRequestParametersWrapper(
            //    jsonParametersParser = JacksonParametersParser(ObjectMapper())
            //),
            //assetsPathProvider = AssetsPathProvider(publicFolderConfig),
            templateProcessor = FreemarkerTemplateProcessor(configuration) //pass here/ configuration is the configuration object that your suposed to build on your own
        )
```

That's it. It does nothing on it's own