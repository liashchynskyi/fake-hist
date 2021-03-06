
# GAN-based generator for histological images
<center><img src="https://i.ibb.co/sW0SY2Y/Picture-1.png" alt="Picture-1" border="0"></center>

# Example

```java
import org.liashchynskyi.gan.Generator;
import org.liashchynskyi.gan.GeneratorBuilder;

...
    //for subdirectories in the output folder
    public static String[] labels = new String[]{
        "hist_proliferative_mast", 
        "histo_fibroadenoma", 
        "histo_fibrozno_kistozna_mastopatia", 
        "histo_lystovydna_fibroadenoma", 
        "histo_neproliferatyvna_mastopatia"
    };
    public static final String MODEL_PATH = "path/to/model/dir";
    
    Generator generator = new GeneratorBuilder()
                                .labels(labels)
                                .modelPath(MODEL_PATH)
                                .num(5) // examples to generate
                                .build();
    generator.loadAndPredict("output/folder");
        
...
```

> There are 5 classes of histological images.
**Note:** set number of generated images to multiple of number of classes.

This code **always** generates images for all classes. In the example above we get 5 images in summary, one image per class.

## Download JAR (no sources)

Latest release is [1.0-beta](https://github.com/liashchynskyi/fake-hist/releases/tag/1.0-beta). See [releases](https://github.com/liashchynskyi/fake-hist/releases) for more info. 

* Download JAR
* Download `model.tar`
* Unpack `tar`
* Add `jar` executable to Java `classpath`

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
