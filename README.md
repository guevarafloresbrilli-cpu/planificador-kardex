# Huerto Escolar de Brilli Guevara Flores — Planificador con kardex

## Propósito
Mejora de mi Planificador de materiales de la semana 7 (taller de huerto escolar, presupuesto S/ 200.00) con un pequeño **kardex** de materiales ficticios: alta de materiales con código estable, búsqueda por nombre o código, cambio de nombre por id, entradas y salidas enteras positivas, existencia física (entradas − salidas), inactivación/eliminación y exportación de movimientos a CSV. Se conservan el cálculo en céntimos, el presupuesto y la validación del pedido. La existencia física es independiente del dinero del presupuesto.

## Archivos
- `index.html`: estructura del planificador (S7) y, al final de `<main>`, la sección `#kardex` (ids `k-*`). Carga `app.js` y luego `kardex.js`.
- `styles.css`: estilos S7 + reglas S9 al final (variable `--color-personal`, etiqueta `.etiqueta-kardex`, tabla del kardex).
- `app.js`: lógica del planificador S7 (sin cambios).
- `kardex.js`: reglas y comportamiento del kardex (`saldoDe`, `agregarMovimiento`, `exportarCSV` y eventos de pantalla).
- `README.md`: este documento.

## Ejecutar y usar
Local: conserve todos los archivos en la misma carpeta y abra `index.html` en Chrome o Edge. Publicado: abra el enlace de GitHub Pages.
1. Escriba un nombre y pulse **Crear material** (se asigna un código tipo `MAT-001`).
2. Elija el material (o filtre con **Buscar por nombre o código**).
3. Elija ENTRADA o SALIDA, escriba una cantidad entera positiva y pulse **Registrar movimiento**.
4. **Cambiar nombre** actúa por id; **Eliminar sin movimientos o inactivar** pide confirmación (cancelable). Un material con movimientos se inactiva y conserva su historial.
5. **Exportar CSV** descarga `movimientos-materiales.csv` (separador `;`, para abrir en Excel).

## Personalización
- Etiqueta HTML: «Nombre del material del huerto (ficticio)» (antes: «Nombre del material»).
- Tamaño CSS de la etiqueta: `font-size: 1.25rem` (antes 1.1rem).
- Paleta RGB: verde `rgb(22,101,52)`, coherente con el tema de huerto; contraste con texto blanco ≈ 7:1.

## Publicación
Repositorio: https://github.com/guevarafloresbrilli-cpu/planificador-kardex
Sitio GitHub Pages: https://guevarafloresbrilli-cpu.github.io/planificador-kardex/

## Aportes y ayuda recibida
Autora: Brilli Guevara Flores (trabajo individual ET505 · S9). Base: mi proyecto S7 y los «Fragmentos de integración ET505 · S9» entregados por el curso.

Utilicé inteligencia artificial como herramienta de apoyo para revisar el trabajo de acuerdo con las indicaciones y los criterios de evaluación establecidos en la rúbrica proporcionada por el docente. Elegí el color verde porque tiene algo en común con mi título, el Huerto Escolar de Brilli Guevara Flores. El detalle está en el PDF entregado en MAXEDRA.

## Límites
- Datos ficticios. Los datos del kardex se guardan en `localStorage`: pertenecen sólo a este navegador y origen; no hay base de datos compartida ni multiusuario.
- El CSV es una copia de los movimientos, no una sincronización con Excel.
- El pedido del planificador sigue siendo temporal (se pierde al recargar), como en S7.
