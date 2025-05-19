# React MFE in Angular Host Application

This project is an example of how to integrate a Micro Frontend (MFE) built in **React** as a remote inside an **Angular** host application using Module Federation.

---

## 🏁 Quick Start

### 1. Start the Angular shell (requires remote already built)

```bash
npx nx serve wc-ng-shell
```
> _Starts the Angular host application (`wc-ng-shell`). The React remote must be previously built._

### 2. Serve the React remote in development mode

```bash
npx nx serve wc-react-remote
```
> _Starts the development server for the React remote MFE with hot reload._

---

## ⚙️ Build Commands

- **Build the Angular host:**
  ```bash
  npx nx build wc-ng-shell
  ```
  > _Builds the Angular host application for production or integration._

- **Build the React remote:**
  ```bash
  npx nx build wc-react-remote
  ```
  > _Builds the React remote MFE for production._

---

## 📂 Relevant Structure

- `wc-react-remote/src/remote-entry.tsx`  
  _Entry point for the React MFE._
- `wc-react-remote/module-federation.config.ts`  
  _Module Federation configuration for the React remote._
- `ng-shell/module-federation.config.ts`  
  _Module Federation configuration for the Angular host._
- `ng-shell/src/app/app.component.ts`  
  _Main component of the Angular host._
- `ng-shell/src/app/app.component.html`  
  _Main template of the Angular host._

---

## 💡 Tips & Best Practices

- **Local development:**  
  You can run both servers (`wc-ng-shell` and `wc-react-remote`) in parallel for local development.  
  _Open two terminals and run the serve/build commands as needed._

- **Remote configuration:**  
  Make sure the remote URLs are correctly set in both `module-federation.config.ts` files.

- **Hot Reload:**  
  The React remote supports hot reload using the `serve` command.

- **Debugging:**  
  If you have issues loading modules, check the browser console and port configuration.

---

## 📚 Covered Topics

- Angular uses **Webpack** to build the host.
- React uses **Rspack** to build the remote.
- Practical example of Angular + React integration via Module Federation.

---

