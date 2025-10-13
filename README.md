# Ex.08 Design of Interactive Image Gallery
# Date:06-10-25
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Interactive Image Gallery</title>
<link rel="stylesheet " href="gal.css">
</head>
<body>

<h1>Interactive Image Gallery</h1>
<div class="gallery">
  <img src="generated-image (3).png"  onclick="openLightbox(this)">
  <img src="generated-image (4).png"  onclick="openLightbox(this)">
  <img src="generated-image (5).png"  onclick="openLightbox(this)">
  <img src="generated-image (6).png"  onclick="openLightbox(this)">
  <img src="generated-image (7).png"  onclick="openLightbox(this)">
  <img src="hacker-with-laptop.jpg"  onclick="openLightbox(this)">
  <img src="istockphoto-537331500-1024x1024.jpg"  onclick="openLightbox(this)">
<img src="pexels-designecologist-1779487.jpg"  onclick="openLightbox(this)">
</div>

<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="close-btn" onclick="closeLightbox()">&times;</span>
  <img id="lightbox-img" src="" alt="Expanded Image" />
</div>

<script>
  function openLightbox(element) {
    const lightbox = document.getElementById('lightbox');
    const lightboxImg = document.getElementById('lightbox-img');
    lightbox.style.display = 'flex';
    lightboxImg.src = element.src;
    lightboxImg.alt = element.alt;
    event.stopPropagation();
  }
  function closeLightbox() {
    const lightbox = document.getElementById('lightbox');
    lightbox.style.display = 'none';
  }
</script>

</body>
</html>


body {
    font-family: Arial, sans-serif;
    background-color: #f7f9fb; 
    margin: 0;
    padding: 20px;
    color: #333;
  }
  h1 {
    text-align: center;
    color: #005f73; 
  }
  .gallery {
    display: grid;
    grid-template-columns: repeat(4,250px);
    gap: 50px;
    max-width: 960px;
    margin: 20px auto;
  }
  .gallery img {
    width: 100%;
    height:300px;
    object-fit: cover;
    border-radius: 8px;
    cursor: pointer;
    box-shadow: 0 2px 6px rgba(0,0,0,0.15);
    transition: transform 0.3s ease;
  }
  .gallery img:hover {
    transform: scale(1.05);
    box-shadow: 0 6px 15px rgba(0,95,115,0.5);
  }

  .lightbox {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,95,115,0.9); 
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }
  .lightbox img {
    max-width: 90%;
    max-height: 80%;
    border-radius: 10px;
    box-shadow: 0 4px 20px rgba(0,0,0,0.7);
  }
  .lightbox:target {
    display: flex;
  }
  
  .close-btn {
    position: fixed;
    top: 20px;
    right: 30px;
    font-size: 30px;
    color: #fff;
    cursor: pointer;
    z-index: 1100;
  }
  .close-btn:hover {
    color: #ffd166;
  }

</body>
</html>
```
# OUTPUT:
![alt text](<WhatsApp Image 2025-10-13 at 11.24.49 (1).jpeg>)
![alt text](<WhatsApp Image 2025-10-13 at 11.24.49 (1).jpeg>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
