<script>

  const siteKey = "6Lc_s-EUAAAAACWS7IpdI5nnh4krvflPvM00ah8l";

  let respuesta;

  const valida = e => {
    let nombre = e.target[0].value;
    let correo = e.target[1].value;
    let mensaje = e.target[2].value;
    let captcha = e.target[3].value;

    if (!!captcha) {
    //   console.log("Valida", nombre, correo, mensaje, captcha);
      respuesta.style.color = "green";
      respuesta.innerHTML = "Se han enviado los datos";
    } else {
        //   console.log("No se ha contestado el captcha");
      respuesta.style.color = "red";
      respuesta.innerHTML = "No se ha contestado el captcha";
    }
  };

</script>

<h1>Formulario con recaptcha</h1>
<form on:submit|preventDefault={valida}>

  <label>
    Nombre:
    <input type="text" placeholder="Nombre" />
  </label>
  <label>
    Correo:
    <input type="email" placeholder="Correo" />
  </label>
  <label>
    Mensaje:
    <textarea name="mensaje" id="mensaje" />
  </label>

  <div class="g-recaptcha" data-sitekey={siteKey} />

  <div>
    <button type="submit">Enviar</button>
  </div>
  <p class="respuesta" bind:this={respuesta} />
</form>
