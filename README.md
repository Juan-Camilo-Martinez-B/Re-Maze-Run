
# Re-Maze-Run

Re-Maze-Run es un videojuego de acción y supervivencia en tercera persona desarrollado en Unity. El jugador asume el papel de un sobreviviente que debe avanzar a través de distintos escenarios (Laberinto, Industry y Boss), enfrentando hordas de enemigos y jefes, destruyendo objetivos y superando desafíos para completar cada nivel en el menor tiempo posible. El juego combina exploración y combate, si el jugador muere, debrá completar el juego desde el incio otra vez, tiene un sistema de puntuación basado en el tiempo y el desempeño. El juego es de modo run, es decir, todo el juego debe desarrollarse sin morir para terminar la run debido a que no tiene checkpoints, la puntuación se dará segun el tiempo total del jugador, de C - S+ siendo C la menor puntuación y S+ la mayor (similar a las partidas de resident evil).

## ¿Cómo funciona el flujo del juego?

El flujo y la lógica principal del juego están gestionados por el script `LevelManager.cs`, que se encarga de:

- Controlar el inicio, pausa y reanudación del juego.
- Gestionar los objetivos de cada nivel (por ejemplo, destruir todos los barriles en el Laberinto, sobrevivir a hordas en Industry, derrotar al jefe final en Boss).
- Llevar el control del tiempo de cada nivel y del tiempo total de la partida.
- Mostrar los paneles de victoria o derrota según el desempeño del jugador.
- Actualizar la interfaz de usuario con información relevante (cronómetro, objetivos, progreso de hordas, etc.).
- Permitir la transición entre niveles y reinicio del juego.

El `LevelManager` detecta cuándo se cumplen los objetivos de cada nivel y detiene el tiempo, mostrando un panel de resultados con estadísticas y rango obtenido. Si el jugador es derrotado, muestra un panel de derrota con la opción de reiniciar o salir. Además, el script permite simular progresión para pruebas y ajusta el flujo según el nivel actual.

## Estructura del Proyecto

- **Assets/**: Carpeta principal de recursos del juego.
  - **Anims/**: Animaciones de personajes y enemigos (Demon, Leon, Tank, Zombie).
  - **Audio/**: Efectos de sonido organizados por tipo y personaje (Armas, Demon, Tank, Zombie).
  - **Effects/**: Prefabs y efectos visuales (explosiones, impactos, etc.).
  - **Images/**: Imágenes y fondos utilizados en el juego.
  - **ImportedAssets/**: Recursos importados de terceros (modelos, texturas, efectos, utilidades).
  - **Materials/**: Materiales utilizados para los modelos 3D.
  - **Models/**: Modelos 3D de personajes y armas.
  - **Prefabs/**: Prefabricados de Unity listos para usar en escenas (personajes, armas, objetos interactivos).
  - **Resources/**: Recursos adicionales como iconos y sprites.
  - **Scenes/**: Escenarios jugables del juego (Boss, Industry, Laberinto).
  - **Scripts/**: Lógica del juego, controladores de personajes, enemigos, armas, HUD, etc.

- **Library/**, **Logs/**, **Packages/**, **ProjectSettings/**, **Temp/**, **UserSettings/**: Carpetas generadas automáticamente por Unity para la gestión del proyecto y no deben ser modificadas manualmente.

## Scripts Principales

- `PlayerController.cs`: Controla el movimiento y acciones del jugador.
- `WeaponController.cs`, `WeaponSlots.cs`: Gestión de armas y slots.
- `BossController.cs`, `DemonController.cs`, `ZombieController.cs`, `TankController.cs`: Controladores de enemigos principales.
- `HealthBar.cs`, `BossHealthBar.cs`, `DemonHealthBar.cs`, `ZombieHealthBar.cs`: Gestión de barras de vida.
- `LevelManager.cs`, `HordeManager.cs`, `MonsterSpawner.cs`, `ZombieSpawner.cs`: Lógica de niveles y generación de enemigos.

## Instalación y Ejecución

### Windows
- El juego puede descargarse y ejecutarse a través de un instalador específico para Windows. Simplemente ejecute el archivo instalador y siga las instrucciones en pantalla.

### Mac
- Para Mac, descargue la carpeta comprimida (zip enviada por el autor), descomprímala y ejecute el archivo del juego desde la carpeta resultante.

## Créditos y Recursos de Terceros
- El proyecto utiliza recursos de terceros incluidos en la carpeta `ImportedAssets/` (modelos, texturas, efectos, etc.). Consulte los archivos `readme.txt` y documentación dentro de cada subcarpeta para más detalles y licencias.

## Notas
- Este proyecto está optimizado para ejecutarse en Windows. La compatibilidad con Mac puede requerir configuraciones adicionales.
- Para dudas o soporte, consulte la documentación incluida en los assets o contacte al desarrollador.
