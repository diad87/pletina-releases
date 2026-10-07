# Pletina

Reproductor de música tipo Spotify para **Windows, Mac, Linux y Android**. Buscas un grupo, eliges un disco y suena: cada canción se reproduce en streaming de solo audio desde YouTube Music, sin anuncios. Biblioteca, playlists, historial, cola tipo DJ y descargas para escuchar sin conexión (también en el móvil); en el PC, además, tu propia música.

Antes se llamaba Musify. Es software libre ([GPL-3.0](https://github.com/diad87/pletina/blob/main/LICENSE)): el código está en [diad87/pletina](https://github.com/diad87/pletina). Aquí se publican las versiones.

![Inicio](screenshots/inicio.png)

| | |
|---|---|
| ![Disco](screenshots/disco.png) | ![Artista](screenshots/artista.png) |
| **Disco:** la portada tiñe toda la pantalla | **Artista:** foto de cabecera y sus canciones más escuchadas |
| ![Sonando ahora](screenshots/sonando.png) | ![Buscar](screenshots/buscar.png) |
| **Sonando ahora:** pantalla completa con la cola | **Buscar:** artistas y discos de Deezer |

## En el móvil

La misma app, pensada para el dedo. La música sigue sonando con la pantalla apagada y se maneja desde la pantalla de bloqueo, la notificación y los auriculares. Los discos y playlists se descargan para escucharlos sin conexión (desde la 0.6.0), y siguen bajando aunque salgas de la app.

<table>
  <tr>
    <td width="33%"><img src="screenshots/movil-inicio.png" alt="Inicio en el móvil" width="100%"></td>
    <td width="33%"><img src="screenshots/movil-sonando.png" alt="Sonando ahora en el móvil" width="100%"></td>
    <td width="33%"><img src="screenshots/movil-cola.png" alt="Cola en el móvil" width="100%"></td>
  </tr>
  <tr>
    <td><b>Inicio</b>, con lo que suena abajo</td>
    <td><b>Sonando ahora</b>: se cierra deslizando hacia abajo</td>
    <td><b>Cola</b>: tu cola se ordena arrastrando el asa</td>
  </tr>
  <tr>
    <td width="33%"><img src="screenshots/movil-disco.png" alt="Disco en el móvil" width="100%"></td>
    <td width="33%"><img src="screenshots/movil-biblioteca.png" alt="Tu biblioteca en el móvil" width="100%"></td>
    <td width="33%"><img src="screenshots/movil-bloqueo.png" alt="Pantalla de bloqueo" width="100%"></td>
  </tr>
  <tr>
    <td><b>Disco</b></td>
    <td><b>Tu biblioteca</b>: playlists y discos guardados</td>
    <td><b>Pantalla de bloqueo</b>: sigue sonando con la pantalla apagada</td>
  </tr>
</table>

## Instalar

Descarga el archivo de tu sistema desde la [última versión](https://github.com/diad87/pletina-releases/releases/latest) (hasta la 0.6.0, los archivos se llaman `Musify_…`):

| Sistema | Archivo |
|---|---|
| Windows 10/11 | `Pletina_x.y.z_x64-setup.exe`: doble clic |
| Mac (chip de Apple o Intel, macOS 11+) | `Pletina_x.y.z_universal.dmg`: arrastrar a Aplicaciones |
| Linux (64 bits) | `Pletina_x.y.z_amd64.AppImage` (cualquier distribución) o `.deb` (Ubuntu/Debian) |
| Android 7 o superior (64 bits) | `Pletina_x.y.z_android.apk`, mejor con Obtainium (abajo) para que se actualice sola |

Los instaladores de escritorio todavía no están firmados por Microsoft ni Apple, así que la primera vez el sistema avisa. En Windows: «Más información» → «Ejecutar de todas formas». En Mac: clic derecho en la app → Abrir. Solo pasa al instalarla: las actualizaciones las baja la propia app. La firma del instalador de Windows está solicitada (ver la [política de firma](https://github.com/diad87/pletina#code-signing-policy)).

Si tenías Musify, Pletina la sustituye y conserva tu biblioteca.

### Android, con Obtainium

Pletina no está en Google Play. [Obtainium](https://github.com/ImranR98/Obtainium) instala el APK desde aquí y lo actualiza cuando sale una versión nueva:

1. Instala Obtainium (desde su GitHub o desde F-Droid).
2. En Obtainium, «Añadir app», pega `https://github.com/diad87/pletina-releases` y pulsa «Añadir».
3. Pulsa «Instalar». La primera vez, Android pide permiso para instalar apps desde Obtainium.

Si ya la tenías en Obtainium con la dirección antigua (`musify-releases`), GitHub la redirige al nombre nuevo. Si Obtainium deja de encontrar versiones, bórrala de Obtainium (sin desinstalar la app) y vuelve a añadirla con la dirección nueva.

## Se actualiza sola

En el PC, la app busca versiones nuevas al arrancar y cada pocas horas, las descarga en segundo plano y las instala al cerrarse. En Linux, las actualizaciones automáticas funcionan con el AppImage.

En Android, Obtainium avisa de cada versión nueva y la instala encima sin perder la biblioteca. La app también lo dice en «Tu biblioteca».

Todas las versiones van firmadas: la app de escritorio no instala nada que no lleve nuestra firma, y Android no deja instalar encima un APK firmado por otro.

## Privacidad

Sin cuentas, sin analíticas y sin servidores propios: tu biblioteca se guarda solo en tu equipo. La app se conecta a Deezer (catálogo y carátulas), YouTube (el audio) y GitHub (actualizaciones). Más detalle en el [README del código](https://github.com/diad87/pletina#privacidad).
