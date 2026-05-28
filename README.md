# Ex.08 Design of Interactive Image Gallery
# Date:17.05.2025
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
<h2 align="center">PORSCHE</h2>
<!DOCTYPE html>


<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
 
  <title>Image Gallery</title>
  

</head>
<style>
 
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  padding: 20px;
}

.image-container {
  position: relative;
  overflow: hidden;
  width: 500px;
  height: 400px;
}

.gallery-item {
  width: 100%;
  height: auto;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.1);
}


.modal {
  display: none; 
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.9);
  overflow: auto;
}

.modal-content {
  display: block;
  margin: auto;
  max-width: 80%;
  max-height: 80%;
}

.close {
  color: #fff;
  font-size: 40px;
  font-weight: bold;
  position: absolute;
  top: 10px;
  right: 25px;
  transition: 0.3s;
  cursor: pointer;
}

.close:hover,
.close:focus {
  color: #ddd;
  text-decoration: none;
  cursor: pointer;
}

#caption {
  text-align: center;
  color: #fff;
  font-size: 20px;
  padding: 10px;
}

</style>
<body>

  <div class="gallery">
    <div class="image-container">
      <img src="911.jpg"  alt="PORSCHE 911" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="718-Boxter-GTS.avif"  alt="718-BOXTER-GTS" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="arunoda.avif"  alt="ARNAUD MORO" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="porsche_photographers_update_new_niklas_koppitsch.avif" alt="NIKLAS KOPPITSCH" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="porsche_photographers_update_new_paul_mckenzie.avif"  alt="PAUL MCKENZIE" class="gallery-item">
    </div>
    <div class="image-container">
      <img src="porsche-20photographers-20to-20inspire-20you-202.avif"  alt="AMY SHORE" class="gallery-item">
    </div>
  
  <div id="myModal" class="modal">
    <span class="close">&times;</span>
    <img class="modal-content" id="img01">
    <div id="caption"></div>
  </div>

  <script>
  
const modal = document.getElementById("myModal");
const modalImg = document.getElementById("img01");
const captionText = document.getElementById("caption");
const closeBtn = document.getElementsByClassName("close")[0];


const images = document.querySelectorAll(".gallery-item");


images.forEach(img => {
  img.onclick = function() {
    modal.style.display = "block";
    modalImg.src = this.src;
    captionText.innerHTML = this.alt;
  };
});


closeBtn.onclick = function() {
  modal.style.display = "none";
};


window.onclick = function(event) {
  if (event.target === modal) {
    modal.style.display = "none";
  }
};

  </script>
  <footer>
    <h2 align="center">Designed and developed by V.Shiryha - 212224230267</h2>
  </footer>
</body>
</html>
```
# OUTPUT:
<img width="1046" height="586" alt="{EF10C1D2-CDBF-4FD5-943C-4428110D18B3}" src="https://github.com/user-attachments/assets/1a213930-ffe2-432d-9173-adb564d554e7" />

<img width="1046" height="553" alt="{85AD5172-A97C-4CBB-9914-F0C628EB2E2F}" src="https://github.com/user-attachments/assets/7cb92872-c5ec-42d7-bb78-6c49a20744b5" />

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
