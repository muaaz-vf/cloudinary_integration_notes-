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
