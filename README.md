# DSM - Tarea 7: Android Basics with Compose (Unidad 5)

Repositorio correspondiente al desarrollo de las actividades, proyectos prácticos y sustentaciones de la **Unidad 5: Cómo conectarse a Internet**, del curso de **Desarrollo de Sistemas Móviles** en la Universidad Nacional Mayor de San Marcos (UNMSM).

---

##  Estructura del Repositorio

- `ruta1-kotlin/`: Ruta 1 - Consumo de servicios REST con Retrofit y Corrutinas (`Mars Photos`).
- `ruta2-kotlin/`: Ruta 2 - Capa de datos, Inyección de Dependencias manual y Coil (`Amphibians`).
- `README.md`: Documentación técnica de la entrega.

---

##  Contenido de las Rutas

###  Ruta 1: Cómo obtener datos de Internet (`Mars Photos`)
- **Descripción:** Conexión asíncrona a un servicio web REST para la recuperación y deserialización de datos estructurados.
- **Conceptos clave aplicados:**
  - `Retrofit 2`: Configuración del cliente HTTP y definición de endpoints REST (`@GET`).
  - `Kotlinx Serialization`: Mapeo de cadenas JSON a objetos nativos de Kotlin (`@Serializable`, `@SerialName`).
  - Corrutinas y concurrencia estructurada: Invocación no bloqueante dentro de `viewModelScope.launch`.
  - Interfaz sellada (`MarsUiState`): Manejo predecible de los estados de la interfaz (`Loading`, `Success`, `Error`).

###  Ruta 2: Carga y muestra de imágenes de Internet (`Amphibians`)
- **Descripción:** Implementación de arquitectura moderna recomendada por Android para la separación de capas, inyección de dependencias y visualización de recursos multimedia remotos.
- **Conceptos clave aplicados:**
  - **Patrón Repositorio:** Abstracción del origen de datos mediante `AmphibiansRepository` y su implementación de red.
  - **Inyección Manual de Dependencias (DI):** Creación de un contenedor global (`AppContainer` / `DefaultAppContainer`) inicializado a nivel de la clase personalizada `Application`.
  - `ViewModelProvider.Factory`: Suministro desacoplado del repositorio al ciclo de vida del ViewModel.
  - **Biblioteca Coil:** Uso del composable `AsyncImage` para descarga asíncrona, caché en memoria/disco y transiciones suaves (`crossfade`).

---

##  Tecnologías y Entorno

- **Lenguaje:** Kotlin
- **Framework UI:** Jetpack Compose (Material 3)
- **Networking:** Retrofit 2 & OkHttp 3
- **Serialización:** Kotlinx Serialization JSON
- **Carga de Imágenes:** Coil Compose
- **IDE:** Android Studio
- **Target SDK:** Android 14+ (API 34 / 35)
