# Data contract / Структура данных

Version `0.1.0`: starter interchange format, not a validated site dataset. All CSV files contain headers only. Copy them to approved private storage before entering real data. JSON `null` and empty CSV cells mean unknown/not entered; **never substitute zero**. Text may be Russian or English; field names, IDs and enum values stay unchanged.

Версия `0.1.0`: начальный формат обмена, не проверенная база объекта. CSV содержат только заголовки. Перед заполнением скопируй их в согласованное закрытое пространство. `null` в JSON и пустая ячейка CSV означают «неизвестно/не введено»; **не подставляй ноль**. Описания могут быть русскими или английскими; ключи, ID и служебные значения не переводятся.

## Evidence states / Статусы подтверждения

| `source_state` | Meaning / Значение | Estimating treatment / Для сметы |
|---|---|---|
| `verified_plan` | Verified against an identified drawing, not necessarily today's installation / Сверено с конкретным чертежом, не обязательно соответствует состоянию сегодня | Cite sheet/revision; assess currency / Указать лист/редакцию и актуальность |
| `observed_field` | Direct field observation/measurement / Наблюдение или обмер на месте | Cite photo, note, measurement or timestamp / Ссылка на фото, запись, обмер или таймкод |
| `inferred` | Unverified interpretation / Непроверенное предположение | Allowance/alternate only; verification needed / Только предварительный резерв/вариант, нужна проверка |
| `proposed` | Intended new work, not existing / Предлагаемые работы, не существующее состояние | Define scope and quantity basis / Указать состав работ и основание количества |
| `unknown` | No usable evidence / Нет пригодных данных | No firm quantity/price; explicit verification or allowance / Не фиксировать объём/цену; проверка или явный резерв |

`confidence`: `high`, `medium`, `low`, or blank if not assessed. Confidence is a review judgment, not a statistical probability. `source_refs`: semicolon-separated evidence IDs; keep actual links/paths in the private manifest. `created_at` / `updated_at`: ISO 8601 timestamps. Every real entity has a unique stable ID and a `model_id` of `CV255` or `NC3007`; references must point to the same property's records unless an explicit cross-property relationship is documented.

`confidence`: `high`, `medium`, `low` либо пусто, если оценка ещё не сделана. Это экспертная оценка, не статистическая вероятность. `source_refs`: ID источников через точку с запятой; сами ссылки/пути — в закрытом реестре. Временные метки — ISO 8601. У каждой реальной записи постоянный уникальный ID и `model_id`: `CV255` или `NC3007`; ссылки относятся к тому же объекту, кроме явно описанных межобъектных связей.

## Templates / Шаблоны

| File | Contents / Содержание |
|---|---|
| `project.json` | Property IDs and empty collections; dimensions/model files not supplied / ID объектов и пустые коллекции; размеров/моделей ещё нет |
| `spaces.csv` | Floor/room, dimensions, units, ceiling/access conditions / Этаж/комната, размеры, единицы, потолок и доступ |
| `assets.csv` | Devices, location, existing/proposed state, visible attributes / Устройства, расположение, существующее/предлагаемое, видимые характеристики |
| `routes.csv` | Endpoints, pathway, length and its basis / Концы трассы, тип прокладки, длина и её основание |
| `estimate.csv` | Quantities, pricing basis and statuses, separate cost components / Количества, основание/статус цен и отдельные составляющие стоимости |
| `assumptions.csv` | Assumption, impact, verification method, responsible person, resolution / Допущение, влияние, способ проверки, ответственный и результат |
| `media-manifest.csv` | Evidence IDs, private relative paths, room and video timestamps / ID источников, закрытые относительные пути, помещение и таймкоды |

## Units, quantities, and costs / Единицы, количества и стоимость

- `dimension_unit` and `length_unit`: `ft`, `in`, `m`, or `mm`; required with any numeric length. Record originals. `quantity_unit`: `each`, `ft`, `m`, `sq_ft`, `sq_m`, or `hour`. Do not combine unlike units. / Для длины обязательно указать единицу; исходные обмеры сохраняются. Не складывать разные единицы.
- `length_basis`: `measured`, `plan_scaled`, `inferred`, `allowance`, or `unknown`. Route length follows a documented path with vertical transitions; point-to-point distance is not installed cable length. / Основание длины указать явно; учесть вертикальные участки. Расстояние по прямой не равно длине проложенного кабеля.
- `scope_state`: `existing`, `proposed`, or `allowance`. `pricing_status`: `ready`, `allowance`, `excluded`, or `verify`. `ready` means reviewed for preliminary pricing, never construction approval. / Существующее, предлагаемое или резерв; «готово» означает готовность к предварительной оценке, не разрешение на строительство.
- `quantity` is the count/length of the selected unit, not a cost. Cost fields are in `currency` (use `USD` when quoting US dollars). `material_unit_cost` is per quantity unit; `labor_hours` and `equipment_cost` are **line totals**. `labor_rate_per_hour` is hourly. `contingency_amount` is an explicit line total, not an implicit percentage. / Количество не является ценой. Материал — за единицу; часы труда, оборудование и резерв — на всю строку; ставка — за час.
- Before tax/markup: `line_subtotal = quantity × material_unit_cost + labor_hours × labor_rate_per_hour + equipment_cost`. `line_total = line_subtotal + contingency_amount`. A missing required input leaves the total unknown, not zero. Enter `0` only when confirmed not applicable; prevent double-counting package prices. / При отсутствии нужного значения итог остаётся неизвестным. Ноль ставится только при подтверждённом отсутствии этой составляющей; стоимость комплектов не учитывать дважды.
- `pricing_basis` and `pricing_date` record the quote/catalog/assumption and date. No prices are supplied. Markups, taxes, permits, testing, disposal and exclusions must be separately identified before any client total; this schema does not calculate them automatically. / Основание и дата цены обязательны; готовых цен нет. Наценки, налоги, разрешения, испытания, вывоз и исключения указываются отдельно до вывода клиентского итога; автоматического расчёта здесь нет.

## Future model layers / Будущие слои модели

`base_geometry`, `observed_existing`, `inferred_existing`, `proposed_scope`, `risk_and_access`. Use distinct labels and rendering styles, not color alone. A beautiful render cannot upgrade evidence. Each model version must retain its source/measurement references and changes that affect takeoff quantities.

Слои: геометрия, наблюдаемое существующее, предполагаемое существующее, предлагаемые работы, риски/доступ. Различать подписями и стилем отображения, не только цветом. Красивый рендер не повышает достоверность. Каждая версия модели сохраняет источники, обмеры и изменения, влияющие на объёмы.
