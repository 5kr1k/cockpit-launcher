
# Cockpit Launcher

Un mini-proyecto simple para ejecutar **Cockpit** como una pseudo-aplicación
nativa, usando **Chromium** en modo `--app` y un lanzador `.desktop`.

Permite abrir Cockpit en una ventana limpia, sin barra de direcciones ni
pestañas, integrándose perfectamente con KDE Plasma u otros entornos.

---

## Características

- Abre Cockpit en una ventana minimalista tipo "app".
- Usa un perfil dedicado de Chromium.
- Incluye lanzador `.desktop` compatible con:
  - KDE Plasma (ideal),
  - GNOME,
  - XFCE, Cinnamon, Mate.
- Permite agregar reglas de ventana en KDE para quitar los bordes.
- Código muy simple: sólo un script y un archivo `.desktop`.

---

## Instalación

### 1. Copiar el script

Guarda el archivo `cockpit-app` en:
~/.local/bin/cockpit-app

Y dale permisos:

```bash
chmod +x ~/.local/bin/cockpit-app
``` 
---

### 2. Instalar el lanzador

Copia cockpit.desktop en:
~/.local/share/applications/cockpit.desktop

Opcional: edita la ruta para que apunte a tu usuario.

Luego actualiza la base de datos de KDE:
~$ kbuildsycoca6

### 3. (Opcional) Icono

Puedes incluir un icono PNG/SVG en:
~/.local/share/icons/cockpit.png

El lanzador está configurado para usar esa ruta.

---

## Integración con KDE Plasma

Para una experiencia más “nativa”, puedes crear una Regla de Ventana
(Configuración del sistema → Comportamiento de ventanas → Reglas de ventanas)
para que la ventana con clase Cockpit se abra:

- sin bordes,

- sin barra de título,

- con tamaño fijo.

Esto convierte al launcher en una app prácticamente indistinguible de una nativa.

---

## Uso

Desde terminal:
~$ cockpit-app

O desde el menú:
Aplicaciones → Cockpit

Puedes anclarlo al panel o al gestor de tareas.

---

## Contribuciones

¡Bienvenidas! Este es un proyecto pequeño pero útil para quienes quieren integrar
Cockpit en su escritorio Linux de forma más limpia.

---

Desarrollado por Sergio Hernández
