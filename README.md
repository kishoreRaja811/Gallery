# Ex.08 Design of Interactive Image Gallery
# Date:12.12.2024
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
``` python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>image gallery</title>
</head>
<style>

    body {
    margin: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 100vh;
    background :#211313;
    overflow: hidden;
  }
  .image-container {
    position: relative;
    width: 200px;
    height: 200px;
    transform-style: preserve-3d;
    transform: perspective(1000px) rotateY(0deg);
    transition: transform 0.9s;
  }
  .image-container span {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    transform: rotateY(calc(var(--i) * 45deg)) translateZ(400px);
  }
  .image-container span img {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
  }
  .btn-container {
    position: relative;
    width: 80%;
  }
  .btn {
    position: absolute;
    bottom: -200px;
    background: crimson;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
  }
  #prev {
    left: 20%;
  }
  #next {
    right: 20%;
  }
  .btn:hover {
    filter:contrast(1);
  }

</style>

<body>

    <div class="image-container">

        <span style="--i:1">
            <img src="bike1.jpg" width="260" height="250">
        </span>

        <span style="--i:2">
            <img src="bike2.jpg" width="260" height="250">
        </span>

        <span style="--i:3">
            <img src="bike3.jpg" width="260" height="250">
        </span>

        <span style="--i:4">
            <img src="bike4.jpg" width="260" height="250">
        </span>

        <span style="--i:5">
            <img src="bike5.jpg" width="260" height="250">
        </span>

        <span style="--i:6">
            <img src="bike6.jpg" width="260" height="250">
        </span>

        <span style="--i:7">
            <img src="bike7.jpg" width="260" height="250">
        </span>

        <span style="--i:8">
            <img src="bike8.jpg" width="260" height="250">
        </span>

    </div>

    <div class="btn-container">
        <button class="btn" id="prev">PREVIOUS</button>
        <button class="btn" id="next">NEXT</button>
    </div>

    <script>

      const imageContainer = document.querySelector('.image-container');
      const prevBtn = document.getElementById('prev');
      const nextBtn = document.getElementById('next');
      
      let x=0;
      prevBtn.addEventListener('click',( ) => {
          x=x+45
          rotate()
      })
      nextBtn.addEventListener('click',( ) => {
          x=x-45
          rotate()
      })
      function rotate() {
          imageContainer.style.transform=`perspective(1000px) rotateY(${x}deg)`;
      }
      
    </script>

</body>
</html>
```
# OUTPUT:
![alt text](<Screenshot 2024-12-22 111808.png>)
![alt text](<Screenshot 2024-12-22 111851.png>)
![alt text](<Screenshot 2024-12-22 111934.png>)
![alt text](<Screenshot 2024-12-22 111905.png>)
![alt text](<Screenshot 2024-12-22 111956.png>)
![alt text](<Screenshot 2024-12-22 112014.png>)
![alt text](<Screenshot 2024-12-22 112204.png>)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
