# 🏒 Xestor de Torneos Escolares - CEIP Balaídos (Versión Cloud)

Ferramenta web para a xestión en tempo real do Torneo de Nadal de hóckey. Conectada a Google Firebase para actualizacións instantáneas e saltar filtros escolares.

## 🔗 Ligazóns

| Para que | Ligazón |
|---|---|
| 🏑 App do torneo (profesor, con login) | https://pablobarrefer.github.io/torneo-hockey/torneo_hockey.html |
| 🎓 App do torneo (alumnado, só lectura) | https://pablobarrefer.github.io/torneo-hockey/torneo_hockey.html?modo=ver |
| 🎲 Sorteo de equipos | https://pablobarrefer.github.io/torneo-hockey/sorteo_equipos.html |

Ficheiros do repositorio: `torneo_hockey.html` (app), `sorteo_equipos.html` (sorteo) e este `README.md`. Para actualizar, sube o ficheiro novo co mesmo nome desde GitHub (Add file → Upload files) e recarga a páxina con Cmd+Shift+R.

## ✅ Orde recomendada de uso

1. **Sorteo:** en `sorteo_equipos.html`, carga a lista de cada clase (unha vez), sortea diante do alumnado e garda os equipos.
2. **Enviar ao torneo:** co botón «🏑 Enviar ao torneo» os equipos pasan ao grupo correspondente da app (só os nomes dos equipos).
3. **Torneo:** na app, entra como profesor, xera as xornadas de cada grupo e engade escudos e fotos se se quere.
4. **Partidos:** introduce resultados (ou usa o ⏱️ marcador) e xera as eliminatorias cando remate cada fase.
5. **Copia de seguridade** antes de cada fase importante.

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
* As fotos de equipo non aparecen nas listas de equipos: só na **galería**, que está pechada por defecto (botón «📷 Ver galería»), para que a páxina sexa áxil.
* As imaxes redúcense (foto ≈ 60 KB, escudo ≈ 8 KB) e gárdanse en Firebase na ruta `torneo_img`, aparte dos datos do torneo. O alumnado só descarga as que ve.
* Tamén se pode seguir usando unha URL de imaxe no lugar da cámara.

## 🗓️ Curso escolar e edición

Ao escribir o curso (por exemplo `2026-2027`) o título calcula automaticamente o número de edición en cifras romanas, a razón dunha edición por curso: **2018-2019 foi a XV**, polo que **2026-2027 é a XXIII**.

## 🎲 Sorteo de equipos

Ferramenta independente para facer o sorteo diante do alumnado: `sorteo_equipos.html`
(https://pablobarrefer.github.io/torneo-hockey/sorteo_equipos.html).

* **Equipos de 4** (2 nenas + 2 nenos) da mesma clase, sorteados con aleatoriedade segura do navegador. Se as contas non cadran, algunhas persoas xogan en dous equipos (marcadas con ★).
* **Listas por clase:** cárgase unha vez o CSV/TXT (ou pegando a lista) e a páxina detecta nenas e nenos polo nome; hai que revisar os nomes dubidosos. O día do sorteo só se elixe a clase e se preme «Sortear».
* **Revelado equipo por equipo**, en pantalla completa para proxectar. Ao final pódese poñer o nome que escolla cada equipo.
* **Gardar equipos**, copiar, imprimir e descargar un CSV con todos os equipos.
* **Enviar ao torneo:** escribe os equipos no grupo correspondente da app (4ºA → grupo 4A). Despois hai que xerar as xornadas en cada grupo.
* **Privacidade:** as listas e os equipos con nomes gárdanse **só no navegador** do ordenador usado. Ao torneo só se envían os nomes dos equipos (Equipo 1, 2… ou o que escollan), nunca os do alumnado.
* **Copia de seguridade:** o navegador pode borrar os datos (habitual en ordenadores compartidos). Descarga a copia de seguridade da propia páxina e gárdaa nun lugar teu.
* Para enviar ao torneo hai que abrir a páxina desde GitHub Pages (non como ficheiro local) e ter a sesión de profesor iniciada.

## 🖥️ Outras funcións

* Modo proxector, impresión e temas de cores.
* Exportar a Excel/CSV.
* Filtros por ciclo e curso, e ocultar a liga.

## 🛠️ Xestión técnica

### Seguridade

* **Lectura aberta:** calquera persoa coa ligazón pode ver o torneo (é o que permite que o alumnado entre sen login). Na base de datos só hai resultados, nomes de equipo e imaxes con emojis; **nunca nomes do alumnado**.
* **Escritura só do profesor:** as regras de Firebase (Realtime Database → Regras) deben permitir escribir só ao usuario do profesor, por exemplo `".write": "auth != null && auth.uid === 'UID_DO_PROFESOR'"`, e a lectura aberta `".read": true`. Firebase seguirá avisando de que a lectura é pública; é o comportamento desexado.
* O aviso «regras inseguras» de Firebase polo acceso de lectura pode ignorarse.

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
