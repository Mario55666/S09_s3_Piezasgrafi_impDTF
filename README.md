# Simulador 3D · Sistema DTF 8072-3 + DF-800A

Página web autocontenida para la Unidad didáctica **Producción y publicación de piezas gráficas** del IES Público Diseño y Comunicación (IDC). Reúne un simulador 3D de una impresora DTF de 60 cm con agitador de polvo, una guía de procedimientos de operación y seguridad, un ejercicio resuelto de verificación previa de un arte final, un verificador de archivos, los anexos de control de calidad y un generador de reporte PDF por estudiante.

- Autor: Mg. Mario Quiroz Martínez, 2026
- Publicación: https://claude.ai/artifact/2A8vegxfxzo7qbiy5d6Lqu
- Formato: un archivo HTML (`index.html`, ≈ 1,8 MB) con estilos, scripts, imágenes y un TIFF de ejemplo incrustados

---

## 1. Equipo modelado

Datos de la ficha comercial "60 CM2 HEAD DTF PRINTE".

| Parámetro | Impresora 8072-3 | Agitador DF-800A (Pro) |
|---|---|---|
| Cabezales | Epson i3200-A1 × 2 | — |
| Ancho de impresión / alimentación | 600 mm | 600 mm |
| Resolución | 3200 ppp | — |
| Tinta | Pigmento C/M/Y/K + blanco | — |
| Alimentación | 220 V 50/60 Hz (110 V opcional), 1500 W | — |
| Velocidad | Paso 6: 9,2 m²/h | — |
| Calefacción | — | 5 tubos infrarrojos |
| Entorno | 18–30 °C, 40–60 % HR | — |
| Medidas de la máquina | 182 × 81 × 155 cm | 194 × 101 × 107 cm |
| Medidas del paquete | 210 × 87 × 75 cm | 157 × 115 × 128 cm |
| Peso N.W. / G.W. | 171 / 230 kg | 310 / 329 kg |

Características listadas en la ficha: presión ajustable de tres garras, transferencia de archivos por WiFi, sistema anticolisión, estación de tapado, servomotor Leadshine. El kit incluye CPU, tintas y estabilizador de voltaje.

El texto extraíble del PDF difiere de la imagen de la ficha en el paquete y el peso de la impresora; se usan los valores de la imagen.

---

## 2. Secciones de la página

| N.° | Sección | Contenido |
|---|---|---|
| — | Portada | Título, canales CMYK + W, seis indicadores de ficha |
| 01 | Simulador | Escena 3D con cuatro vistas (operación, explosionada, circuito de tinta, interior del agitador), rótulos, panel de mandos, parámetros, tanques, registro de eventos |
| 02 | Estructura | 16 tarjetas de componentes; cada una enfoca la pieza en 3D |
| 03 | Sistema de tinta | Esquema animado tanque → damper → cabezal, retorno de circulación W |
| 04 | Procesos | Diagrama de 7 etapas sincronizado con el simulador y tabla de control por etapa |
| 05 | Seguridad | 25 ítems marcables en seis grupos, con etiqueta Ficha / Práctica general |
| 06 | Especificaciones | Tablas de ficha |
| 09 | Costos | Límites de formato, aprovechamiento de film por formato, calculadora de costo de material |
| 07 | Guía GP-DTF-01 | Objetivo, alcance, normativa, responsabilidades, EPP, 7 POE, matriz IPERC 3 × 3, registro por sesión |
| 08 | Arte final | Ejercicio resuelto, iteraciones v1–v4, imagen con errores, verificador de archivo, vista 3D de capas |
| A | Anexo A | Ficha técnica de verificación (DTF / impresión 3D FDM) |
| B | Anexo B | Checklist de 27 ítems con firmas |
| — | Reporte PDF | Formulario de estudiante y generación del PDF |

---

## 3. Simulador 3D

- Escala: 1 unidad = 10 cm. Geometría esquemática construida con primitivas a partir de las medidas exteriores de la ficha.
- Tiempo simulado ×20. Avance real del film: (m²/h ÷ 0,6 m) ÷ 3600.
- Velocidad por modo de paso: paso 6 = 9,2 m²/h (ficha); pasos 4 y 8 = 9,2 × 6 / n (estimación proporcional, señalada en pantalla).
- Túnel IR: respuesta de primer orden con τ = 120 s simulados. Ventana de curado 160–170 °C (material del curso).
- Bloqueos: sin encendido no hay impresión; el paro de emergencia corta movimiento y calefacción y exige rearme; tanque vacío detiene la impresión.
- Advertencias: local fuera de 18–30 °C o 40–60 % HR, agitador detenido durante la impresión, túnel fuera de 160–170 °C, circulación W detenida, nivel bajo de tanque.
- El film muestra el arte cargado en el verificador, en espejo y a escala sobre 600 mm de ancho.

