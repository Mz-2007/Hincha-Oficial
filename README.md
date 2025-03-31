<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imagen en HTML</title>
    <style>
        body {
            display: flex;
            justify-content: center; /* Centra horizontalmente */
            align-items: center;     /* Centra verticalmente */
            height: 100vh;           /* Hace que el body ocupe toda la altura de la ventana */
            margin: 0;
        }

        .imagen {
            width: 45%;  /* Cambia el tamaño de la imagen a un 60% del contenedor */
            height: auto; /* Mantiene la proporción de la imagen */
            transform: rotate(-90deg); /* Gira la imagen */
            transition: transform 0.5s ease; /* Suaviza la rotación */
        }
    </style>
</head>
<body>
<script>
  const qrCodeId = "miQR123"; // Un identificador único para este QR

  // Verificar si ya se usó en este navegador
  if (localStorage.getItem(qrCodeId)) {
      document.body.innerHTML = "<h1>⚠️ESTE CODIGO QR YA FUE USADO NO INTENTES ENGAÑAR⚠️.</h1>";
  } else {
      // Guardar en el almacenamiento local que ya fue usado
      localStorage.setItem(qrCodeId, "usado");

      // Mostrar la información normal
      document.body.innerHTML = `
          <h1>SOCIO #0005</h1>
          <img src="C:/Users/mz096/OneDrive/Escritorio/HinchaOficial/Picsart_25-03-19_00-09-05-675.jpg" alt="Imagen girada" class="imagen">
      `;
  }
</script>
</body>
</html>
