# Ex.08 Design of Interactive Image Gallery
# Date:05.05.2025
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

    <meta charset="UTF-8">
    <title>Interactive Image Gallery</title>
    <style>
        
        body {
            font-family:  "Bokor", serif;;
            text-align: center;
            background-color: rgb(255, 0, 0);
            font-size: 60px;
            background: linear-gradient(red,black);
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
        }

        .photo {
            margin-top: 10%;
            margin-left: 2%;
            width: 240px;
            height: 440px;
            overflow: hidden;
            border-radius: 10px;
            border-width: 2px;
            border-color: solid black;
        }

        .photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .photo img:hover {
            transform: scale(1.1);
        }

        .lightbox {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            align-items: center;
            justify-content: center;
        }

        .lightbox-content {
            max-width: 90%;
            max-height: 80%;
        }

        .close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 30px;
            font-weight: bold;
            color: white;
            cursor: pointer;
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const lightbox = document.getElementById('lightbox');
            const lightboxImg = document.getElementById('lightbox-img');
            const photos = document.querySelectorAll('.photo img');
            const close = document.querySelector('.close');

            photos.forEach(photo => {
                photo.addEventListener('click', function() {
                    lightbox.style.display = 'flex';
                    lightboxImg.src = photo.src;
                });
            });

            close.addEventListener('click', function() {
                lightbox.style.display = 'none';
            });

            lightbox.addEventListener('click', function(event) {
                if (event.target !== lightboxImg) {
                    lightbox.style.display = 'none';
                }
            });
        });
    </script>
</head>
<body>
    <h1 style="font-size: 80px;">FORMULA 1</h1>
    <div class="gallery">
        <div class="photo">
            <img src="ferrari.avif" alt="Apache">
        </div>
        <div class="photo">
            <img src="mercedes.jpg" alt="BMW">
        </div>
        <div class="photo">
            <img src="mclaren.avif" alt="Pulsar">
        </div>
        <div class="photo">
            <img src="redbull.jpg" alt="Royal enfeild">
        </div>
        <div class="photo">
            <img src="astonmartin.jpeg" alt="Yamaha z9x">
        </div>
        <div class="photo">
            <img src="alpine.avif" alt="Yamaha z9x">
        </div>
    </div>
    <div id="lightbox" class="lightbox">
        <span class="close">&times;</span>
        <img class="lightbox-content" id="lightbox-img">
    </div>
</body>
</html>
```
# OUTPUT:
![alt text](<tarun/galleryapp/Screenshot 2025-05-05 081551.png>)
![alt text](<tarun/galleryapp/Screenshot 2025-05-05 081602.png>)
![alt text](<tarun/galleryapp/Screenshot 2025-05-05 081611.png>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
