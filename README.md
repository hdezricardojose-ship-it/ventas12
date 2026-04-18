<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Tienda Online</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f4f4f4;
    }
    header {
      background: #333;
      color: white;
      padding: 15px;
      text-align: center;
    }
    .container {
      padding: 20px;
    }
    .productos {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 20px;
    }
    .producto {
      background: white;
      padding: 15px;
      border-radius: 10px;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
    button {
      background: green;
      color: white;
      border: none;
      padding: 10px;
      cursor: pointer;
      border-radius: 5px;
    }
    button:hover {
      background: darkgreen;
    }
    form {
      margin-top: 30px;
      background: white;
      padding: 20px;
      border-radius: 10px;
    }
    input, select {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
    }
  </style>
</head>
<body>

<header>
  <h1>Mi Tienda Online</h1>
</header>

<div class="container">
  <h2>Productos</h2>

  <div class="productos">
    <div class="producto">
      <h3>Camiseta</h3>
      <p>$20</p>
      <button onclick="seleccionarProducto('Camiseta')">Comprar</button>
    </div>

    <div class="producto">
      <h3>Zapatos</h3>
      <p>$50</p>
      <button onclick="seleccionarProducto('Zapatos')">Comprar</button>
    </div>

    <div class="producto">
      <h3>Gorra</h3>
      <p>$15</p>
      <button onclick="seleccionarProducto('Gorra')">Comprar</button>
    </div>
  </div>

  <h2>Formulario de compra</h2>

  <form onsubmit="enviarFormulario(event)">
    <input type="text" placeholder="Nombre completo" required>
    <input type="email" placeholder="Correo electrónico" required>

    <select id="producto" required>
      <option value="">Selecciona un producto</option>
      <option value="Camiseta">Camiseta</option>
      <option value="Zapatos">Zapatos</option>
      <option value="Gorra">Gorra</option>
    </select>

    <input type="number" placeholder="Cantidad" required>

    <button type="submit">Comprar</button>
  </form>
</div>

<script>
  function seleccionarProducto(nombre) {
    document.getElementById("producto").value = nombre;
    alert("Seleccionaste: " + nombre);
  }

  function enviarFormulario(e) {
    e.preventDefault();
    alert("¡Compra realizada con éxito!");
  }
</script>

</body>
</html>
