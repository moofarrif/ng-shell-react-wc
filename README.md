# React MFE in Angular Host Application

Este proyecto es un ejemplo de cómo integrar un Micro Frontend (MFE) hecho en **React** como remoto dentro de una aplicación **Angular** como host, utilizando Module Federation.

---

## 🏁 Inicio rápido

### 1. Levantar el shell Angular (requiere remoto ya compilado)

```bash
npx nx serve wc-ng-shell
```
> _Levanta la aplicación Angular host (`wc-ng-shell`). El remoto React debe estar previamente compilado._

### 2. Servir el remoto React en modo desarrollo

```bash
npx nx serve wc-react-remote
```
> _Levanta el servidor de desarrollo para el MFE React remoto con hot reload._

---

## ⚙️ Comandos de build

- **Compilar el host Angular:**
  ```bash
  npx nx build wc-ng-shell
  ```
  > _Compila la aplicación Angular host para producción o integración._

- **Compilar el remoto React:**
  ```bash
  npx nx build wc-react-remote
  ```
  > _Compila el MFE React remoto para producción._

---

## 📂 Estructura relevante

- `wc-react-remote/src/remote-entry.tsx`  
  _Punto de entrada del MFE React._
- `wc-react-remote/module-federation.config.ts`  
  _Configuración de Module Federation para el remoto React._
- `ng-shell/module-federation.config.ts`  
  _Configuración de Module Federation para el host Angular._
- `ng-shell/src/app/app.component.ts`  
  _Componente principal del host Angular._
- `ng-shell/src/app/app.component.html`  
  _Template principal del host Angular._

---

## 💡 Tips y buenas prácticas

- **Desarrollo local:**  
  Puedes correr ambos servidores (`wc-ng-shell` y `wc-react-remote`) en paralelo para desarrollo.  
  _Abre dos terminales y ejecuta los comandos de serve/build según corresponda._

- **Configuración de remotos:**  
  Verifica que las URLs de los remotos estén correctamente configuradas en ambos archivos `module-federation.config.ts`.

- **Hot Reload:**  
  El remoto React soporta hot reload usando el comando `serve`.

- **Depuración:**  
  Si tienes problemas de carga de módulos, revisa la consola del navegador y la configuración de los puertos.

---

## 📚 Temas cubiertos

- Angular usa **Webpack** para construir el host.
- React usa **Rspack** para construir el remoto.
- Ejemplo práctico de integración Angular + React vía Module Federation.

---

