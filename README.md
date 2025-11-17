# 🏒 Xestor de Torneos Escolares - CEIP Balaídos

Benvido/a ao repositorio do Xestor de Torneos Escolares, unha ferramenta web creada para organizar o Torneo de Nadal de hóckey do CEIP Balaídos (e adaptable a outros torneos).

Esta aplicación está contida nun único ficheiro HTML que inclúe toda a lóxica (JavaScript) e os estilos (CSS) necesarios para funcionar.

## 🚀 Como Usar a Ferramenta

A ferramenta ten dous modos de uso principais, que se controlan a través da URL.

### 1. Modo Xestión (para profesores/administradores)

É o modo por defecto que permite editar todos os aspectos do torneo.

- **Acceso:** Abre o ficheiro `torneo.html` directamente no navegador ou accede ao enlace principal publicado en GitHub Pages.
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
  - Exemplo: `https://o-teu-usuario.github.io/o-teu-repositorio/torneo.html?modo=ver`
- **Funcionalidades:**
    - Ver todos os equipos, xornadas, resultados e clasificacións.
    - Os controis de edición están ocultos e desactivados.
    - Permite usar os filtros para visualizar por ciclo ou por curso.
    - Permite activar o "Modo Proxector".

## 🛠️ Fluxo de Traballo para o Administrador

O ciclo de traballo para manter o torneo actualizado é o seguinte:

1.  **Editar Localmente:** Abre o teu enlace de xestión (sen `?modo=ver`). Introduce os novos resultados dos partidos. Os datos gárdanse automaticamente no teu navegador (`LocalStorage`).
2.  **Exportar Datos:** Na sección "Xestión de datos", preme o botón **`📤 Exportar`**. Isto copiará o estado actual de todo o torneo no teu portapapeis.
3.  **Actualizar en GitHub:**
    - Edita o ficheiro `torneo.html` directamente en GitHub.
    - Busca a liña `let state = {};`.
    - Substitúe o contido de `{}` polo texto que acabas de copiar.
    - Garda os cambios ("Commit changes").

Ao facelo, a versión pública da páxina quedará actualizada ao instante para que todos poidan ver os novos resultados.

## 🎨 Estrutura do Proxecto

O proxecto está deseñado para ser o máis sinxelo posible, contendo todo nun único arquivo:

- **`torneo.html`**: Contén a estrutura HTML, os estilos CSS e toda a lóxica JavaScript.

## 💡 Posibles Melloras Futuras

Este proxecto pode seguir medrando. Algunhas ideas para o futuro son:

- Implementar criterios de desempate avanzados (enfrontamento directo).
- Engadir unha sección para o "Máximo Goleador" ou "MVP da Xornada".
- Crear efectos visuais para celebrar os campións.

---

*Proxecto creado coa axuda de diferentes IA para o CEIP Balaídos.*
