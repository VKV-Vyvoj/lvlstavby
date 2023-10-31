<script lang="ts">
    import { onMount, onDestroy } from "svelte";
  
    let currentIndex = 0;
    
    const carouselImages = [
      "https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/367400655_17855730939008336_8572029795615723865_n.jpg?alt=media&token=12db99ad-faf6-477e-ace6-a0c5cfdb1ad3&_gl=1*1gaha4n*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4NTczMy4xNy4xLjE2OTg3ODU4MjUuNjAuMC4w",
      "https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/367400655_17855730939008336_8572029795615723865_n.jpg?alt=media&token=12db99ad-faf6-477e-ace6-a0c5cfdb1ad3&_gl=1*1gaha4n*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4NTczMy4xNy4xLjE2OTg3ODU4MjUuNjAuMC4w",
      "https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/367400655_17855730939008336_8572029795615723865_n.jpg?alt=media&token=12db99ad-faf6-477e-ace6-a0c5cfdb1ad3&_gl=1*1gaha4n*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4NTczMy4xNy4xLjE2OTg3ODU4MjUuNjAuMC4w",
      "https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/367400655_17855730939008336_8572029795615723865_n.jpg?alt=media&token=12db99ad-faf6-477e-ace6-a0c5cfdb1ad3&_gl=1*1gaha4n*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4NTczMy4xNy4xLjE2OTg3ODU4MjUuNjAuMC4w",
      "https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/367400655_17855730939008336_8572029795615723865_n.jpg?alt=media&token=12db99ad-faf6-477e-ace6-a0c5cfdb1ad3&_gl=1*1gaha4n*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4NTczMy4xNy4xLjE2OTg3ODU4MjUuNjAuMC4w",
      "https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/367400655_17855730939008336_8572029795615723865_n.jpg?alt=media&token=12db99ad-faf6-477e-ace6-a0c5cfdb1ad3&_gl=1*1gaha4n*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4NTczMy4xNy4xLjE2OTg3ODU4MjUuNjAuMC4w"
    ];
  
    function changeImage() {
      currentIndex = (currentIndex + 1) % carouselImages.length;
    }
  
    onMount(() => {
      let interval = setInterval(changeImage, 5000);
  
      onDestroy(() => {
        clearInterval(interval);
      });
    });
  </script>
  
  <section class="px-5 py-6 py-xxl-10 hcf-bp-center hcf-bs-cover hcf-overlay hcf-transform" style="background-image: url({carouselImages[currentIndex]});">
    <div class="container">
      <div class="row justify-content-md-center">
        <div class="col-12 col-md-11 col-lg-9 col-xl-7 col-xxl-6 text-center text-white">
          <img class="logo" src="https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/354477948_3196963810603328_8421667666525478853_n-removebg-preview%20(1).png?alt=media&token=f60dd99a-db4b-4ec9-938c-67a455c0d11d&_gl=1*1lcn9g3*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4MjAzMi4xNi4xLjE2OTg3ODI4NDIuMTMuMC4w" alt="Logo">
          <h1 class="lead mb-5 animation-slide-up">Stavební firma pro vaše sny.</h1>
          <div class="d-grid gap-2 d-sm-flex justify-content-sm-center">
          </div>
        </div>
      </div>
    </div>
  </section>
  
  <style>
    .hcf-bp-center {
      background-position: center !important;
    }
  
    .hcf-bs-cover {
      background-size: cover !important;
    }
  
    .py-xxl-10 {
      padding-top: 15.75rem !important;
      padding-bottom: 15.75rem !important;
    }
  
    .hcf-overlay {
      --hcf-overlay-opacity: 0.5;
      --hcf-overlay-bg-color: var(--bs-black-rgb);
      position: relative;
    }
  
    .hcf-overlay::after {
      display: block;
      content: "";
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      background-color: rgba(
        var(--hcf-overlay-bg-color),
        var(--hcf-overlay-opacity)
      );
      z-index: 0;
    }
  
    .hcf-overlay > * {
      position: relative;
      z-index: 1;
    }
  
    .hcf-transform {
      transform: scale3d(1, 1, 1);
      transform-style: preserve-3d;
      transition: all 0.5s;
    }
  
    .hcf-transform:hover {
      transform: scale3d(1.02, 1.02, 1.02);
    }
  
    .logo {
      animation: slide-in-left 5s forwards;
      max-width: 100%; /* Responzivní šířka obrázku */
    }
  
    .animation-slide-up {
      animation: slide-up 5s forwards;
    }
  
    @keyframes slide-in-left {
      from {
        transform: translateX(-100%);
        opacity: 0;
      }
      to {
        transform: translateX(0);
        opacity: 1;
      }
    }
  
    @keyframes slide-up {
      0% {
        transform: translateY(50px);
        opacity: 0;
      }
      100% {
        transform: translateY(0);
        opacity: 1;
      }
    }
    
    h1{
      font-weight: 100;
      text-decoration: dashed;
    }
  </style>
  