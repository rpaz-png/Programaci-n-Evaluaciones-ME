# Calendario de Evaluaciones · Ciclo 2026-2

Calendario interactivo de las evaluaciones (exámenes, prácticas y laboratorios) de
Ingeniería Industrial — ciclos 5° a 10°, del 17 de agosto al 11 de diciembre de 2026.

Línea gráfica Made Easy.

## Contenido

| Archivo | Descripción |
|---|---|
| `index.html` | Aplicación completa. Todo va embebido (datos, estilos, logos). No requiere servidor ni dependencias. |

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `calendario-262`).
2. Sube el contenido de este zip a la raíz del repositorio.
3. Entra a **Settings → Pages**.
4. En *Source* elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
5. Guarda. En 1–2 minutos el calendario queda disponible en
   `https://<tu-usuario>.github.io/<nombre-del-repo>/`

## Uso

- **Vistas:** Semana (por defecto), Mes y Agenda de todo el ciclo.
- **Navegación:** flechas verdes, botón *Hoy*, o las teclas ← y →.
- **Filtros:** ciclo (5° a 10°), rama (Analytics, Finanzas, Supply Chain, Ingeniería, Gestión)
  y tipo (Examen, Práctica, Laboratorio).
- **Cursos:** el botón verde *Seleccionar cursos* abre una lista desplegable con buscador,
  agrupada por rama. Los cursos agregados aparecen como etiquetas debajo de los filtros.
- **Detalle:** clic en cualquier evento muestra horarios, aulas, secuencia, vacantes y responsable.
- **Exportar:** el botón `.ics` descarga los eventos filtrados para importarlos a
  Google Calendar, Outlook o Apple Calendar.

## Programación de sesiones

Algunos cursos tienen cargada su programación de temas. Cuando existe, el cuadro del
calendario muestra la actividad concreta (`LABORATORIO 3`, `TAREA ACAD. 1`, `CASO 2`)
en lugar de la etiqueta genérica, y al pasar el cursor aparece el nombre completo de
la actividad junto con el tema de la sesión. Las sesiones no calificadas
(análisis de caso, sesiones dirigidas) llevan el borde punteado.

Cursos con programación cargada:

- `1IND45` Control Estadístico de Calidad
- `1IND52` Diseño de la Cadena de Suministros y Operaciones

Para agregar otro curso, edita el objeto `PROGRAMAS` en `index.html`:

```js
'CLAVE': {
  1: {act:'Laboratorio 1', short:'LABORATORIO 1', cal:true, tema:'Tema de la sesión'},
  2: {act:'Análisis de caso 1', short:'CASO 1', cal:false, tema:'...'}
}
```

La llave numérica es la **semana académica** (1 a 16), que corresponde a la semana del
archivo de horarios menos uno: la semana 1 de clases es la del 17 de agosto.

## Datos

Generado a partir de `Evaluaciones y Horarios 20262.xlsx` (exportado de ARES-PUCP).
Se incluyen 483 sesiones de 29 cursos. Cuando un mismo curso y horario tienen un bloque
de *Laboratorio* seguido inmediatamente de uno de *Práctica*, ambos se fusionan en una sola
sesión de laboratorio con el rango horario completo. Quedan fuera los niveles menores al 5°,
el nivel 0 y los cursos que no pertenecen a ninguna de las cinco ramas.

Para actualizar los datos, edita el arreglo `EVENTS` dentro de `index.html`.

## Notas

- La fuente Poppins se carga desde Google Fonts; sin conexión el calendario usa una
  tipografía de sistema y sigue funcionando igual.
- Los logos van incrustados como data URI, así que el archivo es autocontenido.