---

## 4. Valores de referencia del control de calidad

| Parámetro | Referencia | Fuente |
|---|---|---|
| Modo de color | CMYK + canal alfa (TIFF o PSD) | Curso |
| Transparencia | Canal alfa activo, sin recuadros sólidos | Curso |
| Dimensiones | Formato objetivo ± 1 mm | Taller |
| Ancho máximo | ≤ 600 mm | Ficha |
| Resolución | ≥ 300 ppi a tamaño real | Taller |
| Peso | ≤ 50 MB | Taller |
| Píxeles semitransparentes (alfa 1–254) | ≤ 3 % del área impresa | Taller |
| Margen libre | ≥ 5 mm | Taller |
| Línea / punto mínimo | ≥ 0,5 mm | Práctica DTF |
| Registro CMYK vs. blanco | ± 0,2 mm (medido en film) | Curso |
| Curado en horno | 160–170 °C | Curso |
| Planchado | Algodón 160 °C / 15 s; poliéster 140 °C / 45 s | Curso |

Impresión 3D FDM (Anexo A, selector de técnica): pared ≥ 1,2 mm; ≥ 3 perímetros con boquilla de 0,4 mm; boquilla 210 °C; cama 60 °C; cotas ± 0,2 mm (± 0,1 mm en ajustes).

Un PNG no admite CMYK. El verificador califica un PNG RGBA como "observación" y un archivo sin alfa como "desviación".

---

## 5. Verificador de archivo

Acepta TIFF (CMYK + alfa) y PNG. El análisis se ejecuta en el navegador.

| Medición | Método |
|---|---|
| Modo y perfil | PNG: bloques IHDR e iCCP. TIFF: etiquetas 262, 277, 338 y 34675 (decodificación con UTIF.js) |
| Resolución | PNG: bloque pHYs. TIFF: etiquetas 282 y 296. Sin dato: se asumen 72 ppi |
| Tamaño | px ÷ ppi × 25,4, comparado con el formato objetivo editable |
| Semitransparencia | Píxeles con alfa 1–254 ÷ píxeles con alfa > 0 |
| Recuadro sólido | Sin canal alfa, o borde exterior opaco > 50 %, o cobertura > 98 % |
| Margen | Distancia mínima del contenido opaco al borde |
| Colores | Muestreo 1:64 de zonas opacas, cuantizado a 3 bits por canal |

Al cargar un archivo se actualizan: tabla de datos de la pieza, vistas previas (arte, capa W, espejo), imagen con mapa de defectos y marcadores, lista de errores con corrección recomendada, detalle ampliado con simulación de alfa binario, polo, film del simulador, vista 3D de capas y calculadora de costos. El botón "Restaurar ejemplo resuelto" devuelve el estado inicial.

Vista 3D de capas: film PET, capa CMYK, capa de blanco, polvo adhesivo y mapa de control, cada una con su estado. "Vista sobre prenda" invierte la pila y muestra la imagen legible.

---

## 6. Ejercicio resuelto: arte final

Impresión frontal de 280 × 350 mm para camiseta de algodón azul marino. Valores medidos sobre los archivos generados:

| Versión | Archivo | Resolución | Semitransp. | Margen | Peso | Estado |
|---|---|---|---|---|---|---|
| v1 | `arte_v1_control_previo.png` | 150 ppi | 33,46 % | 0,00 mm | 0,32 MB | 5 desviaciones |
| v2 | `arte_v2_correccion1.png` | 300 ppi | 3,13 % | 11,94 mm | 0,38 MB | 1 desviación |
| v3 | `IDC_DTF_arte_final_280x350_300ppi.png` | 300 ppi | 0,00 % | 12,02 mm | 0,32 MB | RGB |
| v4 | `IDC_DTF_arte_final_280x350_300ppi_CMYK.tif` | 300 ppi | 0,00 % | 12,02 mm | 0,61 MB | Conforme |

Correcciones aplicadas: reexportación a 300 ppi; eliminación de la sombra difusa y umbral de alfa en 128; titular de 27 a 17 mm de cuerpo; líneas de 0,25 a 0,6 mm; punto mínimo de 0,30 a 0,7 mm; conversión a CMYK FOGRA39 (intento colorimétrico relativo) con alfa no asociado y compresión deflate.

