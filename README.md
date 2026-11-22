# Análisis exploratorio del inventario de otras especies en el departamento de Sucre

Trabajo del curso Fundamentos de programación para ciencias biológicas.
Autora: [su nombre]

## De qué trata el conjunto y de dónde sale
El conjunto es el inventario de equinos, asnos, mulos, búfalos, ovinos y caprinos de los 26 municipios del departamento de Sucre (Colombia), con una fila por municipio y año, de 2001 a 2025 (sin 2006). Tiene 622 filas y 10 columnas; tras la limpieza quedan 621 filas.

**Fuente:** Gobernación de Sucre. (2025). *Inventario Otras especies en el departamento de Sucre* [Conjunto de datos]. Portal de Datos Abiertos de Colombia, datos.gov.co. Licencia CC BY-SA [confirme la versión en la página del conjunto]. https://www.datos.gov.co/Ambiente-y-Desarrollo-Sostenible/Inventario-Otras-especies-en-el-departamento-de-Su/33bv-k4eh/about_data. Descargado el 21 de noviembre de 2026.

## Preguntas que se respondieron
1. **¿El inventario de las especies difiere entre subregiones?** Sí, y depende de la especie: en búfalos la mediana va de 55 (Montes de María) a 2191 (San Jorge).
2. **¿Cómo cambió el inventario de equinos entre 2001 y 2025?** No hay una tendencia común; cada subregión cambia distinto, y San Jorge tiene el descenso más marcado.
3. **¿Las especies se relacionan entre sí?** Solo de forma débil o moderada: las correlaciones van de −0,17 a 0,43.

## Figuras principales
**Figura 1. Distribución del inventario de ovinos.** La mediana es 1137 animales y la distribución tiene una cola larga hacia valores altos.

![Figura 1](figuras/figura1_distribucion_ovinos.png)

**Figura 2. Búfalos por subregión.** San Jorge tiene la mediana más alta (2191) y Montes de María la más baja (55).

![Figura 2](figuras/figura2_bufalos_por_subregion.png)

**Figura 3. Equinos y mulos.** Tienden a subir juntos, pero la relación es débil (correlación 0,43).

![Figura 3](figuras/figura3_equinos_mulos.png)

**Figura 4. Equinos en el tiempo.** Las subregiones no cambian igual: Montes de María es la más baja y estable, y Mojana la más variable.

![Figura 4](figuras/figura4_equinos_en_el_tiempo.png)

**Figura 5. Correlaciones entre especies.** Las más altas son equinos con mulos (0,43) y equinos con asnos (0,42); solo búfalos tiene correlaciones negativas.

![Figura 5](figuras/figura5_correlaciones.png)

## Cómo reproducir el análisis desde cero
Se usó Python 3.14.7.

1. Descargue el repositorio (botón verde **Code → Download ZIP**) y descomprímalo.
2. Abra una terminal en la carpeta descomprimida, y cree y active un entorno virtual:
   ```powershell
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```
3. Instale las bibliotecas:
   ```powershell
   pip install -r requirements.txt
   ```
4. Abra `analisis_parcial_fundamentos.ipynb` en VS Code o en Jupyter, elija como kernel el entorno `.venv`, y ejecute todas las celdas de arriba abajo (**Restart → Run All**).

El cuaderno lee el archivo `Datos/Inventario_Otras_especies_en_el_departamento_de_Sucre_20261121.csv`, así que debe abrirse desde la carpeta raíz del proyecto. Las figuras se guardan en la carpeta `figuras`.

## Contenido del repositorio
| Archivo o carpeta | Qué contiene |
|---|---|
| `analisis_parcial_fundamentos.ipynb` | El código, las tablas, las figuras y su interpretación |
| `Datos/` | El conjunto de datos original |
| `figuras/` | Las cinco figuras en formato PNG |
| `Evidencias/` | Capturas que documentan los problemas técnicos y las decisiones |
| `requirements.txt` | Bibliotecas de Python con sus versiones |
