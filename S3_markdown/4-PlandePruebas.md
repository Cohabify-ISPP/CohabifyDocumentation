![US Logo](images/logo_us.png)

Plan de Pruebas
---


![Cohabify](images/Cohabify.png)

<table>
    <tbody>
        <tr>
            <td rowspan=2>Robles Russo, Eduardo (editor)<p></p>
            </td>
        </tr>
    </tbody>
</table>

<table>
  <tr>
    <th>Grupo</th>
    <th>4</th>
    <th>Entregable</th>
    <th>S3</th>
  </tr>
  <tr>
    <td>Repositorio</td>
    <td colspan="3"><a href="https://github.com/Cohabify/Cohabify">https://github.com/Cohabify/Cohabify</a></td>
  </tr>
  <tr>
    <td>Base de conocimiento común</td>
    <td colspan="3"><a href="https://bgcc.vercel.app/">https://bgcc.vercel.app/</a></td>
  </tr>
</table>

###  Versión Cambios Autores
| Versión | Cambios | Autores |
| --- | --- | --- |
| V1.0 | Creación del documento | Eduardo Robles Russo |

### Tabla de Contenidos

- [Plan de Pruebas](#plan-de-pruebas)
  - [Versión Cambios Autores](#versión-cambios-autores)
  - [Tabla de Contenidos](#tabla-de-contenidos)
  - [1. Alcance:](#1-alcance)
  - [2. Estrategia de Pruebas:](#2-estrategia-de-pruebas)
  - [3. Recursos necesarios:](#3-recursos-necesarios)
  - [4. Casos de Prueba:](#4-casos-de-prueba)
  - [5. Criterios de Aceptación:](#5-criterios-de-aceptación)


**Plan de Pruebas**

### 1. Alcance:
   - Se probarán las funcionalidades descritas en los apuntes, incluyendo pruebas unitarias, de integración, de extremo a extremo, de aceptación y de rendimiento.
   - No se probarán aspectos fuera del alcance de la asignatura, como pruebas de seguridad avanzadas o pruebas de carga extremadamente pesadas.

### 2. Estrategia de Pruebas:

Para garantizar la calidad y robustez del software, seguiremos esta estrategia:

- **Pruebas de Camino Feliz y Pruebas Negativas:**
   - Realizaremos pruebas de camino feliz para validar el flujo principal de la aplicación.
   - También ejecutaremos pruebas negativas para verificar cómo el sistema maneja situaciones inesperadas o errores.

-  **Pruebas Manuales y Automáticas:**
   - Utilizaremos una combinación de pruebas manuales y automáticas:
       - **Pruebas Manuales**:
           - Realizaremos exploración manual para descubrir posibles problemas no cubiertos por casos de prueba específicos.
           - Validaremos la interfaz de usuario, flujos de trabajo y escenarios de uso.
       - **Pruebas Automáticas**:
           - Implementaremos pruebas automatizadas para casos repetitivos y regresiones.
           - Utilizaremos herramientas como Selenium, JUnit o PyTest para automatizar pruebas de UI y lógica de negocio.

-  **Casos de Prueba Específicos:**
   - Definiremos casos de prueba específicos para cada tipo de test:
       - **Pruebas Unitarias**:
           - Verificaremos funciones individuales y componentes a nivel de código.
           - Validaremos entradas válidas e inválidas.
       - **Pruebas de Integración**:
           - Probaremos la comunicación entre módulos y servicios.
           - Verificaremos la integración con bases de datos y APIs externas.
       - **Pruebas de Aceptación**:
           - Validaremos que el sistema cumpla con los requisitos del cliente.
           - Probaremos la usabilidad y la experiencia del usuario.
       - **Pruebas de Rendimiento**:
           - Estableceremos umbrales de rendimiento aceptables (tiempos de respuesta, capacidad de carga).
           - Ejecutaremos pruebas de carga y estrés para evaluar el rendimiento bajo diferentes condiciones.

### 3. Recursos necesarios:
   - Equipo de desarrollo: ingenieros de software responsables de implementar las pruebas.
   - Herramientas de prueba: Katalon Recorder, Selenium, JUnit 5, Gatling, entre otras.
   - Ambientes de prueba: entornos de desarrollo, preproducción y producción para pruebas de rendimiento.

### 4. Casos de Prueba:
Los casos de prueba son escenarios específicos diseñados para verificar el correcto funcionamiento de un software. Aquí estan las diferentes tipos de pruebas y los escenarios que se presentan en nuestra aplicacion.

- **Pruebas Unitarias**
  - **Objetivo**: Verificar que las funciones individuales del código produzcan resultados esperados.
  - **Escenarios**:
      - Validar que el link "¿No tienes cuenta?, regístrate." esté presente en la pantalla de inicio de sesión.
      - Verificar que los seis campos de registro tengan su propia validación.
      - Comprobar que los campos se muestren en rojo cuando la entrada no es válida.
      - Confirmar que, una vez rellenados correctamente los seis campos, marcado el aceptar términos y condiciones y pulsado en siguiente, se mueva a una segunda pantalla de registro.

- **Pruebas de Integración**
  - **Objetivo**: Probar la conexión entre los diferentes módulos del sistema y verificar la comunicación correcta con bases de datos externas y servicios web.
  - **Escenarios**:
      - Validar que al pulsar en el link "¿No tienes cuenta?, regístrate." se muestre la pantalla de registro.
      - Comprobar que en la segunda pantalla de registro se pueda seleccionar el género, los tags de interés y una foto de perfil.
      - Verificar que se pueda volver a la pantalla anterior.
      - Confirmar que se pueda completar el registro.

- **Pruebas de Extremo a Extremo**
  - **Objetivo**: Simular el flujo completo de usuario desde la interfaz hasta la base de datos. Validar la funcionalidad del sistema en diferentes navegadores y dispositivos.
  - **Escenarios**:
      - Iniciar sesión con un usuario registrado en el sistema.
      - Verificar que aparezca una pequeña ventana indicando el éxito de la operación al iniciar sesión correctamente.
      - Iniciar sesión mediante Google.
      - Validar que al seleccionar el inicio de sesión con la cuenta deseada, se mueva al usuario a una pantalla de registro modificada.
      - Comprobar que en la pantalla de registro modificada se requieran los campos no aportados por Google o que podrían interesar al usuario cambiar.
      - Confirmar que el campo de correo esté deshabilitado y se muestre para que el usuario sepa con qué correo se está haciendo el proceso.

- **Pruebas de Aceptación**
  - **Objetivo**: Verificar que el sistema cumpla con los requisitos del cliente descritos en los escenarios de aceptación. Probar la usabilidad y la experiencia del usuario en situaciones normales y de excepción.
  - **Escenarios**:
      - Ver el perfil del usuario y editarlo.
      - Publicar anuncios y verificar que sean visibles para otros usuarios.
      - Buscar anuncios de vivienda y aplicar filtros a la búsqueda.
      - Dejar comentarios en los anuncios de vivienda y confirmar que sean visibles para otros usuarios.
      - Ver un listado de anuncios de compañeros de piso y aplicar filtros a la búsqueda.
      - Dejar comentarios y dar “me gusta” en los perfiles de otros usuarios, y que estas interacciones sean visibles para otros usuarios.

- **Pruebas de Rendimiento**
  - **Objetivo**: Realizar pruebas de carga para determinar el comportamiento del sistema bajo diferentes niveles de carga. Ejecutar pruebas de estrés para identificar el punto de quiebre del sistema y su capacidad de recuperación.
  - **Escenarios**:
      - Evaluar la eficiencia del proceso de registro y edición de perfil.
      - Medir la rapidez en la publicación y visualización de anuncios.
      - Comprobar la agilidad en las búsquedas y filtrados de anuncios.
      - Validar que las interacciones en los perfiles de usuarios no afecten negativamente al rendimiento general de la plataforma.
  - **Umbrales de rendimiento**: Este tiene que cumplir con unos umbrales capacidad de manejo de carga y tiempo de respuesta maximo:

    - **Capacidad de manejo de carga:** Necesitaremos dos instancias en nuestro proyecto (backend y frontend). Teniendo en cuenta que cada instancia de Google App Engine puede manejar hasta 80 solicitudes concurrentes. Esto significa que, en un momento dado, una sola instancia puede procesar hasta 80 solicitudes de usuarios al mismo tiempo. Con el plan F1 se crean automaticamente mas instancias pero esto hace que aumente el precio. Por tanto concluimos que como maximo podemos tener unos 80 usuarios concurrentes usando la web.

    - **Tiempo de Carga de la Página Inicial**:
        - **Objetivo**: La página de inicio debe cargarse rápidamente para proporcionar una buena primera impresión.
        - **Umbral Aceptable**: Menos de **2 segundos** para cargar completamente la página principal.
    - **Tiempo de Carga de la Página Inicial**:
        - **Objetivo**: La página de inicio debe cargarse rápidamente para proporcionar una buena primera impresión.
        - **Umbral Aceptable**: Menos de **2 segundos** para cargar completamente la página principal.
    - **Tiempo de Respuesta de Búsquedas y Filtros**:
      - **Objetivo**: Las búsquedas y aplicaciones de filtros deben ser ágiles para mantener la experiencia del usuario.
      - **Umbral Aceptable**: Menos de **1 segundo** para mostrar resultados después de aplicar un filtro o realizar una búsqueda.

    - **Tiempo de Carga de Perfiles de Usuario y Anuncios**:
      - **Objetivo**: Los perfiles de usuario y los anuncios deben cargarse rápidamente para que los usuarios puedan acceder a la información relevante.
      - **Umbral Aceptable**: Menos de **1 segundo** para cargar un perfil de usuario o un anuncio.

    - **Tiempo de Carga de Imágenes y Contenido Multimedia**:
      - **Objetivo**: Las imágenes y otros elementos multimedia deben cargarse sin demoras significativas.
      - **Umbral Aceptable**: Menos de **2 segundos** para cargar imágenes y contenido multimedia en una página.

    - **Tiempo de Inicio de Sesión y Autenticación**:
      - **Objetivo**: El proceso de inicio de sesión debe ser rápido y eficiente.
      - **Umbral Aceptable**: Menos de **3 segundos** para completar el inicio de sesión.

    - **Tiempo de Publicación de Anuncios y Comentarios**:
      - **Objetivo**: Los usuarios deben poder publicar anuncios y dejar comentarios sin retrasos notables.
      - **Umbral Aceptable**: Menos de **2 segundos** para completar la publicación o el comentario.

### 5. Criterios de Aceptación:
   - Las pruebas se considerarán exitosas si todas las funcionalidades probadas cumplen con los criterios de aceptación definidos. Estos criterios ayudarán a garantizar que la aplicación cumpla con los estándares de calidad y satisfaga las necesidades de los usuarios:
        - **Registro de Usuario:**
           - El usuario debe poder registrarse con éxito proporcionando información válida.
           - Los campos obligatorios (como nombre, correo electrónico y contraseña) deben validarse correctamente.
           - Después del registro, el usuario debe recibir una confirmación o notificación de éxito.    
        - **Inicio de Sesión:**
          - El usuario debe poder iniciar sesión con sus credenciales correctamente.
          - Las credenciales incorrectas deben generar un mensaje de error adecuado.
          - La sesión debe mantenerse activa mientras el usuario navega por la aplicación.
        - **Perfil de Usuario:**
          - El usuario debe poder ver y editar su perfil.
          - Los cambios en el perfil (como la foto de perfil o la información personal) deben reflejarse correctamente.
        - **Publicación de Anuncios:**
          - Los usuarios deben poder crear y publicar anuncios.
          - Los anuncios deben mostrarse correctamente en la plataforma.

        - **Búsqueda y Filtros:**
          - Los usuarios deben poder buscar anuncios de vivienda y aplicar filtros (por ubicación, precio, etc.).
          - Los resultados de búsqueda deben ser precisos y actualizarse en tiempo real.
        - **Comentarios y Valoraciones:**
          - Los usuarios deben poder dejar comentarios en los anuncios.
          - Las valoraciones y comentarios deben mostrarse correctamente en los perfiles y anuncios.
        - **Rendimiento y Escalabilidad:**
          - La aplicación debe manejar una carga razonable de usuarios simultáneos sin degradar el rendimiento.
          - Las consultas a la base de datos y las operaciones deben ser eficientes.
        - **Compatibilidad y Pruebas Cruzadas:**
          - La aplicación debe funcionar correctamente en diferentes navegadores y dispositivos (móviles, tabletas, etc.).
          - Se deben realizar pruebas en diferentes escenarios (navegación, búsqueda, publicación, etc.).
        - **Seguridad:**
          - Las contraseñas deben almacenarse de forma segura (hashing y salting).
          - La aplicación debe protegerse contra ataques comunes (inyección SQL, XSS, CSRF, etc.).
        - **Experiencia del Usuario:**
          - La interfaz de usuario debe ser intuitiva y fácil de usar.
          - Los mensajes de error y las notificaciones deben ser claros y útiles.

**6. Conclusiones de los Resultados:**
   - Se documentarán los resultados de las pruebas, incluyendo cualquier error encontrado y las acciones correctivas tomadas.
   - Se realizará un análisis de los resultados para identificar áreas de mejora y posibles problemas pendientes.

**7. Aprobaciones:**
   - Se solicitarán las firmas de los GM para validar el plan de pruebas y los resultados obtenidos. Estas son sus firmas:

<tr>
    <td><img src="images/Aspose.Words.cb4b4684-16f7-4731-86da-bd03434bf4af.001.png"></td>
    <td><img src="images/Aspose.Words.cb4b4684-16f7-4731-86da-bd03434bf4af.002.png"></td>
    <td><img src="images/Aspose.Words.cb4b4684-16f7-4731-86da-bd03434bf4af.003.png"></td>
    <td><img src="images/Aspose.Words.cb4b4684-16f7-4731-86da-bd03434bf4af.004.jpeg"></td>
</tr>
