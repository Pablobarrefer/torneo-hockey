# 🏒 Xestor de Torneos Escolares - CEIP Balaídos

Benvido/a ao repositorio do Xestor de Torneos Escolares, unha ferramenta web creada para organizar o Torneo de Nadal de hóckey do CEIP Balaídos.

Esta aplicación é unha **Web App Progresiva (PWA) estática**: todo o funcionamento está contido nun único ficheiro HTML, sen necesidade de servidores complexos nin bases de datos.

## 🚀 Modos de Uso

A ferramenta detecta automaticamente como comportarse dependendo da ligazón que utilices:

### 1. 🛠️ Modo Xestión (Profesorado)
*Prioridade: Memoria do dispositivo (LocalStorage)*

Este é o modo para introducir datos, resultados e xestionar o torneo.
- **Acceso:** Abre o ficheiro `index.html` (ou a ligazón principal sen parámetros).
- **Comportamento:** A aplicación le primeiro a memoria do teu dispositivo para non perder o traballo en curso. Se a memoria está baleira, tentará cargar os datos da nube para empezar.
- **Funcionalidades:**
    - Xestionar equipos, escudos e fotos.
    - Xerar calendarios e eliminatorias.
    - Anotar resultados e Fair Play.
    - **Sincronizar:** Botón especial para traer datos actualizados dende GitHub.

### 2. 👀 Modo Consulta (Alumnado e Familias)
*Prioridade: A Nube (GitHub)*

Este é o modo de só lectura para ver a clasificación en tempo real.
- **Acceso:** Engade `?modo=ver` ao final da URL.
  - Exemplo: `https://o-teu-usuario.github.io/nome-do-repo/index.html?modo=ver`
- **Comportamento:** Ignora a memoria local e **forza sempre a descarga** dos últimos datos subidos a GitHub (`datos.json`).
- **Funcionalidades:**
    - Visualización de táboas, resultados e galería de fotos.
    - Non aparecen botóns de borrar nin editar.

---

## 🔄 Fluxo de Traballo: Como actualizar o torneo

Para que o alumnado vexa os resultados no seus móbiles, debes seguir este proceso de "relevos" entre o teu dispositivo e GitHub.

### Paso 1: Edición (No teu PC ou Móbil)
1. Entra na aplicación en **Modo Xestión**.
2. Introduce os resultados dos partidos, xera xornadas, etc.
3. *Os datos gárdanse automaticamente na memoria do teu dispositivo.*

### Paso 2: Publicación (Subida á Nube)
Cando remates a xornada e queiras facer públicos os datos:
1. Vai á sección **⚙️ Xestión de datos**.
2. Preme o botón **"⬇️ Descargar JSON"**.
3. Gardarase un ficheiro (ex: `datos.json`) no teu dispositivo.
4. Vai a este repositorio en GitHub.
5. Preme **Add file > Upload files**.
6. Arrastra o ficheiro `datos.json` e preme no botón verde **Commit changes**.

*En 1 ou 2 minutos, a web actualizarase para todo o alumnado.*

### Paso 3: Sincronización (Cambio de dispositivo)
Se traballaches dende o móbil no patio e agora queres seguir dende o ordenador (ou viceversa):
1. Asegúrate de ter subido o `datos.json` a GitHub dende o dispositivo onde traballaches (Paso 2).
2. Abre a web no outro dispositivo (ex: o ordenador).
3. Na sección de xestión, preme o botón **"☁️ Cargar de GitHub"**.
4. Isto borrará a memoria local antiga dese dispositivo e traerá a última versión da nube.

---

## 💡 Guía de Botóns de Xestión

* **📤 Exportar JSON:** Copia os datos ao portapapeis (útil para copias de seguridade rápidas).
* **📊 Exportar Excel:** Xera un ficheiro CSV compatible con Excel con todas as estatísticas.
* **⬇️ Descargar JSON:** Descarga o ficheiro necesario para subir a GitHub.
* **☁️ Cargar de GitHub:** Forza a actualización do teu panel de control cos datos que haxa na nube (útil se cambiaches de dispositivo).
* **📷 Galería:** Activa ou desactiva a visualización da galería de fotos no panel de xestión.
* **🗑️ Reiniciar:** Borra todos os datos locais e deixa o torneo a cero (Perigo!).

---

Proxecto de código aberto para a xestión deportiva escolar en galego.
* **Nota 2:** Se os cambios non aparecen inmediatamente, pide aos alumnos que refresquen a páxina. O sistema está configurado para evitar que o móbil garde datos antigos.


