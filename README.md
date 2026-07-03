# Seguimiento presupuesto Levi's 2026

Landing estática de Comercializadora UB Cuarenta para presentar la ejecución del fondo de mercadeo asignado por Levi's.

## Publicar con GitHub Pages

1. Crea un repositorio en GitHub.
2. Sube todo el contenido de esta carpeta, excepto los archivos excluidos por `.gitignore`.
3. En GitHub abre **Settings → Pages**.
4. En **Build and deployment**, selecciona **Deploy from a branch**.
5. Selecciona la rama `main`, carpeta `/ (root)` y guarda.
6. GitHub mostrará la dirección pública del informe cuando termine la publicación.

## Actualizar el informe

La página incluye el botón **Actualizar informe**. Este permite cargar un archivo `.xlsx` o `.xlsm` con las hojas:

- `Dispersión`: presupuesto anual y distribución trimestral.
- `Reporte de ejecución`: movimientos, estados y tipo de pago.
- `Evidencias`: fotografías alojadas en Google Drive.

El formato base está disponible dentro de `downloads/` y también se descarga desde la propia landing.

Para cada fotografía de Drive, configura el acceso como **Cualquier persona con el enlace** y pega el vínculo en la columna `Enlace de Drive`.

La última carga queda almacenada en el navegador del usuario. No modifica los archivos publicados en GitHub.

## Estructura

```text
index.html
assets/
  css/styles.css
  js/app.js
  js/data.js
  js/import-excel.js
  logos/
downloads/
  FORMATO SEGUIMIENTO PPTO 2026 CON EVIDENCIAS.xlsx
```

## Privacidad

`assets/js/data.js` contiene el detalle utilizado para la carga inicial del informe. En un repositorio público, esta información será accesible para cualquier persona. Usa un repositorio privado o elimina los datos iniciales si el reporte no debe ser público.

## Modo administrador

La vista pública no muestra controles de actualización. Para administrar el informe, agrega `?admin=1` al final de la dirección:

```text
https://usuario.github.io/repositorio/?admin=1
```

En este modo:

1. Carga el Excel desde **Cargar Excel**.
2. Revisa las cifras y las evidencias de Drive.
3. Pulsa **Descargar actualización**.
4. Reemplaza `assets/js/data.js` en el repositorio de GitHub por el archivo descargado.

La URL sin `?admin=1` conserva la presentación limpia para gerencia.
