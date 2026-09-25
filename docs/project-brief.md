# Project brief / Задание

## English

**Objective:** create an editable, browser-based existing-conditions model for each property, then use source-linked rooms, devices, routes, and proposals for Sava's preliminary electrical/networking estimate.

| ID | Address | Jurisdiction |
|---|---|---|
| `CV255` | 255 Third Ave, Chula Vista, CA | City of Chula Vista |
| `NC3007` | 3007 Highland Ave, National City, CA | City of National City |

The exact floors, suites, occupied areas, intended uses, work scope, and current ownership/permission documentation must still be confirmed. Do not assume the entire property is included.

**Responsibilities:** SFS coordinates the project and model workflow. Boris coordinates incoming materials and access. Sava supplies practical trade observations, scope, quantity review, estimating assumptions, and pricing. The authorized owner supplies access and any necessary permission to obtain or use plans. Qualified professionals handle final engineering, safety, permitting, and construction decisions.

**Sequence and acceptance gates:**

1. Confirm site boundaries and priorities. Output: agreed work areas and missing-input list.
2. Collect authorized records and safe measured capture in private storage. Output: source manifest and dimensional anchors for every modeled area.
3. Build the base model. Output: browser navigation, room IDs, scale/units, floor/ceiling geometry, and measurement checks. Unknown geometry stays visibly approximate.
4. Add separate observed, inferred, and proposed layers. Output: each item has provenance, confidence, and an evidence state; inaccessible areas are marked.
5. Produce the pre-estimate. Output: quantities, units, source links, dated pricing basis, assumptions, exclusions, allowances, and Sava's review. A model screenshot alone is not a takeoff.

**Planned implementation, not built yet:** a web viewer using structured JSON/CSV records and an editable geometry export such as GLB. Keep stable IDs shared between the model and the estimate. Choose the final viewer/toolchain when usable source data arrives; do not buy software or fabricate a building from public exterior images alone.

**Immediate questions for Sava:** Which property first? Which rooms/suites? Repair/replace existing systems or add new loads/drops? What equipment and usage are planned? What access and measurements can be obtained safely?

## Русский

**Цель:** создать редактируемую браузерную 3D-модель фактического состояния каждого объекта, затем связать помещения, устройства, трассы и предлагаемые работы с источниками данных для предварительной сметы Савы по электрике и сетям.

Объекты: `CV255` — 255 Third Ave, Chula Vista; `NC3007` — 3007 Highland Ave, National City. Это разные муниципалитеты. Этажи, помещения, занятые зоны, назначение, объём работ и документы на доступ ещё нужно уточнить. Не считать автоматически, что в работу входит весь объект.

**Роли:** SFS координирует проект и моделирование. Борис организует получение материалов и доступа. Сава отвечает за практические наблюдения, состав работ, проверку количеств, допущения и цены. Уполномоченный собственник предоставляет доступ и необходимые разрешения на получение/использование планов. Окончательные инженерные решения, безопасность, разрешения и строительные работы — зона ответственности соответствующих квалифицированных специалистов.

**Этапы и критерии готовности:**

1. Уточнить границы работ и приоритеты. Результат: согласованные зоны и список недостающих данных.
2. Собрать разрешённые документы, безопасную съёмку и обмеры в закрытом пространстве. Результат: реестр источников и размерные привязки для всех моделируемых зон.
3. Построить основу модели. Результат: просмотр в браузере, ID помещений, масштаб и единицы, геометрия этажей/потолков и проверка размеров. Неизвестную геометрию явно обозначить приблизительной.
4. Добавить отдельные слои наблюдаемого, предполагаемого и предлагаемого. Результат: у каждого элемента есть источник, уровень уверенности и статус подтверждения; недоступные зоны отмечены.
5. Подготовить предварительную смету. Результат: количества, единицы, ссылки на источники, основание и дата цен, допущения, исключения, резервы и проверка Савой. Один скриншот модели не заменяет ведомость объёмов.

**Планируемая реализация, ещё не готова:** веб-просмотрщик, структурированные JSON/CSV и редактируемый экспорт геометрии, например GLB. Идентификаторы элементов модели и сметы должны совпадать. Окончательные инструменты выберем после получения пригодных исходных данных; не покупаем ПО и не выдумываем здание по одним наружным фотографиям.

**Первые вопросы Саве:** какой объект первый? Какие помещения? Ремонт/замена существующего или новые нагрузки/сетевые точки? Какое оборудование и использование планируются? Какой доступ и какие обмеры можно безопасно получить?
