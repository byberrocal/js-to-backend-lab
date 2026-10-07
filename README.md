# De JS a Backend 🧪

Laboratorio interactivo **para hacer en clase, en parejas** (programación por parejas:
Piloto/Copiloto). Cubre el puente de JavaScript al backend, con **código que se ejecuta de verdad**.

**Bilingüe ES/EN · Sistemas Web · Grado en IA · Universidad San Jorge**

## Estaciones
1. 🚦 **Inicio · en parejas** — cómo trabajar (roles, cambios de rol)
2. ➡️ **Arrow functions** — sintaxis `=>`, y el cambio en `this`
3. ⏳ **async / await** — promesas, esperar sin congelar, secuencial vs `Promise.all`
4. 🌳 **El DOM** — el árbol vivo que JS lee y modifica (sandbox real)
5. ⚡ **Sincronía en el DOM** — bugs jugables: respuestas en desorden (carrera) y pintar antes de tener el dato; con su arreglo
6. 💾 **BBDD local (IndexedDB)** — mini-app de notas real que **persiste** al recargar
7. ☁️ **BBDD en la nube** — `fetch` **en vivo** a una API pública + patrón **Supabase/Firebase** y por qué hace falta un backend

Todo en **un solo `index.html`** (HTML + CSS + JS, sin dependencias ni build).

## Características
- Editor de código **ejecutable** en cada estación (botón *Ejecutar*).
- Demos interactivas de los bugs de sincronía (botones *Simular*, casilla *Arreglar*).
- **IndexedDB** real y **fetch** real a la nube.
- Modo **claro/oscuro**, barra de **parejas** (nombres + cambiar roles), botón **ES/EN**.

---

## Desplegar en Vercel

### GitHub + Vercel (URL estable para alumnos)
```bash
cd js-to-backend-lab
git init && git add . && git commit -m "De JS a Backend"
git branch -M main
git remote add origin https://github.com/byberrocal/js-to-backend-lab.git
git push -u origin main
```
Luego en https://vercel.com → **Add New… → Project** → importa `byberrocal/js-to-backend-lab`
→ Framework **Other** → **Deploy**. La URL `…vercel.app` es la que pasas a tus alumnos.
Cada `git push` vuelve a desplegar.

### O con Vercel CLI
```bash
cd js-to-backend-lab
vercel --prod
```

## Notas
- El progreso (estación, idioma, tema, nombres) se guarda en el navegador de cada alumno.
- La estación de la nube hace una llamada real a `jsonplaceholder.typicode.com` (necesita internet).
- Para añadir/editar estaciones: en `index.html`, cada estación es una función `m…(p)` registrada en el array `STATIONS`.
