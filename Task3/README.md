# Задание 3. Требования к качеству и стратегия доступности

Для MVP на модульном монолите предлагаются отдельные контракты каталога, оплаты и уведомлений. «Сервис» здесь означает предоставляемую возможность, а не обязательный отдельный процесс или микросервис. Статус требований — **предложены к согласованию и проверке до запуска**.

| Документ | Назначение |
|---|---|
| [nfr-registry.md](nfr-registry.md) | Измеримые НФТ, проверки и соответствие Cloud Native checklist |
| [availability-economics.md](availability-economics.md) | Стоимость дополнительных девяток, бюджеты ошибок и пределы выбранного уровня |
| [slo/catalog.md](slo/catalog.md) | Доступность, задержка и актуальность каталога |
| [slo/payments.md](slo/payments.md) | Собственный API, внешний платёжный путь и отражение подтверждений |
| [slo/notifications.md](slo/notifications.md) | Своевременная передача уведомлений и контроль доставки |
| [quality-attribute-scenarios.md](quality-attribute-scenarios.md) | Сценарии качества с шестью полями и критериями испытаний |
| [fmea.md](fmea.md) | Отказы собственных компонентов и партнёров, RPN и меры защиты |
| [adr-002-caching-strategy.md](adr-002-caching-strategy.md) | Что кешируется, TTL, инвалидация и допустимая деградация |
| [observability.md](observability.md) | Четыре золотых сигнала, сбор телеметрии, алерты и действия дежурного |

## Источники

- Требование непрерывной работы и $12 тыс. выручки за минуту распродажи: источник — артефакт 1, реплика инвестора «One minute of downtime during a sale».
- Мобильная производительность: источник — артефакт 2, разделы «Target audience» и «Experience requirements from the brand side».
- 99,99%, RPO=0, multi-cloud и наблюдаемость: источник — артефакт 5, разделы «Cloud native, properly», «Multi-cloud from the start» и «Availability»; приложение — Cloud Native checklist.
- Лимит расходов: источник — артефакт 6, п. 1; ограничение штата — п. 5. Пункты — семь последовательных абзацев ограничений от «Infrastructure» до «Licensed software».
- Обработка данных и внешние платежи: источник — артефакт 3, разделы «Nigeria» и «Payments».
- Архитектурная основа: [ADR-001](../Task2/adr-001-architecture-style.md), [Architecture Vision](../Task2/architecture-vision.md), [допущения TCO](../Task2/tco-assumptions.md).

Методическая основа: [OpenSLO](https://openslo.com/specification/) для структуры измерений, [CNCF](https://github.com/cncf/toc/blob/main/DEFINITION.md) для Cloud Native, [Google SRE](https://sre.google/workbook/alerting-on-slos/) для бюджета ошибок и алертов. Проектные значения и условия их применения заданы в документах; они не являются требованиями этих методик.

## Assumptions

Нагрузочный профиль и цены взяты из задания 2 и остаются оценками. Возможности площадок, SLA партнёров и круглосуточное дежурство должны быть подтверждены. Требование CTO 99,99% без деградации не принято молча: предлагаемый компромисс, исключения из checklist и остаточные риски требуют решения бизнеса.

## Диаграммы и трассировка

- Наблюдаемость: [исходник](observability.mmd), [SVG](observability.svg).
- [Контракты OpenSLO v1](slo/README.md): три YAML-файла, 16 отдельных целей.
- [Связь ключевых решений с противоречиями](../decision-traceability.md).
- [Все диаграммы и правила рендеринга](../diagrams.md).
