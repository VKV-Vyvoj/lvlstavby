<script lang="ts">
    // Definovat URL pro logo
    const logoUrl = 'https://firebasestorage.googleapis.com/v0/b/lvstavby-dcc5f.appspot.com/o/354477948_3196963810603328_8421667666525478853_n-removebg-preview%20(1).png?alt=media&token=f60dd99a-db4b-4ec9-938c-67a455c0d11d&_gl=1*1lcn9g3*_ga*NDcxMjk1NjM5LjE2OTg0MDU2NDA.*_ga_CW55HF8NVT*MTY5ODc4MjAzMi4xNi4xLjE2OTg3ODI4NDIuMTMuMC4w';
    let navbar: HTMLDivElement | null = null;
    // Funkce pro obsluhu tlačítka "Napsat email"
    function sendEmail() {
      // Zde můžete implementovat akci pro tlačítko "Napsat email"
    }
  
    // Funkce pro obsluhu tlačítka "Zavolat nám"
    function callUs() {
      // Zde můžete implementovat akci pro tlačítko "Zavolat nám"
    }
  
    // Funkce pro otevření hamburger menu
    function openMenu() {
      if (navbar) {
        navbar.classList.toggle('show');
        document.body.classList.toggle('overlay');
      }
    }
  </script>
  <!-- HTML pro navigační lištu -->
  <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top">
    <div class="container">
      <!-- Logo na levé straně (zobrazeno na mobilech) -->
      <a class="navbar-brand ml-2 d-lg-none" href="/">
        <img src={logoUrl} alt="Logo" height="50" />
      </a>
      <!-- Hamburger menu pro mobilní zařízení (posunuto na pravou stranu) -->
      <button
        class="navbar-toggler d-lg-none ml-auto"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
        on:click={openMenu}
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <!-- Logo na pravé straně (zobrazeno na PC) -->
      <a class="navbar-brand ml-auto d-none d-lg-block" href="/">
        <img src={logoUrl} alt="Logo" height="90" />
      </a>
  
      <!-- Odkazy na PC (zobrazeny na PC) -->
      <div class="collapse navbar-collapse" id="navbarNav" bind:this={navbar}>
        <ul class="navbar-nav justify-content-center">
          <li class="nav-item">
            <a class="nav-link" href="#home">Domů</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#about">O nás</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#services">Služby</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#team">TEXT</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/eshop">TEXT</a>
          </li>
          <li class="nav-item contact-info-pc">
            <a class="nav-link" href="tel:+420736730085">Telefon:</a>
          </li>
          <li class="nav-item contact-info-pc">
            <a class="nav-link" href="#">Adresa:</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://www.instagram.com/r.plusservis/">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-instagram" viewBox="0 0 16 16">
                <path d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"/>
              </svg>
              
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://www.facebook.com/profile.php?id=100087342341713">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-facebook" viewBox="0 0 16 16">
                <path d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"/>
              </svg>
            
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link btn btn-primary" on:click={sendEmail}>Napsat email</a>
          </li>
          <li class="nav-item">
            <a class="nav-link btn btn-success" on:click={callUs}>Zavolat nám</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  
  <!-- HTML pro hamburger menu na mobilních zařízeních -->
  <nav class="navbar navbar-light bg-light d-lg-none">
    <!-- Logo a kontakt (zobrazeno na mobilech) -->
    <div class="container d-flex justify-content-between align-items-center">
      <!-- Odkazy, telefon, adresa a sociální ikony v hamburger menu -->
      <div class="collapse navbar-collapse" id="navbarNav" bind:this={navbar}>
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" href="#home">Domů</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#about">O nás</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#services">Služby</a>
          </li>
          <li class="nav-item">
           
          
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/eshop">TEXT</a>
          </li>
          <li class="nav-item contact-info-mobile">
            <a class="nav-link" href="tel:+420736730085">Telefon:</a>
          </li>
          <li class="nav-item contact-info-mobile">
            <a class="nav-link" href="#">Adresa:</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://www.instagram.com/r.plusservis/">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-instagram" viewBox="0 0 16 16">
                <path d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"/>
              </svg>
            
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="https://www.facebook.com/profile.php?id=100087342341713">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-facebook" viewBox="0 0 16 16">
                <path d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"/>
              </svg>
            
            </a>
          </li>
          
        </ul>
      </div>
    </div>
  </nav>
  
  
   <style>
      /* Styly pro hamburger ikonu */
      .navbar-toggler-icon {
        background-color: #01851e00; /* Barva ikony */
      }
    
      /* Styly pro otevřené hamburger menu */
      .navbar-collapse.show {
        background-color: #fff; /* Barva pozadí */
        position: absolute; /* Překryje obsah na pozadí */
        top: 60px; /* Výška menu nad obsahem */
        left: 0;
        right: 0;
        border-bottom: 1px solid #ccc; /* Oddělovací linka pod menu */
      }
    
      /* Styly pro odkazy v otevřeném hamburger menu */
      .navbar-nav {
        margin: 0;
        padding: 0;
      }
    
      .nav-item {
        text-align: center;
      }
    
      .nav-link {
        padding: 10px 20px;
        display: block;
      }
    
      /* Styly pro ikony sociálních sítí v hamburger menu */
      .social-icons a {
        display: block;
        margin: 10px auto;
      }
    
      /* Styly pro kontakt info v hamburger menu na mobilech */
      .contact-info-mobile {
        text-align: center;
        padding: 20px;
        border-top: 1px solid #ccc; /* Oddělovací linka nad kontaktními informacemi */
      }
    
      /* Styly pro mobilní zařízení (maximální šířka 768px) */
      @media (max-width: 768px) {
        .navbar {
          padding: 10px;
        }
        .navbar-brand {
          margin-left: 0;
        }
        .nav-item {
          margin-right: 0;
        }
        .btn {
          font-size: 14px;
          padding: 8px 16px;
        }
      }
    
      /* Styly pro tlačítka a kontaktní informace na počítači (zobrazeny na PC) */
      .contact-info-pc {
        text-align: center;
        padding: 10px 20px;
      }
    
      .contact-info-pc a {
        text-align: center;
      }
    
      .contact-info, .social-icons, .btn {
        font-size: 16px;
        padding: 10px 20px;
      }
    
      .contact-info {
        margin-right: 20px;
      }
    
      .social-icons {
        margin-right: 20px;
      }
    
      .social-icons a {
        margin-right: 10px;
        margin-left: 10px;
      }
    
      .btn {
       
        background: transparent;
        color: rgb(202, 139, 3);
        transition: background-color 0.3s, color 0.3s;
      }
    
      .btn:hover {
        background-color: #805700;
        color: white;
      }
  
       /* Styly pro overlay */
    .overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5); /* Průhledné černé pozadí */
      z-index: 100; /* Zajistí, že overlay bude nad obsahem stránky */
    }
  
    .overlay.show {
      display: block;
    }
    </style>