# Conectar este repo a GitHub Pages

Una sola vez. Después, cada cambio en `web/index.html` se publica solo.

## 1) Crear el repositorio en GitHub

En https://github.com/new:
- **Nombre:** `archivo-del-corazon` (o el que quieras)
- **Público** — en el plan gratis, Pages solo funciona con repos públicos.
  Acá no hay nada privado: ni credenciales ni grabaciones. Ver el README.
- **No** marques "Add a README" ni ".gitignore": este repo ya los tiene.

## 2) Conectarlo y subir

Desde `ARCHIVOS/web/publicar`:

```bash
git remote add origin https://github.com/TU_USUARIO/archivo-del-corazon.git
git push -u origin main
```

Git te va a pedir usuario y contraseña. **La contraseña NO es la de tu cuenta**: hay que
crear un token en https://github.com/settings/tokens → *Generate new token (classic)* →
marcar el permiso **repo**. Copiá el token y pegalo como contraseña.
macOS lo guarda en el Llavero, así que se pide una sola vez.

## 3) Encender Pages

En el repo: **Settings → Pages**
- *Source:* **Deploy from a branch**
- *Branch:* `main`, carpeta `/ (root)` → **Save**

En un minuto el sitio queda en:

```
https://TU_USUARIO.github.io/archivo-del-corazon/
```

## 4) Comprobar que la publicación automática anda

```bash
cd ../.. && ARCHIVOS/web/../../venv/bin/python ARCHIVOS/web/publicar_sitio.py --url
```

Y para publicar a mano en cualquier momento:

```bash
cd /Users/elericelias/Desktop/ECG/ARCHIVOS/web && ../../venv/bin/python publicar_sitio.py
```
