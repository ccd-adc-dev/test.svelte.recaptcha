<script>

const valida = () => {
    
    console.log("Valida");
    
}
</script>


<h1>Formulario con recaptcha</h1>
<form on:submit={valida()} >

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

<div>
<button type="submit" >Enviar</button>
</div>
</form>
