# Savant Hub: versiones publicadas

Este repositorio contiene solo las versiones publicadas de Savant Hub, el puente local entre Shelly y Savant. No contiene código fuente.

## Instalar o actualizar

En el host Savant, como el usuario normal (en los Smart Hosts es `RPM`, no root):

```sh
curl -fsSL https://github.com/d-krugger/savant-hub-releases/releases/latest/download/get.sh | sh
```

El instalador hace lo siguiente:

1. Descarga Node.js y verifica su suma SHA-256.
2. Descarga la versión más reciente.
3. Verifica la firma Ed25519 del paquete. Si no es válida, no instala nada.
4. Instala el hub. En una actualización conserva la configuración, la base de datos y los usuarios.

Equipos compatibles: Smart Hosts de Savant (Linux ARM) y Pro Hosts (macOS).

Para no activar el arranque automático:

```sh
curl -fsSL https://github.com/d-krugger/savant-hub-releases/releases/latest/download/get.sh | sh -s -- --no-autostart
```
