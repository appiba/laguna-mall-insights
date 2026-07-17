# LAGUNA MALL INSIGHTS

Plataforma web para encuestas, análisis de visitantes e inteligencia comercial de Laguna Mall.

## 1. Instalar dependencias

```bash
npm install
```

## 2. Ejecutar localmente

```bash
npm run dev
```

Abra la URL local que muestre Vite. La aplicación funciona inicialmente con `localStorage`.

## 3. Crear versión de producción

```bash
npm run build
```

La carpeta generada será `dist/`.

## 4. Publicar en GitHub Pages

1. Cree un repositorio en GitHub.
2. Suba el proyecto a la rama `main`.
3. En GitHub, entre a **Settings > Pages**.
4. En **Build and deployment**, seleccione **GitHub Actions**.
5. Cada vez que suba cambios a `main`, GitHub creará la versión publicada.

La app usa `HashRouter` para funcionar correctamente en GitHub Pages. Los enlaces públicos quedarán así:

- Inicio: `https://usuario.github.io/repositorio/`
- Encuesta: `https://usuario.github.io/repositorio/#/encuesta`
- Administración: `https://usuario.github.io/repositorio/#/admin/login`

## 5. Configurar Google Apps Script

La aplicación incluye la configuración inicial:

```ts
const CONFIG = {
  apiUrl: "",
  useLocalStorage: true
};
```

También puede editar esos valores desde **Configuración** dentro del panel administrativo.

Cuando tenga la URL `/exec` de Google Apps Script:

1. Péguela en **Configuración > URL de Google Apps Script**.
2. Mantenga activado **Usar almacenamiento local**.
3. Guarde.
4. Presione **Subir datos locales a Google Sheets**.
5. Desactive **Usar almacenamiento local**.
6. Guarde otra vez.

## 6. Credenciales administrativas de demostración

Las credenciales iniciales están en `src/context/AppContext.tsx`.

- Usuario: `PATO NIETO`
- Clave: `241987`

Estas credenciales son solo para demostración. Antes de publicar la aplicación, deben reemplazarse por autenticación segura.
