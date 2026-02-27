# 🌿 Ingredientes de Temporada — Provincia de Buenos Aires

Dashboard interactivo que mapea la disponibilidad estacional de frutas, verduras y hierbas en las principales zonas productivas de la provincia de Buenos Aires.

👉 **[Ver dashboard en Tableau Public](https://public.tableau.com/app/profile/julia.fernandez8319/vizzes)**

---

## ¿Qué muestra este proyecto?

- **¿Qué ingredientes están en temporada este mes?** — filtrable por mes, categoría y subcategoría
- **¿Dónde se producen?** — mapa de zonas productivas con intensidad de producción por variedad
- **¿Cuándo es la temporada de cada familia?** — calendario visual de cucurbitáceas, carozos, hoja, raíz y más

---

## Estructura del proyecto

```
📁 ingredientes-temporada-bsas
├── README.md
├── dashboard_temporadas_bsas.csv   ← dataset principal (612 filas)
├── ingredientes.csv                ← catálogo de 45 ingredientes
├── temporadas.csv                  ← relación ingrediente × zona × mes
└── zonas_geo.csv                   ← 7 zonas con coordenadas
```

---

## Dataset

| Campo | Descripción |
|---|---|
| `mes_num` / `mes_nombre` | Mes del año (1-12 / Enero-Diciembre) |
| `ingrediente` | Nombre del ingrediente |
| `categoria` | fruta / verdura / hierba |
| `subcategoria` | carozo, hoja, raíz, tubérculo, etc. |
| `zona` | Zona productiva de la provincia |
| `disponibilidad` | plena / inicio / fin |
| `disponibilidad_valor` | plena=3, inicio=1, fin=2 (campo calculado) |
| `lat` / `lon` | Coordenadas de la zona |
| `tipo_clima` | Clima característico de la zona |

**Zonas incluidas:**
- Delta del Tigre
- GBA Norte Hortícola
- GBA Sur Hortícola
- Costa Atlántica
- Cuenca del Salado
- Pampa Húmeda Interior
- Sur Bonaerense

---

## Dashboard — Vistas

### 🗺️ Mapa Zonas
Mapa de la provincia con las zonas productivas. El tamaño y color de cada punto indica la diversidad de ingredientes producidos. Filtrable por subcategoría.

### 📅 Disponibilidad por Mes
Heatmap que muestra qué ingredientes están disponibles cada mes. Filtros por mes, categoría y subcategoría.

### 📊 Temporada por Familia
Gráfico de barras que muestra la intensidad de producción por mes para cada familia de ingredientes (cucurbitáceas, carozos, hoja, raíz, etc.).

---

## Fuente de datos

Los datos fueron construidos a partir de:
- Calendarios de producción del **INTA** (Instituto Nacional de Tecnología Agropecuaria)
- Conocimiento agronómico de las zonas productivas bonaerenses
- Expertise culinario propio

---

## Próximos pasos

- [ ] Agregar zona Oeste bonaerense (Junín, Pergamino, 9 de Julio)
- [ ] Incorporar datos de precios mayoristas (Mercado Central / INDEC)
- [ ] Conectar dataset a Google Sheets como fuente de datos viva
- [ ] Análisis de correlación precio × temporada

---

## Sobre la autora

**Julia Fernandez** — Chef profesional reconvertida en Data Analyst.  
15+ años en gastronomía de autor (Zaranda ★, Berasategui ★★★, Fotografiska ★ Green) + formación en Python, SQL y visualización de datos.

🔗 [Tableau Public](https://public.tableau.com/app/profile/julia.fernandez8319/vizzes) · [LinkedIn](https://linkedin.com/in/julia-fernandez-481144233) · [GitHub](https://github.com/AilujDH)
