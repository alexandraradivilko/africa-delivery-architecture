# Диаграммы проекта

Все диаграммы созданы из PlantUML или Mermaid. Для каждой диаграммы сохранено одно изображение: PNG для PlantUML, SVG для Mermaid.

| Задание | Диаграмма | Исходник | Изображение |
|---|---|---|---|
| 1 | Влияние и интерес | [mmd](Task1/stakeholder-influence-interest.mmd) | [SVG](Task1/stakeholder-influence-interest.svg) |
| 2 | C4 Context | [puml](Task2/c4-context.puml) | [PNG](Task2/c4-context.png) |
| 2 | Use Case | [puml](Task2/use-cases.puml) | [PNG](Task2/use-cases.png) |
| 3 | Наблюдаемость | [mmd](Task3/observability.mmd) | [SVG](Task3/observability.svg) |
| 4 | C4 Container | [puml](Task4/c4-container.puml) | [PNG](Task4/c4-container.png) |
| 4 | Deployment | [puml](Task4/deployment-diagram.puml) | [PNG](Task4/deployment-diagram.png) |
| 5 | Roadmap | [mmd](Task5/roadmap.mmd) | [SVG](Task5/roadmap.svg) |
| 5 | Value Stream | [puml](Task5/value-stream.puml) | [PNG](Task5/value-stream.png) |

## Повторный рендеринг

Проверенные версии: PlantUML 1.2025.2 (Java 17, Graphviz) и Mermaid 11.12.1. Для PlantUML: `java -jar plantuml.jar -charset UTF-8 -tpng путь/к/файлу.puml`. C4 Context использует библиотеку C4, включённую в PlantUML.

Для Mermaid передать содержимое `.mmd` в `mermaid.render` версии 11.12.1 и сохранить поле `svg`. Параметры использованного рендеринга:

```json
{"startOnLoad":false,"theme":"default","securityLevel":"strict","fontFamily":"Arial","themeVariables":{"quadrantPointFill":"#444444","quadrantPointTextFill":"#131300"},"gantt":{"useMaxWidth":false,"fontSize":16,"leftPadding":330,"barHeight":28,"sectionFontSize":18},"quadrantChart":{"chartWidth":1000,"chartHeight":900},"flowchart":{"useMaxWidth":false}}
```

Встроенные Mermaid-блоки в документах соответствуют отдельным `.mmd`. При изменении исходника необходимо обновить встроенный блок и изображения. Дата проверки — 04.11.2026.
