# f1-pit-stop-strategy

**Panel Histórico de Rendimiento en Fórmula 1**

Comparar las estrategias de boxes entre equipos y medir el impacto del pit stop en el resultado final de la carrera.

## Fuente de datos

- **Dataset:** Formula 1 World Championship (1950-2020), Kaggle
- **Autor:** rohanrao
- **Tablas usadas:** `pit_stops`, `races`, `results`, `drivers`, `constructors`, `status`
- **Período analizado:** 2011-2024. `pit_stops` solo tiene paradas registradas desde 2011; la versión descargada llega hasta 2024.

## Herramientas

pandas, numpy, matplotlib, seaborn, SQL, Power BI.

## Estructura del repositorio

```
data/                  CSV originales y tablas generadas
F1_EDA_FRANK_2.ipynb   Notebook de preparación, limpieza y EDA
README.md
```

## Fases del proyecto

- [x] Preparación de datos
- [x] Limpieza y join de tablas
- [ ] Análisis exploratorio (EDA)
- [ ] Consultas SQL
- [ ] Dashboard en Power BI
- [ ] Documentación final

## Estado actual

Preparación y limpieza terminadas. Tengo dos tablas de trabajo: `df_stops` (una fila por parada) y `df_race` (una fila por piloto y carrera), para 285 carreras y 23 equipos. Columnas renombradas a inglés.

## Próximos pasos

Fase 3, EDA: tiempo medio de parada por equipo, relación entre cantidad de paradas y `PositionFinal`, y evolución del tiempo de parada por año.

## Decisiones de limpieza

- Conservo los 385 pilotos sin paradas. Largaron la carrera; los excluyo solo en los análisis que necesitan paradas.
- Marco con `valid_stop` las paradas anómalas (límite IQR por carrera) en vez de borrarlas.
- Agrupo `status` en `status_category`: `Finished`, `Lapped` y `DNF`.
- Renombro `positionOrder` a `PositionFinal`.
- Uso nombres de columnas y tablas en inglés, en `snake_case`, para que lleguen listos a SQL y Power BI.

## Hallazgos

_Pendiente. Se completa después del EDA._

## Dashboard

_Pendiente. Se completa en la fase 5._

## Autor

Maximiliano Frank · [GitHub](https://github.com/MaxiFrank7) · [LinkedIn](https://www.linkedin.com/in/maximiliano-frank-5641b6169/)
