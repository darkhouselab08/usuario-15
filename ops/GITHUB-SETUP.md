# Protocolo — Cuenta y repo de GitHub

> **Estado:** ✅ Hecho. Cuenta creada, repo `darkhouselab08/usuario-15` conectado y en **privado**. Esta guía queda como referencia/histórico.

Guía paso a paso que se siguió para crear la cuenta y dejar el proyecto **Refugio del Cielo** publicado.

## 1. Crear la cuenta

1. Ir a **https://github.com/signup**
2. **Email**: usar `darkhouselab026@gmail.com` (o el que prefieras para el negocio).
3. **Password**: mínimo 15 caracteres, o al menos 8 con un número y una minúscula. Usa una contraseña única y guárdala en un gestor.
4. **Username**: elige uno corto y profesional. Sugerencias: `refugiodelcielo`, `refugio-del-cielo`, `franco-refugio`. Debe estar disponible.
5. Resuelve el desafío de verificación (puzzle).
6. Clic en **Create account**.

## 2. Verificar el email

1. GitHub envía un código de 6–8 dígitos a `darkhouselab026@gmail.com`.
2. Abre el correo (revisa spam) e ingresa el código.

## 3. Preferencias iniciales

1. Cuando pregunte el plan, elige **Free** (gratis, suficiente para este proyecto).
2. Las preguntas de personalización ("how do you plan to use GitHub") son opcionales; puedes saltarlas.

## 4. Activar 2FA (autenticación de dos factores) — recomendado

1. Ve a **Settings → Password and authentication**.
2. En **Two-factor authentication**, clic en **Enable 2FA**.
3. Escanea el QR con una app (Google Authenticator, Authy, 1Password).
4. **Guarda los códigos de recuperación** en un lugar seguro — sin ellos puedes perder el acceso.

## 5. Configurar el perfil (opcional pero útil)

- Foto, nombre visible y una bio corta ("Refugio del Cielo — cabaña-mirador off-grid, Tobía").

## 6. Publicar el proyecto

Una vez creada la cuenta:

1. En GitHub, clic en **+ → New repository**.
2. **Repository name**: `refugio-del-cielo`
3. **Description**: "Landing one-page de Refugio del Cielo".
4. Visibilidad: **Private** — el repo guarda datos de negocio (`ops/`), nunca debe ser público. Ver `ARQUITECTURA.md`.
5. **No** marques "Add README / .gitignore / license" (ya los tenemos en local).
6. Clic en **Create repository**.
7. Conectar el repo local (ya tiene commit inicial) — desde tu terminal, en la carpeta del proyecto:

```bash
git remote add origin https://github.com/<TU-USUARIO>/refugio-del-cielo.git
git push -u origin main
```

GitHub te pedirá autenticación. La forma recomendada es un **Personal Access Token** (Settings → Developer settings → Personal access tokens) usado como contraseña, o instalar **GitHub CLI** (`gh auth login`).

## 7. Publicar la web con GitHub Pages

El sitio vive en `frontend/`, no en la raíz, así que Pages necesita el modo por Actions (no "deploy from branch"):

1. Repo → **Settings → Pages**.
2. Source: **GitHub Actions**.
3. Ya existe el workflow `.github/workflows/deploy.yml` que publica `frontend/` en cada push a `main`. En el primer push a `main` después de activar esto, corre solo.
4. URL resultante: `https://<TU-USUARIO>.github.io/usuario-15/`.

> Pendiente de decisión: GitHub Pages vs Netlify (ver `ops/INBOX.md` INB-004). El workflow queda listo pero dormido hasta activar el Source de arriba.

---

**Datos que solo tú debes ingresar:** email, contraseña, código de verificación y códigos 2FA. Nunca los compartas.
