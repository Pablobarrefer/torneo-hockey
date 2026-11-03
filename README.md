# 🏒 Xestor de Torneos Escolares - CEIP Balaídos (Versión Cloud)

Ferramenta web para a xestión en tempo real do Torneo de Nadal de hóckey. Conectada a Google Firebase para actualizacións instantáneas e saltar filtros escolares.

Ligazón da aplicación: https://pablobarrefer.github.io/torneo-hockey/torneo_hockey.html

## 🚀 Como funciona

A aplicación ten dous comportamentos automáticos:

### 1. 🎓 Modo Alumno / Familias (só lectura)

* **Acceso:** calquera persoa que entre na ligazón. Para o alumnado recoméndase engadir `?modo=ver` ao final: `.../torneo_hockey.html?modo=ver`.
* **Que ven?** Clasificacións, resultados, eliminatorias, estatísticas de nivel e galería de equipos, actualizados ao segundo.
* **Seguridade:** non poden editar, borrar nin estragar nada.

### 2. 🛡️ Modo Profesor (administración)

* **Acceso:** na mesma ligazón, preme o botón "🔒 Acceso Profesor (Editar)".
* **Login:** introduce o email e o contrasinal de administrador (xestionados en Firebase Console → Authentication).
* **Funcionalidades:**
  * Desbloquéanse os controis de edición.
  * Xerar xornadas (dobre rolda), eliminatorias por nivel e Gran Final de ciclo (con prórroga e penaltis).
  * Introducir resultados á man ou co **⏱️ marcador e cronómetro de mesa** de cada partido.
  * Fair play, premios de grupo e estatísticas por nivel.
  * Xestionar equipos, escudos e fotos (ver abaixo).
* **Gardado:** os resultados e demais cambios gárdanse na nube ao instante. Son excepción os **equipos** (preme "Gardar equipos" no grupo) e o **curso escolar** (preme "💾 Gardar" ou Enter).

## 📷 Fotos de equipo e escudos

Nos equipos de cada grupo, o profesor ten dous botóns: **🛡️ Escudo (cámara)** e **📷 Foto equipo**. No móbil abren a cámara ou a galería.

* **Foto de equipo (protección de imaxe):** o detector de caras funciona **no propio navegador** (nada se envía a terceiros) e pon un emoji sobre cada cara. Hai vista previa: tocando unha cara sen emoji engádese, e tocando un emoji quítase. Opción de estilo cómic. A foto orixinal non se garda en ningún sitio; só se sube a versión con emojis. Revisa sempre a vista previa antes de gardar.
* **Escudo debuxado:** recorte cadrado con zoom e mellora automática de contraste e fondo branco.
* As imaxes redúcense (foto ≈ 60 KB, escudo ≈ 8 KB) e gárdanse en Firebase na ruta `torneo_img`, aparte dos datos do torneo. O alumnado só descarga as que ve.
* Tamén se pode seguir usando unha URL de imaxe no lugar da cámara.

## 🗓️ Curso escolar e edición

Ao escribir o curso (por exemplo `2026-2027`) o título calcula automaticamente o número de edición en cifras romanas, a razón dunha edición por curso: **2018-2019 foi a XV**, polo que **2026-2027 é a XXIII**.

## 🖥️ Outras funcións

* Modo proxector, impresión e temas de cores.
* Exportar a Excel/CSV.
* Filtros por ciclo e curso, e ocultar a liga.

## 🛠️ Xestión técnica

### Copias de seguridade

Aínda que o sistema é automático, recoméndase facer un backup periódico (por exemplo, cada semana):

1. Entra como Profesor.
2. Preme "📤 Exportar Backup" e garda o ficheiro nun lugar seguro. **Ollo:** esta copia garda os datos do torneo pero **só as referencias das imaxes, non as imaxes**.
3. Para unha copia **completa** (incluídas fotos e escudos), entra en [Firebase Console](https://console.firebase.google.com/) → Realtime Database, e no menú de tres puntos (⋮) da raíz elixe **Exportar JSON**.

### Restaurar datos

Se ocorre unha catástrofe (borrado accidental):

* **Só datos do torneo:** como Profesor, preme "📥 Importar JSON" e pega o contido da copia de "Exportar Backup".
* **Todo (con imaxes):** en Firebase Console → Realtime Database, no menú de tres puntos (⋮) elixe **Importar JSON** e sube a copia completa.

### Reiniciar o torneo

O botón "🗑️ Reiniciar" borra **todos** os datos do torneo e as imaxes en Firebase. Fai antes unha copia de seguridade.

### Recomendacións antes de empezar

* Probar a aplicación en PC, tablet e móbil, e nun ordenador Abalar do centro (o filtro da Consellería pode bloquear dominios de Firebase).
* Abrir sempre a páxina desde a ligazón de GitHub Pages: abrir o ficheiro en local (`file://`) impide o login.

Deseñado para funcionar en PC, Tablet e Móbil.
Proxecto de código aberto para a xestión deportiva escolar en galego.

Proxecto de código aberto para a xestión deportiva escolar en galego.


