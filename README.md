# Ex.08 Design of Interactive Image Gallery
# Date: 21 / 10 / 2024
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
## CarCollections.html 
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cars</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Lavishly+Yours&family=Playwrite+HU:wght@100..400&family=Sora:wght@100..800&display=swap');

        * {
            padding: 0px;
            margin: 0px;
        }

        body {
            background-color: black;
            color: aliceblue;
            font-family: "Lavishly Yours", cursive;
            font-weight: 400;
            font-style: normal;
            font-size: 80px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }



        .cars {
            display: flex;
            align-items: flex-end;
            justify-content: space-evenly;
            width: 100%;
        }

        h2 {
            text-align: center;
        }

        svg {
            height: 200px;
            width: 200px;
            cursor: pointer;
        }

        img {
            width: 800px;
            height: 500px;
        }
    </style>
</head>

<body>
    <h1>Car Collection Image Gallery </h1>
    <div class="cars">
        <svg onclick="decrement()" xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960"
            width="24px" fill="#e8eaed">
            <path
                d="m480-320 56-56-64-64h168v-80H472l64-64-56-56-160 160 160 160Zm0 240q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-80q134 0 227-93t93-227q0-134-93-227t-227-93q-134 0-227 93t-93 227q0 134 93 227t227 93Zm0-320Z" />
        </svg>
        <div class="car" id="car">

        </div>
        <svg onclick='increment()' xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 -960 960 960"
            width="24px" fill="#e8eaed">
            <path
                d="m480-320 160-160-160-160-56 56 64 64H320v80h168l-64 64 56 56Zm0 240q-83 0-156-31.5T197-197q-54-54-85.5-127T80-480q0-83 31.5-156T197-763q54-54 127-85.5T480-880q83 0 156 31.5T763-763q54 54 85.5 127T880-480q0 83-31.5 156T763-197q-54 54-127 85.5T480-80Zm0-80q134 0 227-93t93-227q0-134-93-227t-227-93q-134 0-227 93t-93 227q0 134 93 227t227 93Zm0-320Z" />
        </svg>
    </div>
    <script>
        function createCar(obj) {
            const car = document.getElementById('car')
            car.innerHTML = ''
            const img = document.createElement('img')
            img.src = obj.img
            img.alt = obj.name
            img.className = 'shape'
            car.append(img)
            const h1 = document.createElement('h2')
            h1.innerText = obj.name
            car.append(h1)
        }
        const arr = [{
            img: './pictures/benz.jpeg',
            name: 'Mercedes Benz'
        }, {
            img: './pictures/audi.jpg',
            name: 'Audi'
        }, {
            img: './pictures/bmw.jpeg',
            name: 'BMW'
        }, {
            img: './pictures/rools.jpeg',
            name: 'Rolls Royce'
        }, {
            img: './pictures/ferari.jpeg',
            name: 'Ferrari'
        },]
        let index = 0
        function increment() {
            if (index < arr.length) {
                index += 1;
                createCar(arr[index])
            }
        }
        function decrement() {
            if (index >= 0) {
                index--;
                createCar(arr[index])

            }
        }
        createCar(arr[index])



    </script>
</body>

</html>
```
# OUTPUT:
## Image 1 
![image](https://github.com/user-attachments/assets/ec7c2703-ccdc-4397-9d8e-912e1138ee64)
## Image 2
![image](https://github.com/user-attachments/assets/848d10f4-8095-4bdd-9996-0fd81978e47e)
## Image 3 
![image](https://github.com/user-attachments/assets/0c798590-c57e-496a-8e33-afa7174d687b)
## Image 4
![image](https://github.com/user-attachments/assets/09252f5c-54dc-46b8-a5fa-88ad9d76c065)
## Image 5 
![image](https://github.com/user-attachments/assets/6ae3c137-0a0e-4084-b7fa-d4da6fa59773)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
