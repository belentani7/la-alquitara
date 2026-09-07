# LA ALQUITARA · Apothecary Shader Engine (beta autónoma) · AGPLv3

UI library invertida: no es estante muerto (shadcndaisy/MUI/Radix). Comprende su entorno,
destila sus propios assets (fragment shaders WebGL validados por compilación real),
gestiona su GPU y se detiene sola al saciarse. Doble mundo: pociones ⌬ cinabrio ⇄ GLSL copiable.

## Repo

```
la-alquitara/
├── index.html   # TODO: motor + sensor + mercado + previews WebGL (cero deps JS)
└── README.md
```

## Comandos

```bash
# Opción A: abrir directo (doble clic en index.html)
# Opción B: servir local
npx serve Documents/01_PROYECTOS/la-alquitara
# → http://localhost:3000
```

Sin build, sin npm install. Solo necesita internet para fuentes Google (Sora/Inter/JetBrains Mono).

## Instrucciones de uso

1. Abrir: el sensor lee GPU (WEBGL_debug_renderer_info), cores, memoria, puntero,
   gamut, hora local y reduced-motion → fija techo (7/12 vasijas), resolución y sesgo paleta.
2. Destilación (cada 2.8s): combina 9 familias × 5 colorizadores, compila en contexto
   compartido; lo inerte o repetido se descarta con log. Para al saciarse
   (diversidad ≥4 familias + conteo ≥ techo, o 6 rechazos seguidos): estado SACIADA.
3. Mercado: precio oscila (seno + tier), stock aleatorio, eventos de escasez cada 9s,
   comentarios alien. Adquirir descuenta ⌬ y stock; a stock 0 el programa GPU se borra.
4. Transfusión manual: pega tu GLSL (debe traer `void main`), se valida compilando;
   si pasa, entra al estante como poción propia.
5. Consumo real: Copiar GLSL (portapapeles) o .glsl (descarga). Previews en pausa
   fuera de viewport (IntersectionObserver) para no quemar GPU.

## Notas honestas

- Máx ~12 contextos WebGL (límite navegador ~16): previews pausados + deconsecración al agotar.
- `file://` funciona; clipboard requiere contexto seguro (localhost o https).
- ES primario; EN/PT pendientes. Tema BELENTANI v1.1 CHROMA.
