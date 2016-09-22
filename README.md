
# Cloudinary React Library

Cloudinary is a cloud service that offers a solution to a web application's entire image management pipeline.

Easily upload images to the cloud. Automatically perform smart image resizing, cropping and conversion without installing any complex software. Integrate Facebook or Twitter profile image extraction in a snap, in any dimension and style to match your website’s graphics requirements. Images are seamlessly delivered through a fast CDN, and much much more.

Cloudinary offers comprehensive APIs and administration capabilities and is easy to integrate with any web application, existing or new.

Cloudinary provides URL and HTTP based APIs that can be easily integrated with any Web development framework.

## Getting started guide

![](http://res.cloudinary.com/cloudinary/image/upload/see_more_bullet.png)  **Take a look at our [Getting started guide for jQuery](http://cloudinary.com/documentation/jquery_integration#getting_started_guide)**.

## Installation


### NPM

1. Install the files using the following command. Use the optional `--save` parameter if you wish to save the dependency in your `bower.json` file.

   ```shell
   npm install cloudinary-react --save
   ```

1. Include the javascript files in your code. For Example:

   import {Image} from 'cloudinary-react';


## Setup

In order to properly use this library you have to provide it with a few configuration parameters. All configuration parameters can be applied directly to the element or usign a CloudinaryContext element.


```
ReactDOM.render(
            <div>
                <h1>Hello, world!</h1>
                <Image cloudName="demo" publicId="sample" width="300" crop="scale"/>
                 { /* or using the namespace cloudinaryReact */ }
                <cloudinaryReact.CloudinaryContext cloudName="demo">
                    <cloudinaryReact.Image publicId="sample">
                        <cloudinaryReact.Transformation width="200" crop="scale" angle="10"/>
                    </cloudinaryReact.Image>
                </cloudinaryReact.CloudinaryContext>
            </div>,
            document.getElementById('example')
    );
```

Required:

* `cloudName` - The cloudinary cloud name associated with your Cloudinary account.

Optional:

* `privateCdn`, `secureDistribution`, `cname`, `cdnSubdomain` - Please refer to [Cloudinary Documentation](http://cloudinary.com/documentation/rails_additional_topics#configuration_options) for information on these parameters.


## Usage

The library includes 4 Elements:

* CloudinaryContext
* Image
* Video
* Transformation

### CloudinaryContext
CloudinaryContext allows you to define shared parameters that are applied to all children elements.

### Image
The Image element defines a Cloudinary Image tag.
 
### Video
The Image element defines a Cloudinary Image tag.

### Transformation
The Transformation element allows you to defined additional transformations on the parent element.

For example:

```
<Image cloudName="demo" publicId="sample">
    <Transformation angle="-45"/>
    <Transformation effect="trim" angle="45" crop="scale" width="600">
      <Transformation overlay="text:Arial_100:Hello" />
    </Transformation>
</Image>
```


The Cloudinary Documentation can be found at:
http://cloudinary.com/documentation

## Additional resources

Additional resources are available at:

* [Website](http://cloudinary.com)
* [Documentation](http://cloudinary.com/documentation)
* [Knowledge Base](http://support.cloudinary.com/forums)
* [Documentation for jQuery integration](http://cloudinary.com/documentation/jquery_integration)
* [jQuery image upload documentation](http://cloudinary.com/documentation/jquery_image_upload)
* [jQuery image manipulation documentation](http://cloudinary.com/documentation/jquery_image_manipulation)
* [Image transformations documentation](http://cloudinary.com/documentation/image_transformations)

## Support

You can [open an issue through GitHub](https://github.com/cloudinary/cloudinary_js/issues).

Contact us at [http://cloudinary.com/contact](http://cloudinary.com/contact).

Stay tuned for updates, tips and tutorials: [Blog](http://cloudinary.com/blog), [Twitter](https://twitter.com/cloudinary), [Facebook](http://www.facebook.com/Cloudinary).


## License

Released under the MIT license.

The direct image upload feature of the plugin is based on https://github.com/blueimp/jQuery-File-Upload