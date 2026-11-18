# Sophy Hub: versiones publicadas

**Sophy Hub**, de [Sophy Systems](https://www.sophysystems.com), es un puente local entre dispositivos Shelly y sistemas Savant (compatible con Savant).

Este repositorio contiene solo las versiones publicadas. No contiene código fuente.

## Instalar o actualizar

En el host, como el usuario normal (en los Smart Hosts de Savant es `RPM`, no root):

```sh
curl -fsSL https://get.sophysystems.com | sh
```

URL directa, por si la anterior no responde:

```sh
curl -fsSL https://github.com/d-krugger/sophy-hub-releases/releases/latest/download/get.sh | sh
```

El instalador hace lo siguiente:

1. Descarga Node.js y verifica su suma SHA-256.
2. Descarga la versión estable más reciente.
3. Verifica la firma Ed25519 del paquete. Si no es válida, no instala nada.
4. Instala el hub en `~/sophy-hub`. En una actualización conserva la configuración, la base de datos y los usuarios.

Equipos compatibles: Smart Hosts de Savant (Linux ARM) y Pro Hosts (macOS 11 o superior).

Para no activar el arranque automático, agrega `-s -- --no-autostart` después de `sh`.

«Savant» es marca de Savant Systems.
