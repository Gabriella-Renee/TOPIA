<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>TOPIA</title>

    <link rel="stylesheet" media="screen" href="assets/styles/main.css" charset="utf-8">
    <link href="https://fonts.googleapis.com/css?family=Arimo:400,400i,700,700i|Cabin:400,400i,500,500i,600,600i,700,700i|Vollkorn:400,400i,700,700i" rel="stylesheet">



  </head>

  <body>
    <main>

        <h1>TOPIA</h1>

      <nav class="social_media">
        <a href="https://www.instagram.com/topiamagazine/"><img id="first" src="assets/images/instagram.gif" alt="" /></a>
        <a href="http://www.facebook.com"><img id="first" src="assets/images/facebook.jpg" alt="" /></a>
        <a href="https://au.pinterest.com/EllaBetts1595/topia/"><img id="first" src="assets/images/pinterest.jpeg" alt="" /></a>
      </nav>

      <div class="border">
      <h2>Issue 1: France From An Outsiders Perspective...</h2>
      </div>

      <div class="border-two">
      <nav>
        <a id="main" href="influences.html">INFLUENCES</a>
        <a id="main" href="aesthetics.html">AESTHETICS</a>
        <a id="main" href="destinations.html">DESTINATIONS</a>
        <a id="main" href="immersion.html">IMMERSION</a>
        <a id="main" href="Concept.html">CONCEPT</a>
      </nav>
      </div>

      <div id="image-area">
        <!-- This empty div is populated randomly through the Javascript below -->
      </div>

    </main>

    <script type="text/javascript">

    // This creates a blank array and then populates it sequentially from 1 to 16
    // Change the number 16 below to however many images you add. Make sure to name them topia-#.jpg
    var imageAreaArray = [];
    for (var i = 1; i <= 15; i = i + 1) {
      imageAreaArray.push(i)
    }

    // This reorders that first array randomly
    imageAreaArray.sort(function() {
      return 0.5 - Math.random()
    });

    // This populates the div #image-area with your images. It does it randomly using the array above
    // Change the number 15 below to one less than the total of images
    var imageArea = document.getElementById('image-area');
    for (var i = 0; i <= 14; i = i + 1) {
      var image = imageAreaArray[i];
      imageArea.innerHTML = imageArea.innerHTML + "<img src='assets/images/topia-" + image + ".jpg'>";
    }

    // This checks if the images are portrait or landscape and applies a class accordingly
    // Change the number 15 below to one less than the total of images
    for (var i = 0; i <= 14; i = i + 1) {
      var currentImage = imageArea.getElementsByTagName('img')[i];
      currentImage.addEventListener('load', function() {
        if (this.naturalWidth > this.naturalHeight) {
          this.className += 'landscape'
        } else {
          this.className += 'portrait'
        }
      })
    }

    </script>

    <a href="Lipstick.html"><figure><img id="landscape-home" src="assets/images/Danielle_landscape.jpg" alt=""/>
    </figure>

  </body>
</html>
