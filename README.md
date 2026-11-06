# Tutorial-Guali-Android Frontend

## Prerrequisitos y Software 

Para desarrollar el proyecto se necesita:
- Sistema Operativo: Windows 10 u 11, macOS o Linux
- Android Studio: IDE oficial para el desarrollo en Android
- Java JDK: Android Studio lo instala automáticamente 
- Conexión a Internet

### Instalación

1. Ir a la página oficial (https://developer.android.com/studio) y descargar el instalador correspondiente al sistema operativo de la computadora
![Descarga](img/1.Web.png)

2. Ejecutar el instalador. En la ventana de configuración, seleccionar la ruta donde se instalará Android Studio y los componentes de SDK
![Instalador](img/2.instalador.png)

3. Elegir la carpeta donde se crearán los accesos directos y continuar la instalación
![Carpeta Inicio](img/3.instalador.png)

## Creación del Proyecto

1. Al abrir Android Studio, hacer clic en "New Project" en la pantalla de bienvenida
![Bienvenida](img/4.incioAS.png)  

2. Seleccionar la plantilla que prefiramos y hacer clic en "Next"
![Plantilla](img/5.Plantilla.png)

3. Configurar los datos del proyecto:
- Name: `GualiAndroid`
- Package name: `com.guali.tutor.gualiandroid`
- Lenguaje: `Java`
- Minimum SDK: `API 24`

Hacer clic en "Finish".
![Configuración Proyecto](img/6.plantilla.png)

4. Esperar a que Gradle termine de sincronizar e importar el proyecto
![Gradle Sync](img/7.sincronizar.png)

## Creación de la Interfaz

1. Hacer clic derecho sobre la carpeta `res` > New > Android Resource Directory. Seleccionar `layout` y crear la carpeta
![Crear Carpeta Layout](img/8.crearlayout.png)

2. Dentro de la carpeta `layout` hacer clic derecho > New > Layout Resource File y nombrarlo `activity_main.xml`
![Crear activity_main](img/9.Crearmain.png)

3. Abrir el archivo `activity_main.xml`. Se creará por defecto con un `ConstraintLayout`.Se puede cambiar la vista entre **Code**, **Split** o **Design**
![Vista Layout](img/10.vistamain.png)

4. Reemplazar el código por un `LinearLayout` vertical para estructurar nuestra interfaz principal (título, editor y consola)
![Layout Vacio](img/13.creardiseñomain.png)

## Agregar Iconos y Botones

1. Para los botones inferiores, se usaron iconos vectoriales. Para agregarlos hacer clic derecho sobre `res/drawable` > New > Vector Asset
![Nuevo Vector](img/11.agregarlogotipos.png)

2. Hacer clic en "Clip Art", buscar iconos (como listas, libro, herramientas o play), seleccionarlos y hacer clic en "Next" y luego en "Finish"
![Seleccionar Icono](img/12.elegirsimbolo.png)

3. En el archivo `activity_main.xml`, agregar la barra de botones usando "MaterialButton" para asignarle los iconos y textos (Menú, Lección, Compilar, Ejecutar)
![Botones Layout](img/13.creardiseñomain.png)

## Creación del Menú

1. Hacer clic derecho sobre `res` > New > Android Resource Directory, seleccionar `menu` y crear la carpeta
2. Dentro de la carpeta `menu` hacer clic derecho > New > Menu Resource File y nombrarlo `principal.xml`
3. Agregar los items para el menú: Lecciones, Configuración, Historial y Ayuda
![Menu XML](img/14.crearopcionemenu.png)

## Personalización del Tema

1. Abrir el archivo `res/values/themes.xml`
2. Cambiar el `parent` del tema a `Theme.MaterialComponents.DayNight.NoActionBar` para quitar la barra morada superior
![Temas XML](img/15.cambiartema.png)

## Lógica de la Pantalla Principal (Java)

1. En la carpeta `java` > `com.guali.tutor.gualiandroid`, abrir la clase `PantallaPrincipal.java`
2. Agregar la lógica para enlazar los botones con los paneles emergentes (`AlertDialog`) que sirven para las opciones de Lecciones, Configuración, Historial y Ayuda
![Código Java](img/16.pantallaprincipal.png)

## Registro en el AndroidManifest

1. Abrir el archivo `app/src/main/AndroidManifest.xml`
2. Verificar que la actividad `PantallaPrincipal` esté registrada como pantalla de inicio con su respectivo `intent-filter`
![Manifest](img/17.agregarpantallaprincipal.png)

## Ejecución y Prueba

1. Hacer clic en el botón "Run" (triángulo verde) y seleccionar el emulador. Esperar a que compile exitosamente
![App Corriendo](img/18.runapp.png)

2. Presionar el botón "Menú" en la parte inferior para desplegar las opciones
![Menú Desplegado](img/19.menu.png)

3. Probar cada uno de los paneles:
- **Lecciones:** Abre el panel para abrir o cerrar una lección
![Panel Lecciones](img/20.lecciones.png)

- **Buscar Lección:** Muestra el campo de texto para ingresar la ruta de una lección
![Buscar Lección](img/21.lecciones.png)

- **Configuración:** Permite ingresar la ruta del JDK
![Configuración](img/22.configuracion.png)

- **Historial:** Muestra la tabla con el registro de sesiones
![Historial](img/23.historial.png)

- **Ayuda:** Muestra el texto con las instrucciones de uso

![Ayuda](img/24.ayuda.png)

- **Panel de Lección Activa:** Muestra el estado actual cuando no hay lecciones cargadas
![Lección Activa](img/25.leccionactiva.png)
