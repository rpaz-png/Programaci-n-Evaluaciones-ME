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

## Datos

Generado a partir de `Evaluaciones y Horarios 20262.xlsx` (exportado de ARES-PUCP).
Se incluyen 538 evaluaciones de 29 cursos. Quedan fuera los niveles menores al 5°,
el nivel 0 y los cursos que no pertenecen a ninguna de las cinco ramas.

Para actualizar los datos, edita el arreglo `EVENTS` dentro de `index.html`.

## Notas

- La fuente Poppins se carga desde Google Fonts; sin conexión el calendario usa una
  tipografía de sistema y sigue funcionando igual.
- Los logos van incrustados como data URI, así que el archivo es autocontenido.
