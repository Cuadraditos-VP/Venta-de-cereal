# Venta de Grano · Movimiento de cereal

Versión web (PWA) de la planilla `venta grano.xlsm`: ingreso de stock, ventas y resumen de ventas anuales.

## Qué hace (igual que el Excel)
- **Stock disponible** = total ingresado − total vendido. Si llega a 0 muestra **SIN STOCK** titilando.
- **Registrar venta**: fecha, cantidad (q), precio por tn ($ K) y cotización del dólar. Valida campos obligatorios, que no supere el stock y que la fecha no sea anterior a la última venta.
- **Total** = cantidad × precio tn × 100 · **Total dólares** = total ÷ cotización.
- **Ventas anuales**: suma por año (se arma solo, no hace falta agregar años a mano).
- **Cargar stock**, **borrar último ingreso** y **borrar todo** piden la contraseña.
- Filtro por año en la tabla de ventas.
- Respaldo: guardar / restaurar (JSON) y exportar a Excel (CSV).

Los datos quedan guardados en el navegador de cada dispositivo (no se comparten entre el celu y la PC). Usá el respaldo para pasarlos de uno a otro.

## Subir a GitHub Pages
1. Creá un repositorio nuevo en GitHub (por ejemplo `venta-grano`).
2. Subí **todos** los archivos de esta carpeta (index.html, manifest.webmanifest, sw.js, README.md y la carpeta `icons`).
3. En el repo: **Settings → Pages → Branch: `main` / `(root)` → Save**.
4. En 1–2 minutos queda en `https://TU-USUARIO.github.io/venta-grano/`.

## Instalar como app
- **Android (Chrome)**: abrir el link → menú ⋮ → *Instalar app* / *Agregar a la pantalla principal*.
- **iPhone (Safari)**: botón Compartir → *Agregar a inicio*.
- **PC (Chrome/Edge)**: ícono de instalar en la barra de direcciones.

Funciona sin internet una vez abierta la primera vez.

## Actualizar
Cuando cambies algo, subí los archivos y cambiá `venta-grano-v1` por `v2`, `v3`… en `sw.js`.
