# Pletina

Pletina es un reproductor de música y pódcasts disponible como **app web en iPhone, iPad, Android, Windows, macOS y Linux**. Puedes crear playlists, importar listas de Spotify y descargar el audio disponible para escucharlo sin conexión.

**[Abrir Pletina en Tuqo](https://pletina-app.tuqo.ru/)** · [Instalar en iPhone y iPad](#instalar-en-iphone-y-ipad) · [Descargar instaladores nativos](#instalar)

Aquí se publican las versiones nativas y sus actualizaciones. Pletina es software libre con licencia [GPL-3.0](https://github.com/diad87/pletina/blob/main/LICENSE). Antes se llamaba Musify. [Repositorio del código fuente](https://github.com/diad87/pletina).

## Instalar en iPhone y iPad

Abre [Pletina en Safari](https://pletina-app.tuqo.ru/). En el menú **Compartir**, toca **Añadir a pantalla de inicio**. Si aparece **Abrir como app web**, actívalo y toca **Añadir**. También puedes elegir **Probar sin instalar** en la web. [Guía de Apple para iPhone](https://support.apple.com/es-es/guide/iphone/iphea86e5236/ios).

En Android y en el ordenador, abre la web oficial y pulsa **Instalar Pletina** para seguir los pasos de tu navegador.

### Llevar tu biblioteca a la web

En la aplicación nativa 0.13.0, guarda una copia desde **Tu biblioteca → Llevar mi biblioteca a la web**. Si vienes de otra instalación web, usa **Tu biblioteca → Copia de seguridad**. Abre Pletina desde el icono nuevo de Tuqo e importa el archivo en **Tu biblioteca → Copia de seguridad**.

La copia incluye favoritos, listas, historial y progreso de pódcasts. El audio descargado queda en la instalación anterior. Puedes volver a descargar en la web el audio disponible. [Notas de Pletina 0.13.0](https://github.com/diad87/pletina-releases/releases/tag/v0.13.0).

## Capturas de la versión web

![Inicio de Pletina en escritorio con discos y artistas para descubrir](screenshots/web-escritorio-inicio.png)

La interfaz móvil se muestra en una vista emulada de iPhone.

| Álbum | Sonando ahora | Pódcast |
| :---: | :---: | :---: |
| ![Ficha de un álbum con su lista de canciones en la vista de iPhone](screenshots/web-iphone-disco.png) | ![Reproductor en la vista de iPhone con saltos de 15 segundos](screenshots/web-iphone-sonando.png) | ![Ficha de un pódcast y sus episodios en la vista de iPhone](screenshots/web-iphone-podcast.png) |

## Instalar

Descarga el archivo de tu sistema desde la [última versión nativa](https://github.com/diad87/pletina-releases/releases/latest). La APK permite usar Android Auto y acceder al audio que ya descargaste en Android.

| Sistema | Archivo |
|---|---|
| Windows 10/11 | `Pletina_x.y.z_x64-setup.exe`: doble clic |
| Mac (chip de Apple o Intel, macOS 11+) | `Pletina_x.y.z_universal.dmg`: arrastrar a Aplicaciones |
| Linux (64 bits) | `Pletina_x.y.z_amd64.AppImage` (distribuciones recientes) o `.deb` (Ubuntu/Debian) |
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

## Comprobar que una descarga es auténtica

Desde la 0.8.0, cada archivo lleva un certificado de procedencia de GitHub: demuestra que sale del código de [diad87/pletina](https://github.com/diad87/pletina) y de su compilación en GitHub Actions, sin pasar por el ordenador de nadie. Con la [CLI de GitHub](https://cli.github.com):

```bash
gh attestation verify Pletina_0.9.0_x64-setup.exe --repo diad87/pletina
```

Cada versión trae además `SHA256SUMS.txt` con la huella de cada archivo: `sha256sum -c SHA256SUMS.txt` en Linux o Mac, o `Get-FileHash` en Windows y compararla con la de la lista.

## Privacidad

Pletina funciona sin cuenta. La versión web guarda la biblioteca en el navegador. En la aplicación nativa, la biblioteca se guarda en el dispositivo y la app funciona sin analíticas. [Privacidad y servicios que consulta Pletina](https://github.com/diad87/pletina#privacidad).
