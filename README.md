# E-Commerce Image Management with Filestack

This repository demonstrates how to enhance e-commerce image management by integrating **Filestack's Image Upload, Optimization, and Transformation APIs**. The example code provides a simple yet powerful interface to upload, optimize, and enhance product images with features like smart cropping, auto-enhancement, and delivery via a global CDN.

---

## Features

- **Image Upload**: Upload product images securely using Filestack's SDK.
- **Image Optimization**: Automatically optimize images for fast loading and better user experience.
- **Smart Cropping**: Dynamically crop images to specific dimensions.
- **Auto-Enhancement**: Apply Filestack's auto-enhancement preset for high-quality images.
- **Global CDN Delivery**: Deliver optimized images via a Content Delivery Network for faster access.

---

## Getting Started

### Prerequisites

- A [Filestack](https://www.filestack.com/) API key. Sign up for free to obtain your API key.

### Installation

1. Clone this repository:
  
   - git clone https://github.com/shamalja/ecommerce-image-management-filestack.git
   - cd ecommerce-image-management-filestack
   - Open the FilestackEnhanceECommerceImageManagement.html file in a browser using a server. You can use a local server as well—just ensure your server is whitelisted in the Filestack dashboard under the security section.


- Replace YOUR_API_KEY in the script with your actual Filestack API key.

## Usage

Click Choose Image to upload a product image.

The uploaded image will be optimized with the following transformations:
- Smart Cropping: Resizes to 400x400 pixels (size can be changed as per the requirement).
- Auto-Enhancement: Enhances image quality.
- Cache Control: Caches the image for 3600 seconds (you can change this as per the requirement).

The optimized image will display on the screen with details.

## Code Highlights

### Key Transformations

**javascript** 

`const optimizedImageUrl = `https://cdn.filestackcontent.com/smart_crop=width:400,height:400/enhance=preset:auto/cache=expiry:3600/${fileHandle}`;

- Smart Cropping: Dynamically adjusts dimensions for product images.
- Auto-Enhancement: Improves image quality.
- Cache Control: Ensures efficient image delivery.

### Integration with Filestack SDK
The Filestack JavaScript SDK is used to handle image uploads:

**javascript**

```javascript
const client = filestack.init('YOUR_API_KEY');  
client.upload(file).then(response => {
  // Handle optimized image delivery
});```  


## Live Demo

You can view the example live by opening the FilestackEnhanceECommerceImageManagement.html file in your browser after replacing the API key.

## License

This project is licensed under the MIT License.

## Resources

Filestack Documentation (https://www.filestack.com/docs/)

Happy coding! 🚀  


