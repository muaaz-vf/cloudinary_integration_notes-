# Cloudinary Integration -
### Introduction 

Purpose of this document is to enable the reader to quickly integrate cloudinary in his/her project. Our main focus will be on the essential features of cloudinary api. Essential features are listed below,
  
  * Fetching cloud resource and getting the corresponding image. 
  * Retaining information for future use. 
  * Upload asset to cloudinary cloud. 

Before we dig into technical details lets check out difference between alternative services out there.

### Alternative Services 

Below is a very brief difference between different services out there. 

#### [Cloudinary](http://cloudinary.com/)

  * It’s the most useful service out there with many feature and easy integration. Impressive free tier.
  * Images are delivered via CDN which can speed up thing on the client end.
  * GUI interface to manipulate your assets and manage them outside the system.
  * Documentation is excellent and fluent.
  * It uses internal storage rather than s3 kind of service. Which means it will be very hard to moving on if we use this service.
  * When you create temporary images, they stick around and do not go away automatically.
  * Suitable for low to mid level business which requires less expensive solutions.

#### [Imgix](https://www.imgix.com/)
  * Nice interface and easy to manage images.
  * Super fast image processing and CDN is up-to mark.
  * Flat rate pay as you use the service.
  * Only 10$ credit no free tier available.
  * Multiple platform easy integration and support libraries available.
  * Recommended by [rubyweekly.com](http://rubyweekly.com/).
  * Suitable for business where traffic rate can be judged and cost can be calculated.

#### [Filestack](https://www.filestack.com/)
* Images are delivered via CDN which can speed up thing on the client end.
* GUI interface to manipulate your assets and manage them outside the system.
* Various integrations to different platform available for example github,facebook and google drive etc,.  
* Little bit expensive than cloudinary. 
* Limited integrations with programming platforms. 

#### [Blitline](https://www.blitline.com/v3/home)
* It only gives you processing ability rather than a whole solution.
* You will need connect S3 for using in accordance to use this service.
* No official gem as Cloudinary gives support to multiple platforms.
* Less expensive but free tier is not useful to start the service.
* Most effective you are dealing very large images processing system.
 
Some more similar services [Filespin](https://filespin.io/) and [Kloudless](https://kloudless.com/).

### Fetch Resource

Fetching a resource from cloudinary is very simple and easy. Cloudinary store every file in there cloud with a unique id which is called public_id in there api documentation, on which you can get the image resource. Below is a simple example using in angular, ruby on rails and node cloudinary libraries.

#### Angular

Below are the steps to setup cloudinary into your angular application. 
* First acquire cloudinary via bower `bower install cloudinary_ng --save` and include the module in manifest file. Below are the files you will need to include, 
  ..* lodash/lodash.min
  ..* cloudinary-core/cloudinary-core.min 
  ..* cloudinary_ng/js/angular.cloudinary
* Include the module into your app `angular.module('appName',[cloudinary])`
* In your config block add this `cloudinaryProvider.set("cloud_name", cloud_name) ` , if you are using multi environments best to use with config.json.
* Now you can simply use the built in directive provided by the lib `<cl-image public-id="{some_public_id}" class="thumbnail inline" angle="20" format="jpg">
<cl-transformation height="150" width="150" crop="fill" gravity="north" effect="sepia" radius="20"/></cl-image>`
