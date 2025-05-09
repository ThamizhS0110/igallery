# Ex.08 Design of Interactive Image Gallery
## Date:08.05.2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interactive Photo Gallery</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 p-6">

  <h1 class="text-3xl font-bold text-center mb-8">Interactive Photo Gallery</h1>

  <!-- Image Gallery Grid -->
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
    <img src="a.jpeg" alt="Gallery 1"
         class="cursor-pointer rounded shadow hover:scale-105 transition"
         onclick="openLightbox(this.src)" />
         
    <img src="b.jpg" alt="Gallery 2"
         class="cursor-pointer rounded shadow hover:scale-105 transition"
         onclick="openLightbox(this.src)" />
         
    <img src="c.png" alt="Gallery 3"
         class="cursor-pointer rounded shadow hover:scale-105 transition"
         onclick="openLightbox(this.src)" />
         
    <img src="download.jpeg" alt="Gallery 4"
         class="cursor-pointer rounded shadow hover:scale-105 transition"
         onclick="openLightbox(this.src)" />
  </div>

  <!-- Lightbox Modal -->
  <div id="lightbox" class="fixed inset-0 bg-black bg-opacity-80 hidden items-center justify-center z-50">
    <img id="lightbox-img" class="max-w-full max-h-full rounded shadow-2xl" />
    <button onclick="closeLightbox()"
            class="absolute top-4 right-4 text-white text-3xl font-bold hover:text-red-400 transition">
      &times;
    </button>
  </div>

  <!-- JavaScript -->
  <script>
    function openLightbox(src) {
      const lightbox = document.getElementById('lightbox');
      const lightboxImg = document.getElementById('lightbox-img');

      lightboxImg.src = src;
      lightbox.classList.remove('hidden');
      lightbox.classList.add('flex');
    }

    function closeLightbox() {
      const lightbox = document.getElementById('lightbox');
      lightbox.classList.remove('flex');
      lightbox.classList.add('hidden');
    }

    // Optional: Close lightbox on outside click
    document.getElementById('lightbox').addEventListener('click', function (e) {
      if (e.target.id === 'lightbox') {
        closeLightbox();
      }
    });
  </script>

</body>
</html>

```

## OUTPUT:
![alt text](<Screenshot 2025-05-08 163107.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
