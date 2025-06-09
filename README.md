# lilitahouse-lilitadesign
#Codigos de consulta por seccion

#Codigo css del search-form en pagina de inicio(global)

/*Estilos basicos del seach-form*/
.search-form-label label {
    color: #008FA9;
    font-family: 'Roboto', sans-serif;
  text-transform: uppercase;
  font-size: 14px;
}

/*estilos del elemento select del search-form*/
.search-form-label select {
    border-radius: 10px !important;
    border-color: white !important;
    box-shadow: 0px 5px 10px rgba(173, 173, 173, 0.25);
}

/*estilos especifico elemento select de invitados del search-form*/

.mphb_sc_search-adults select {
    border-radius: 10px !important;
    border-color: white !important;
    box-shadow: 0px 5px 10px rgba(173, 173, 173, 0.25);
}

/*estilos del boton del search-form*/

.search-form-label .button  {
   padding-top: 15px;
   padding-bottom: 15px;
   padding-left: 30px;
   padding-right: 30px;
}

/*estilos de los elementos input del search-form*/
.mphb_sc_search-submit-button-wrapper input.button {
    font-family: 'Raleway';
    font-size: 18px;
    font-weight: 500;
    letter-spacing: 1px;
}

/*estilos del wrapper que contiene los inputs de checkin-checkout del search-form*/

.mphb-datepick {
    border-radius: 10px !important;
    border: 1px solid white !important;
    box-shadow: 0px 5px 10px rgba(173, 173, 173, 0.25) !important;
    font-family: 'Raleway';
    font-size: 16px;
    font-weight: 600;
    letter-spacing: 1px;
    color: black;
}

# Script del search-form pagina de inicio(global)
<script>
document.addEventListener("DOMContentLoaded", function () {
  const select = document.querySelector('select[name="mphb_attributes[tipo-de-reserva]"]');
  if (select) {
    select.value = "78";
  }
});
</script>

# Codigo css del search-form para retiros(global)
.search-form-label label {
    color: #008FA9;
}

.search-form-label select {
    border-radius: 10px !important;
    box-shadow: 0px 0px 3px rgba(0, 0, 0, 0.25);
}

.search-form-label .button  {
   padding-left: 30px;
   padding-right: 30px;
}

.mphb-datepick {
    border-radius: 10px !important;
    box-shadow: 0px 0px 3px rgba(0, 0, 0, 0.25);
}

#retreat-date .search-form-label .mphb_sc_search-adults {
    display: none;
}

#retreat-title-page .search-form-label .mphb_sc_search-adults {
    display: none;
}

#search-retreat-movil .mphb_sc_search-adults {
    display: none;
}

# Script del search-form para retiros
<script>
document.addEventListener("DOMContentLoaded", function () {
  const select = document.querySelector('select[name="mphb_attributes[tipo-de-reserva]"]');
  const form = document.querySelector('.search-form-label');
  
  console.log(form)
  
  if (select) {
    select.value = "79";
  }

});
</script>

----------------------------------

# codigo de checkout columna izquierda

<script>
  document.addEventListener("DOMContentLoaded", function() {
    const original = document.getElementById("mphb-price-details");
    const destino = document.getElementById("datos-precio");

    if (original && destino) {
      // Clonar toda la sección (estructura + contenido)
      const clon = original.cloneNode(true);

      // (Opcional) Si tienes funciones JS asociadas con botones u otros elementos
      // y fueron agregadas con addEventListener, deberías reasignarlas aquí manualmente.

      // Por ejemplo: clonar un evento a un botón específico
      const originalBtn = original.querySelector(".mi-boton");
      const clonBtn = clon.querySelector(".mi-boton");

      if (originalBtn && clonBtn) {
        clonBtn.addEventListener("click", function(e) {
          console.log("¡Botón dentro del clon fue clicado!");
          // Aquí puedes replicar el comportamiento original
        });
      }

      // Agregar el clon al destino
      destino.appendChild(clon);
      destino.style.fontFamily = "Roboto";
      destino.style.fontSize = "18px";
    }
  });
</script>

# Codigo Css de la columna izquierda

#datos-precio {
    max-height: 400px;
    font-family: 'Roboto';
    font-size: 16px;
    letter-spacing: 1px;
    color: black;
}

.mphb-price-breakdown-dates,  .mphb-price-breakdown-fees,  .mphb-price-breakdown-fee-taxes, .mphb-price-breakdown-total, .mphb-price-breakdown-accommodation-taxes {
    background-color: #008FA9;
    color: white;
}

.mphb-price-breakdown-dates,  .mphb-price-breakdown-date {
    display: none;
}


@media (max-width: 1315px) {
    #datos-precio {
        display: none;
    }
}

----------------------------------

# codigo css de la columna derecha 

#checkout-form {
    font-family: 'Roboto';
    font-size: 16px;
    letter-spacing: 1px;
    color: black;
}

#checkout-form input {
    border-radius: 10px !important;
    border: 1px solid white !important;
    box-shadow: 0 1px 6px 0 #e6ebf1 !important;
}

#checkout-form select {
        border-radius: 10px !important;
    border-color: white !important;
    box-shadow: 0 1px 6px 0 #e6ebf1;
}

#checkout-form textarea {
    border-radius: 10px !important;
    border-color: white !important;
    box-shadow: 0 1px 6px 0 #e6ebf1;
}

.mphb-customer-marketing-consent label {
    padding: 10px;
}

.mphb-customer-privacy-policy label {
    padding: 10px;
} 

.mphb-login-form-wrap, .mphb-room-details, .mphb-reserve-rooms-details  {
    display: none;
}

#checkout-form #mphb-price-details {
    display: none;
}



@media (max-width: 1315px) {
     #checkout-form #mphb-price-details {
        display: block;
    }
}

.mphb-customer-security-deposit-header {
    margin-top: 50px;
}
