# 🏒 Xestor de Torneos Escolares - CEIP Balaídos

Benvido/a ao repositorio do Xestor de Torneos Escolares, unha ferramenta web creada para organizar o Torneo de Nadal de hóckey do CEIP Balaídos (e adaptable a outros torneos).

Esta aplicación está contida nun único ficheiro HTML que inclúe toda a lóxica (JavaScript) e os estilos (CSS) necesarios para funcionar.

## 🚀 Como Usar a Ferramenta

A ferramenta ten dous modos de uso principais, que se controlan a través da URL.

### 1. Modo Xestión (para profesores/administradores)

É o modo por defecto que permite editar todos os aspectos do torneo.

- **Acceso:** Abre o ficheiro `torneo_hockey_maestro.html` directamente no navegador ou accede ao enlace principal publicado en GitHub Pages.
- **Funcionalidades:**
    - Engadir, eliminar e gardar equipos e os seus escudos (mediante URL).
    - Xerar calendarios de partidos a dobre volta por xornadas.
    - Introducir resultados dos partidos.
    - Xerar as fases finais (eliminatorias) automaticamente.
    - Exportar e importar todos os datos do torneo en formato JSON.
    - Activar un "Modo Proxector" para unha mellor visualización en pizarras dixitais.

### 2. Modo Consulta (para alumnos/visitantes)

Un modo de só lectura ideal para compartir os resultados.

- **Acceso:** Engade `?modo=ver` ao final da URL.
  - Exemplo: `https://o-teu-usuario.github.io/o-teu-repositorio/torneo_hockey_maestro.html?modo=ver`
- **Funcionalidades:**
    - Ver todos os equipos, xornadas, resultados e clasificacións.
    - Os controis de edición están ocultos e desactivados.
    - Permite usar os filtros para visualizar por ciclo ou por curso.
    - Permite activar o "Modo Proxector".

    
## 🔄 Flujo de Trabajo: Actualización de Resultados

Este proyecto utiliza un sistema de **datos externos** para separar la gestión del torneo de la visualización pública. De esta forma, los alumnos pueden consultar los resultados sin riesgo de modificar la base de datos.

### 1. Gestión del Torneo (Rol del Profesor)
Para introducir resultados, crear jornadas o modificar equipos:
1. Abre el archivo `index.html` en tu ordenador (o accede a tu versión de gestión privada).
2. Realiza los cambios necesarios (goles, actas, fair play, etc.).
3. Ve a la sección **⚙️ Xestión de datos**.
4. Haz clic en el botón **"⬇️ Descargar JSON"**.
5. Se descargará un archivo (ej: `torneo_balaidos_2025.json`).
6. **IMPORTANTE:** Renombra ese archivo a **`datos.json`** (todo en minúsculas).

### 2. Publicación de Datos (Subida a GitHub)
Para que los alumnos vean los cambios:
1. Ve a la página principal de este repositorio en GitHub.
2. Haz clic en el botón **Add file** > **Upload files**.
3. Arrastra el archivo **`datos.json`** que acabas de renombrar.
4. Escribe un mensaje breve en "Commit changes" (ej: *"Resultados jornada 3"*).
5. Pulsa el botón verde **Commit changes**.

*GitHub actualizará automáticamente la página en unos segundos.*

### 3. Visualización (Rol del Alumno)
Los alumnos deben acceder a través del siguiente enlace para ver la clasificación y los partidos en modo "solo lectura":

> **https://[TU-USUARIO].github.io/[NOMBRE-DEL-REPO]/index.html?modo=ver**

* **Nota:** El parámetro `?modo=ver` oculta los botones de administración para una experiencia más limpia.
* **Nota 2:** Si los cambios no aparecen inmediatamente, pide a los alumnos que refresquen la página. El sistema está configurado para evitar que el móvil guarde datos antiguos.


