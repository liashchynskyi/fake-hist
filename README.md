# Example

```java
import org.liashchynskyi.gan.Generator;
import org.liashchynskyi.gan.GeneratorBuilder;

...

    public static String[] labels = new String[]{"label1", "label2", "label3", "label4", "label5"}; //for subdirectories in the output folder
    public static final String MODEL_PATH = "path/to/model/dir";
    
    Generator generator = new GeneratorBuilder().labels(labels).modelPath(MODEL_PATH).num(5).build();
    generator.loadAndPredict("output/folder");
        
...
```

> There are 5 classes of histological images.
**Note:** set number of generated images to multiple of number of classes.

This code **always** generates images for all classes. Summary, in the example above we get 5 images, one image per class.

## Download JAR (no sources)

Latest release is [1.0-beta](https://github.com/liashchynskyi/fake-hist/releases/tag/1.0-beta). See [releases](https://github.com/liashchynskyi/fake-hist/releases) for more info. 

* Download JAR
* Download `model.tar`
* Unpack `tar`
* See the example above


## Citation
```
@misc{liashchynskyi2019,
  author = {Liashchynskyi, Petro},
  title = {fake-hist},
  year = {2019},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/liashchynskyi/fake-hist}},
}
````
