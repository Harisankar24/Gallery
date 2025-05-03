# Ex.08 Design of Interactive Image Gallery
# Date:03-05-2025
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
index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Photo Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Interactive Photo Gallery</h1>
    <div class="gallery">
        <img src="https://img.freepik.com/premium-photo/beautiful-sunset-with-rocks-along-beach_103127-640.jpg?w=826" alt="Image 1" onclick="openModal(this)">
        <img src="https://img.freepik.com/free-photo/asian-woman-wearing-thai-dress-costume-traditional-according-thai-culture-pha-dok-siew-waterfall-chiang-mai-thailand_335224-1164.jpg?t=st=1746165656~exp=1746169256~hmac=75797beb62249d8794236bdf046b76a4836d33d18630e248d6e2027e0b2f5161&w=826 " alt="Image 2" onclick="openModal(this)">
        <img src="https://img.freepik.com/free-photo/water-fall_335224-985.jpg?t=st=1746165812~exp=1746169412~hmac=754d7cf17fe66ece44e4c9f9265aa1465453b00bec5d94303d1eca2d47d7570d&w=826" alt="Image 3" onclick="openModal(this)">
        <img  src="https://img.freepik.com/free-photo/water-landscape-scenery-natural-blue-ancient_1417-1224.jpg?t=st=1746173854~exp=1746177454~hmac=18c01faf7c4bdfc47ef952b2685e5773b0cc15a0978263906c81ae5dd83e4248&w=1380" alt="Image 4" onclick="openModal(this)">
        <img src="https://img.freepik.com/free-photo/closeup-shot-beautiful-butterfly-orange-petaled-flower_181624-13884.jpg?t=st=1746165996~exp=1746169596~hmac=4bc77808c40fb5610c9e0554ed217f859689838463aa68747751f97e574d2fc7&w=826" alt="Image 5" onclick="openModal(this)">
    </div>

    <div class="modal" id="imageModal">
        <span onclick="closeModal()">&times;</span>
        <img id="modalImage" src="" alt="">
    </div>
    <script src="script.js"></script>
</body>
</html>



```
style.css
```
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
    background-color: #f4f4f4;
    
    background-size:cover;
    
}

h1 {
    margin-top: 20px;
    margin-top:50px;
    font-family:"caveat";
    font-size:70px;
    color:black;
}

.gallery {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
    padding: 20px;
    margin-top:110px;
}

.gallery img {
    width: 200px;
    height: 150px;
    border: 2px solid #ccc;
    border-radius: 8px;
    cursor: pointer;
    transition: transform 0.3s, box-shadow 0.3s;
}

.gallery img:hover {
    transform: scale(1.1);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
    z-index: 1000;
}

.modal img {
    max-width: 90%;
    max-height: 90%;
    border: 4px solid white;
    border-radius: 10px;
}

.modal span {
    position: absolute;
    top: 20px;
    right: 40px;
    font-size: 30px;
    color: white;
    cursor: pointer;
    font-weight: bold;
}
```
scripts.js
```
function openModal(image) {
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImage');
    modal.style.display = 'flex';
    modalImg.src = image.src;
}

// Function to close the modal
function closeModal() {
    const modal = document.getElementById('imageModal');
    modal.style.display = 'none';

}    

```
# OUTPUT:
![alt text](<Screenshot 2025-05-03 112941.png>)
![alt text](<Screenshot 2025-05-03 112955.png>)
![alt text](<Screenshot 2025-05-03 113111.png>)
![alt text](<Screenshot 2025-05-03 113123.png>)
![alt text](<Screenshot 2025-05-03 113146.png>)
![alt text](<Screenshot 2025-05-03 113155.png>)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
