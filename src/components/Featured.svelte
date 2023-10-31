<script lang="ts">
    import Swal from 'sweetalert2';
  
    // Deklarace ceníkových položek
 
  
    // Text s důležitými informacemi
    let importantInfo = `
      <p><strong>Důležité:</strong></p>
      <p>Platba bude provedena v hotovosti k rukám vedoucího pracovníka po dokončení stěhování nebo převodem na ÚČET firmy R+ SERVIS s.r.o. u České spořitelny 6395986309/0800 variabilní symbol: ČÍSLO NABÍDKY a to nejpozději dva dny před termínem stěhovaní.</p>
      <p>Všechny ceny v nabídce jsou uvedeny bez DPH. Minimální zúčtovací sazba je 3 hodiny.</p>
      <p>Veškeré nástěnné montážní práce jsou prováděny pouze proškolenými pracovníky za použití špičkového nářadí DeWalt s přímým odsáváním prachu. Díky tomu Vám šetříme čas strávený při úklidu i peníze.</p>
      <p>Při zrušení termínu stěhování bude účtován STORNO poplatek ve výši 3000,-</p>
    `;
  
    const openModal = (title: string, content: string | null) => {
    if (title === "E-SHOP") {
      Swal.fire({
        title: title,
        html: content
          ? `
            <div class="modal-content">
              ${content}
              <div class="modal-buttons">
                <button id="go-to-eshop" class="btn btn-primary">Přejít na E-SHOP</button>
              </div>
            </div>
          `
          : '', // Pokud je content null, použije se prázdný řetězec
        showCloseButton: false, // Zde vypněte zobrazování výchozího tlačítka "Zavřít"
      });
  
      // Přidejte posluchače událostí na tlačítka
      const closeModalButton = document.getElementById("close-modal");
      if (closeModalButton) {
        closeModalButton.addEventListener("click", () => {
          Swal.close();
        });
      }
  
      const goToEshopButton = document.getElementById("go-to-eshop");
      if (goToEshopButton) {
        goToEshopButton.addEventListener("click", () => {
          // Přesměrování na stránku "/eshop"
          window.location.href = "/eshop";
        });
      }
    } else {
      Swal.fire({
        title: title,
        html: content ? content : '', // Pokud je content null, použije se prázdný řetězec
        showCloseButton: true,
      });
    }
  };
  
  
  </script>
  
  
  
  <div id="main">
    <section id="featured-services" class="featured-services section-bg">
      <div class="container">
        <div class="row no-gutters">
          <div class="col-lg-4 col-md-6">
            <div class="icon-box">
              <div class="icon"><i class="bi bi-laptop"></i></div>
              <h4 class="title"><a>Informace k platbě</a></h4>
              <p class="description">Přečtěte si veškeré informace k platbám</p>
            </div>
          </div>
          <div class="col-lg-4 col-md-6">
            <div class="icon-box">
              <div class="icon"><i class="bi bi-briefcase"></i></div>
              <h4 class="title"><a>Ceník</a></h4>
              <p class="description">Přečtěte si veškeré informace o našich cenách.</p>
            </div>
          </div>
          <div class="col-lg-4 col-md-6">
            <div class="icon-box">
              <div class="icon"><i class="bi bi-calendar4-week"></i></div>
              <h4 class="title">Bazar</a></h4>
              <p class="description">Občas nám zbydou pěkné kousky, které by mohli ještě posloužit, mrkněte.</p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
  