---

## 7. Costos y tamaños

Límites: ancho de impresión 600 mm; ancho útil 590 mm (5 mm de margen por lado); largo continuo, limitado por la bobina (100 m en el formato comercial de 60 cm).

Fórmulas por pieza:

```
film      = 0,6 m × (alto de fila + 5 mm) ÷ piezas por fila × (precio del rollo ÷ 60 m²)
tinta     = área × cobertura × consumo (ml/m²) ÷ 1000 × precio por litro   (color y blanco por separado)
polvo     = área × cobertura × consumo (g/m²) ÷ 1000 × precio por kg
energía   = m² de film ÷ 9,2 m²/h × 1,5 kW × tarifa
total     = (film + tintas + polvo + energía) × (1 + merma)
```

Valores de partida: rollo S/ 270,00 (TIMG, Lima, consultado el 29/10/2026); tinta color 18 ml/m² y blanca 25 ml/m² (ficha Coltex: 15–20 y 20–30 ml/m²); polvo 24 g/m² (m8d.io). Precios de tinta (S/ 150 y 170 por litro), polvo (S/ 90 por kg) y tarifa eléctrica (S/ 0,80 por kWh): estimaciones marcadas "reemplazar". Resultado con la pieza de ejemplo: S/ 0,729 por pieza. No incluye prenda, mano de obra, mantenimiento ni depreciación.

---

## 8. Reporte PDF

- Campos: nombres y apellidos (obligatorios), código y sección (opcionales). El nombre se copia al Anexo A y a la firma del operador.
- Contenido: datos y dictamen (página 1), imagen con errores y resultado del verificador (página 2), Anexo A (página 3), Anexo B y firmas (página 4). Pie con autoría, estudiante y paginación.
- Dictamen APTO solo si el Anexo A está conforme y el verificador no registra desviaciones. Si el archivo del Anexo A difiere del analizado, el reporte lo indica.
- Nombre del archivo: `Reporte_CC_DTF_<Apellidos>_<Nombres>_<AAAA-MM-DD>.pdf`.
- Descarga mediante la capacidad `downloads` del artefacto; el visitante confirma cada descarga. Fuera de claude.ai el PDF se genera pero no se descarga.

---

## 9. Normativa citada en la guía

- Ley N.° 29783, Ley de Seguridad y Salud en el Trabajo (2011), y Ley N.° 30222
- D.S. N.° 005-2012-TR, Reglamento de la Ley N.° 29783
- R.M. N.° 050-2013-TR, formatos referenciales de registros del SGSST

La matriz IPERC de la guía es una versión simplificada 3 × 3 de uso didáctico (NR = P × S; 1–2 bajo, 3–4 moderado, 6–9 alto), no el método oficial de la R.M. 050-2013-TR.

---

## 10. Bibliotecas

| Biblioteca | Versión | Uso | Carga |
|---|---|---|---|
| Three.js | 0.186.1 | Escenas 3D | jsDelivr, import map |
| Anime.js | 4.5.0 | Animación y adaptador Three | jsDelivr, import map |
| UTIF.js + pako | 3.1.0 / 1.0.11 | Lectura de TIFF | jsDelivr, carga diferida |
| jsPDF + AutoTable | 2.5.1 / 3.8.2 | Reporte PDF | cdnjs, carga diferida |
| IBM Plex Sans / Mono | — | Tipografía | Google Fonts |

---

## 11. Limitaciones

- Geometría 3D esquemática; no reproduce piezas internas reales del fabricante.
- Grosor de línea y diámetro de punto no se miden de forma automática; se registran desde el original vectorial.
- El registro CMYK vs. blanco solo se puede medir en el film impreso.
- La conversión CMYK → RGB de la vista previa TIFF es aproximada (UTIF.js).
- Precios de tinta, polvo y energía sin cotización peruana verificada.
- Las listas, fichas y firmas no se guardan entre visitas; se conservan en el PDF.

---

## 12. Archivos entregados

| Archivo | Descripción |
|---|---|
| `index.html` | Página publicada |
| `IDC_DTF_arte_final_280x350_300ppi_CMYK.tif` | Arte final v4, CMYK + alfa, FOGRA39 |
| `arte_v1_control_previo.png` | Arte v1 con errores, para práctica del verificador |
| `Reporte_CC_DTF_*.pdf` | Ejemplo de reporte generado |
| `SUPERPROMPT.md` | Instrucción para regenerar el documento |

---

Mg. Mario Quiroz Martínez 2026 — Unidad didáctica de Producción y publicación de piezas gráficas
