# El lenguaje del corazón — archivo

Sitio del archivo de sesiones del proyecto: pulso, voz y las hojas que salen de cada
registro. Es **una sola página estática**, sin compilación ni dependencias que instalar.

Los datos NO están acá. Viven en Supabase, detrás de login y con RLS: sin una cuenta del
equipo, esta página no muestra nada.

## Qué hay en el repo

- `index.html` — la página entera (estilos y lógica incluidos)

## Qué NO hay, a propósito

- `config.json`, que lleva la `service_role_key` — esa llave salta todos los permisos
- las grabaciones de participantes (audio, ECG): son datos personales

La clave que sí aparece en `index.html` es la **anon key**, que está pensada para el
navegador y es pública por diseño. Lo que protege el contenido es el login más las
políticas de la base, no esconder esa clave.
