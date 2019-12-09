# Example

```java
import org.liashchynskyi.gan.Generator;
import org.liashchynskyi.gan.GeneratorBuilder;

...

    public static String[] labels = new String[]{"label1", "label2", "label3", "label4", "label5"}; //for subdirectories in the output folder
    public static final String MODEL_PATH = "path/to/model/dir/model";
    
    Generator generator = new GeneratorBuilder().labels(labels).modelPath(MODEL_PATH).num(5).build();
    generator.loadAndPredict("output/folder");
        
...
```

> There are 5 classes of histological images.

This code **always** generates images for all classes. Summary, in the example above we get 5 images, one image per class.

## Download JAR (no sources)

See [releases](https://github.com/liashchynskyi/fake-hist/releases).
