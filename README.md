Tarea AppMoviles_-Consulta 1 : Tarea Individual - Aplicaciones Web - Jose Pila
# Iconos personalizados
En Ionic Angular, los iconos personalizados son gráficos creados o modificados por ti mismo (por ejemplo en formato SVG o PNG) que reemplazan o complementan los iconos estándar del framework (los Ionicons) para adaptarse al diseño, estilo o marca de tu aplicación.

Por defecto, Ionic usa la librería Ionicons, una colección muy completa de iconos nativos en formato SVG. Sin embargo, puede que quieras usar tus propios íconos.
## Formas de crear un icono personalizado 
Para crear el icono es necesario realizar las siguientes pasos:
1. Instalar el plugin para el manejo de **assets**:
<pre> npm install @capacitor/assets --save-dev</pre>
2. Luego generamos los archivos iconos con los cuales queremos realizar la generación de iconos:
   
   <img width="299" height="73" alt="image" src="https://github.com/user-attachments/assets/2a00b383-205e-4772-b070-b1f5ab0fc7a3" />
3. Luego ejecutamos la instancia para la ejecucion en Android Studio
<pre>npx capacitor-assets generate</pre>
# ¿Qué es el Splash Screen?
El Splash Screen es una pantalla inicial la cual se ejecuta cuando se abre la aplicación móvil por primera vez y se da antes de que cargue la interfaz principal (por ejemplo app.component o tabs/home).
## Procedimiento para implementar
1. Primero instalamos la instancia de splash screen:
<pre>npm install @capacitor/splash-screen</pre>
2. Luego añadimos en el archivo ***capacitor.config.ts***
<pre> 
plugins: {
     "SplashScreen": {
          "launchShowDuration": 3000,
           "launchAutoHide": true,
           "launchFadeOutDuration": 3000,
           "backgroundColor": "#ffffffff",
           "androidSplashResourceName": "splash",
           "androidScaleType": "CENTER_CROP",
           "showSpinner": true,
           "androidSpinnerStyle": "large",
           "iosSpinnerStyle": "small",
           "spinnerColor": "#999999",
           "splashFullScreen": true,
           "splashImmersive": true,
           "layoutName": "launch_screen",
           "useDialog": true
          }
     } 
</pre>
3. Importamos la instancia en el ***\*.component.ts***
<pre>import { SplashScreen } from '@capacitor/splash-screen';</pre>
4. Luego generamos la instancia para la ejecución el Splash Screen ***(esta instancia se ejecutara al abrir la aplicación)***


<img width="285" height="223" alt="image" src="https://github.com/user-attachments/assets/35504ef3-a959-4034-b834-69b2c71229e0" />


5. Creamos la configuración  de las dependencias para su ejecución en los dispositivos móviles (Android/IOS)
<pre> npm install @capacitor/android </pre>
o bien,
<pre> npm install @capacitor/ios </pre>
6. Luego construimos el paquete de ejecución
<pre>ionic build</pre>
7.
# Archivo AndroidManifest.xml
El archivo AndroidManifest.xml es un archivo esencial en todas las aplicaciones Android, incluso las creadas con Ionic Angular.

Su función principal es declarar la estructura, permisos y configuración básica de tu aplicación Android para que el sistema operativo sepa cómo debe ejecutarla.

Sin este archivo, Android no sabría qué actividades (pantallas) abrir, qué permisos necesitas ni cómo mostrar tu app al usuario.


<img width="799" height="673" alt="image" src="https://github.com/user-attachments/assets/1cdabaef-3105-4f25-a2ca-587b285ada06" />



