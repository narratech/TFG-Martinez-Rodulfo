# TFG - Generación Procedimental de Mazmorras con Dungeon Architect

Este repositorio contiene el Trabajo de Fin de Grado (TFG) titulado **"Generación procedimental de escenarios para videojuegos estructurados en anillos concéntricos"**, desarrollado en la **Facultad de Informática de la Universidad Complutense de Madrid (UCM)**.

## Autores
- **Pablo Martínez Quesada**
- **Alfonso Jaime Rodulfo Guío**

## Tutor
**Federico Peinado** (Narratech Laboratories, UCM)

## Descripción
Este proyecto explora el uso de técnicas de generación procedimental de escenarios en videojuegos, centrándose en la herramienta **Dungeon Architect** para la creación de mazmorras.

## Tecnologías Utilizadas
- **Unreal Engine** (versión recomendada: 5.4.4)
- **Dungeon Architect** (versión: 2.34.0_UE_5.4)
- **Blueprints**

## Contenido del Repositorio 
- **BP_ConcentricRingsBuilder.uasset** Builder personalizado
- **T_RoomColorChange.uasset** Tema cambio de color para debug
- **BP_RoomColorChange.uasset** Bluprint cambio de color para debug
- **ST_ArrayOfArray.uasset** Estructura auxiliar para organizar habitaciones
- **README.md**: Este documento

## Instalación y Uso

### 🛠 Requisitos Previos

Tener **Dungeon Architect** instalado es un requisito obligatorio para el correcto funcionamiento de esta herramienta.  
Puedes adquirir Dungeon Architect en el Unreal Marketplace desde el siguiente enlace:  
[https://www.unrealengine.com/marketplace/en-US/product/dungeon-architect](https://www.unrealengine.com/marketplace/en-US/product/dungeon-architect)


#### 🔧 Instalación Manual de Dungeon Architect (si no lo tienes instalado)

Si has adquirido **Dungeon Architect** desde Code Respawn, puedes instalarlo manualmente siguiendo estos pasos:

1. En el directorio raíz de tu juego, crea una carpeta llamada `Plugins` (si no existe).
2. Copia la carpeta `DungeonArchitect` que se encuentra en el archivo descargado, bajo `Plugin/4.X/`, dentro de la carpeta `Plugins` de tu juego.
   
  Por ejemplo, en el proyecto de ejemplo `ShooterGame`, la estructura quedaría así:

    ShooterGame/
    └── Plugins/
    └── DungeonArchitect/

3. Reinicia el **Unreal Editor** (si ya lo tenías abierto) y verifica que el plugin **Dungeon Architect** esté habilitado desde el gestor de plugins.


### 📦 Paso 1: Instalar el Concentric Rings Builder

Copia la carpeta ConcentricRingsBuilder que cuenta con los siguientes archivos:
    BP_ConcentricRingsBuilder.uasset
    BP_RoomColorChange.uasset
    T_RoomColorChange.uasset
    Structures
      ST_ArrayOfArray.uasset

    \end{itemize}

En la siguiente ruta de tu proyecto:

[RUTA_DEL_PROYECTO]\Plugins\DungeonArchitect\Content\Samples\DA_CustomBuilder\Blueprints

### 🧱 Paso 2: Configurar el Actor de la Mazmorra

1. Crea un nuevo **nivel** en tu proyecto.  
2. Añade un actor de **Dungeon** al nivel.  
3. En las propiedades del actor de mazmorra:  
   - Establece la clase del constructor como:  
     BP_ConcentricRingsBuilder  
   - Haz clic en el ícono **+** junto al array `Themes` para añadir una nueva entrada.  
   - Asigna el tema con nombre:  
     BP_RoomColorChange  

**⚠️ Importante**: Activa las opciones `Show Engine Content` y `Show Plugin Content` en el explorador de contenido.

### ▶️ Paso 3: Ejecutar el Constructor

Ejecuta el constructor desde el actor de Dungeon y genera diferentes mazmorras. Elige el diseño que mejor se adapte a tu juego.

### ✅ ¡Todo Listo!

Tu constructor personalizado de mazmorras está listo para utilizarse en tu proyecto.

## Contacto

Para cualquier consulta o colaboración, puedes contactar a través de:

### Pablo Martínez Quesada
- 📧 Email: pambar31@ucm.es  
- 💻 GitHub: [@Ares75643](https://github.com/Ares75643)

### Alfonso Jaime Rodulfo Guío
- 📧 Email: arodulfo@ucm.es  
- 💻 GitHub: [@ARodulfo](https://github.com/ARodulfo)
