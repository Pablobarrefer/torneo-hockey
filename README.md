# 🏒 Xestor de Torneos Escolares - CEIP Balaídos (Versión Cloud)

Ferramenta web para a xestión en tempo real do Torneo de Nadal de hóckey.
Conectada a **Google Firebase** para actualizacións instantáneas e saltar filtros escolares.

## 🚀 Como funciona

A aplicación ten dous comportamentos automáticos:

### 1. 🎓 Modo Alumno / Familias (Só lectura)
- **Acceso:** Calquera persoa que entre na ligazón.
- **Que ven?** Clasificacións, resultados e fotos actualizados ao segundo.
- **Seguridade:** Non poden editar, borrar nin estragar nada.

### 2. 🛡️ Modo Profesor (Administración)
- **Acceso:** Na mesma ligazón, preme o botón azul **"🔒 Acceso Profesor"**.
- **Login:** Introduce o email e contrasinal de administrador.
- **Funcionalidades:**
    - Desbloquéanse os controis de edición.
    - Aparecen os botóns para xerar xornadas, eliminatorias e cargar fotos.
    - **Gardado Automático:** Calquera cambio que fagas gárdase na nube ao instante. Non hai botón de "Gardar", faise só.

---

## 🛠️ Xestión Técnica

### Copias de Seguridade
Aínda que o sistema é automático, recoméndase facer un backup periódico:
1. Entra como Profesor.
2. Vai a "Xestión de datos".
3. Preme **"📤 Exportar"** e garda o texto nun documento seguro.

### Restaurar datos
Se ocorre unha catástrofe (borrado accidental), podes recuperar os datos:
1. Entra na consola de [Firebase Console](https://console.firebase.google.com/).
2. Vai a **Realtime Database**.
3. No menú de tres puntos (⋮), elixe **Importar JSON** e sube a túa copia de seguridade.

---
*Deseñado para funcionar en PC, Tablet e Móbil.*

---

Proxecto de código aberto para a xestión deportiva escolar en galego.


