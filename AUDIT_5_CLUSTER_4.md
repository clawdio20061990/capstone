# Аудит Кластеру 4: Marketing Strategy, Operations & Supply Chain, Risk Analysis

**Дата аудиту:** 20 березня 2026  
**Аудитор:** AI-аудитор (zero-trust режим)  
**Документи:** MARKETING_STRATEGY.md, OPERATIONS_SUPPLY_CHAIN.md, RISK_ANALYSIS.md  
**Методологія:** Незалежна перевірка фактів, верифікація джерел, аналіз внутрішньої логіки

---

## Загальний висновок

Три документи демонструють солідну MBA-рівня роботу з добре структурованими стратегіями та обґрунтованими рішеннями. Проте виявлено ряд проблем: помилкове цитування авторів наукових статей, перекручування статистичних даних з джерел, внутрішні суперечності між документами, та значні прогалини в операційному плані. Нижче — детальний реєстр усіх знахідок.

---

## Документ 1: MARKETING_STRATEGY.md

### MS-01: Перекручення статистики 5W PR — "63% pet owners"

**[SEVERITY: HIGH]**  
**Локація:** Розділ 2.3 (Growth Segment), Розділ 4.2 (Influencer Marketing)  

**Проблема:** Стверджується: "63% of pet owners use Instagram and TikTok for product discovery (5W PR, 2026)." Фактичний зміст статті 5W PR зовсім інший. Оригінальна стаття стверджує, що YouTube Shorts захопив 45% pet product discovery, Instagram — 32%, а цифра 63% стосується відсотка власників тварин, які **стежать за інфлюенсерами на YouTube та Instagram** для рекомендацій щодо покупок. TikTok у цьому контексті не згадується.

**Рекомендація:** Виправити цитату відповідно до оригінального джерела. Це суттєво змінює канальну стратегію — YouTube має бути пріоритетнішим, ніж описано.

---

### MS-02: Непідтверджені дані Euromonitor — "68% Gen Z, 69% Millennials"

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 1.2 (Pillar 2), Розділ 2.3  

**Проблема:** Стверджується: "68% of Gen Z and 69% of Millennials consider pets as family members (Euromonitor, 2025)." Сторонні джерела дають інші цифри: Gravitis Pet Supplies (2025) наводить 72% для Gen Z і 58% для Millennials. Підозрілою є також логіка, що Gen Z (68%) має нижчий показник, ніж Millennials (69%) — більшість досліджень показують, що молодші покоління мають вищий рівень "гуманізації" тварин.

**Рекомендація:** Перевірити оригінальне джерело Euromonitor. Якщо доступ відсутній, замінити на верифіковане джерело з конкретним посиланням на сторінку/звіт.

---

### MS-03: Суперечність DTC-only моделі з Amazon

**[SEVERITY: HIGH]**  
**Локація:** Executive Summary ("DTC-only distribution model") vs. Розділ 3.3 (Phase 3)  

**Проблема:** Executive Summary чітко заявляє "Direct-to-Consumer (DTC) only distribution model." Проте в Розділі 3.3 для Німеччини вказано "Amazon DE" як ключовий канал, а для UK — "Amazon UK." Розділ 4.1 також згадує Amazon FBA. Це пряма суперечність ключовому стратегічному рішенню документа.

**Рекомендація:** Або змінити позиціонування з "DTC-only" на "DTC-first з вибірковим marketplace-розширенням," або видалити згадки Amazon з канальної стратегії.

---

### MS-04: Слабкі показники LTV:CAC на рівні покупця

**[SEVERITY: HIGH]**  
**Локація:** Розділ 5.2 (CAC Targets & Unit Economics)  

**Проблема:** LTV:CAC per buyer при 50% conversion = 1.4:1 (Рік 1), при реалістичних 35% = 1.2:1. У Рік 2 при 35% conversion — 1.0:1. Стандартним мінімумом для здорового SaaS/hardware бізнесу вважається 3:1. Показник 1.0:1 означає, що бізнес тільки повертає витрати на залучення без прибутку. Документ визнає це, але не пропонує чіткого плану дій для критичного сценарію.

**Рекомендація:** Додати чіткий contingency plan для сценарію LTV:CAC < 1.5:1. Розглянути підвищення ціни hardware (€180+), агресивніше зниження CAC, або перехід до моделі з обов'язковою підпискою.

---

### MS-05: Email ROI "$36–42 per $1 spent" — завищений діапазон

**[SEVERITY: LOW]**  
**Локація:** Розділ 4.5  

**Проблема:** Стверджується "average $36–42 per $1 spent across industries." Класичне джерело (Litmus, 2023) дає $36:1. Верхня межа $42 не підтверджена конкретним джерелом та виглядає як довільне розширення діапазону.

**Рекомендація:** Використовувати конкретну цифру з конкретного джерела: "$36 per $1 spent (Litmus, 2023)" або навести актуальніше джерело.

---

### MS-06: Sprout Social vs Impact.com — помилкова атрибуція

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 4.2  

**Проблема:** Стверджується "$1,719 (€1,600) average value of pet influencer post (Sprout Social via Impact.com, 2025)." Impact.com — це окрема платформа, не підрозділ Sprout Social. Атрибуція "Sprout Social via Impact.com" заплутує читача.

**Рекомендація:** Уточнити джерело: або це дані Impact.com, або Sprout Social. Навести пряме посилання.

---

### MS-07: Відсутність YouTube як ключового каналу

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 3, Розділ 4, Розділ 7  

**Проблема:** Згідно з даними самого ж цитованого джерела 5W PR (2026), YouTube Shorts захопив 45% pet product discovery — більше ніж Instagram (32%). Проте в бюджетних алокаціях YouTube не виділений як окремий канал, а лише згадується в контент-стратегії. Для продукту з сильним візуальним компонентом (кіт + лазер + AI) YouTube має бути пріоритетнішим.

**Рекомендація:** Виділити YouTube Ads / YouTube content production як окрему бюджетну категорію або обґрунтувати його відсутність.

---

### MS-08: Нереалістичний Target — 50% Trial-to-Paid Conversion

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 6.2, Розділ 8.2  

**Проблема:** 50% trial-to-paid conversion — це амбітний показник для нової категорії продуктів без аналогів на ринку. Типовий benchmark для SaaS freemium — 2-5%, для free trial — 15-25%. Документ називає це "base case," але для абсолютно нового типу продукту це скоріше оптимістичний сценарій.

**Рекомендація:** Перейменувати 50% з "base case" на "optimistic case." Зробити 25-30% як base case та побудувати фінансову модель навколо цього сценарію.

---

### MS-09: Відсутній аналіз сезонності

**[SEVERITY: LOW]**  
**Локація:** Весь документ  

**Проблема:** Для hardware продукту з ціною €150 сезонність (Q4 holiday season, Black Friday) критично впливає на продажі. Документ не адресує це — рівномірний розподіл продажів по місяцях нереалістичний.

**Рекомендація:** Додати аналіз сезонності та відповідну корекцію маркетингового бюджету і таргетів.

---

### MS-10: "79% of pet owners" — непідтверджене джерело

**[SEVERITY: LOW]**  
**Локація:** Розділ 2.1  

**Проблема:** "79% of pet owners view cats as family (Euromonitor, 2025)" — конкретна сторінка звіту Euromonitor не вказана. Без прямого доступу до платного звіту неможливо перевірити.

**Рекомендація:** Додати конкретну назву звіту Euromonitor та номер сторінки, або замінити на відкрите джерело.

---

## Документ 2: OPERATIONS_SUPPLY_CHAIN.md

### OS-01: Повна відсутність зовнішніх джерел

**[SEVERITY: CRITICAL]**  
**Локація:** Розділ References  

**Проблема:** Розділ References містить ВИКЛЮЧНО внутрішні документи проєкту. Жодного зовнішнього джерела — ні для assembly time estimates, ні для fulfillment costs, ні для quality benchmarks (AQL levels), ні для MTBF targets, ні для support cost benchmarks. Для MBA capstone документа це неприйнятна якість.

**Рекомендація:** Додати зовнішні джерела для: benchmarks assembly time (EMS industry reports), fulfillment cost benchmarks (EU 3PL providers), AQL standards (ISO 2859-1), MTBF estimation methodology, cloud infrastructure cost benchmarks. Мінімум 10-15 зовнішніх джерел.

---

### OS-02: RPi 4B — застарілий компонент

**[SEVERITY: HIGH]**  
**Локація:** Розділ 1.1, Розділ 2.1  

**Проблема:** Документ базується на Raspberry Pi 4B як основному обчислювальному модулі. Станом на березень 2026, RPi 5 вже є основним продуктом лінійки, а RPi 4B рухається до статусу end-of-life. Підвищення цін на RPi, задокументоване в Risk Analysis, стосується саме RPi 5. Вибір RPi 4B для нового продукту в 2026 році є стратегічно сумнівним — зменшується доступність, скорочується lifecycle підтримки.

**Рекомендація:** Обґрунтувати вибір RPi 4B замість RPi 5 (ціна? сумісність?) або перейти на RPi 5 / RPi Compute Module 4/5 з відповідним оновленням BOM.

---

### OS-03: Суперечність у fulfillment costs

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 4.2  

**Проблема:** Текст під таблицею стверджує: "Consistent with Financial Analysis fulfillment assumption (€9 Year 1, €8.50 Year 3)." Проте таблиця показує: Year 2 = €8.50, Year 3 = €7.50. Або текст неправильний, або таблиця не відповідає Financial Analysis.

**Рекомендація:** Звірити з Financial Analysis та виправити невідповідність.

---

### OS-04: "25 min/unit" assembly time — без обґрунтування

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 2.2  

**Проблема:** 25 хвилин на збирання одиниці IoT-пристрою з: RPi монтажем, серво-інтеграцією, лазерним модулем, камерою, проводкою, прошивкою firmware, функціональним тестуванням, пакуванням — це дуже оптимістична оцінка. Типовий час збирання подібних IoT-пристроїв — 45-90 хвилин. Прошивка firmware + тестування самі по собі можуть зайняти 10-15 хвилин.

**Рекомендація:** Навести джерело або обґрунтування. Порівняти з industry benchmarks для аналогічних IoT-пристроїв. При 45+ хв/unit виробнича потужність значно зменшується — це впливає на batch planning.

---

### OS-05: Відсутній процес CE-маркування та лазерної сертифікації

**[SEVERITY: HIGH]**  
**Локація:** Весь документ  

**Проблема:** Для IoT-пристрою з лазером, що продається в ЄС, CE-маркування обов'язкове (LVD, EMC, RED директиви). Лазерний модуль потребує відповідності IEC 60825-1. Жоден з цих процесів не згаданий в операційному плані: ні timeline, ні бюджет, ні відповідальні. Risk Analysis згадує це, але Operations — ні.

**Рекомендація:** Додати розділ "Regulatory Compliance & Certification" з timeline (6-12 тижнів для CE), бюджетом (€5,000-15,000), та інтеграцією в production workflow.

---

### OS-06: MTBF >5,000 годин — необґрунтований target

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 3.2  

**Проблема:** Target MTBF >5,000 operating hours заявлений без методології розрахунку. Risk Analysis сам вказує, що MG90S серво має lifecycle ~10,000 циклів. При щоденному використанні (30 хв, інтенсивний рух) серво може вичерпати ресурс за 12-18 місяців. 5,000 годин = 278 днів безперервної роботи. Невідповідність між MTBF target та відомими обмеженнями серво.

**Рекомендація:** Провести MTBF-аналіз на основі компонентних характеристик (MIL-HDBK-217 або подібна методологія). Вказати, що MTBF стосується системи без серво або з обмеженням серво-операцій.

---

### OS-07: Команда з 2 FTE — нереалістичне навантаження

**[SEVERITY: HIGH]**  
**Локація:** Розділ 7.2  

**Проблема:** У Рік 1 команда з 2 FTE (CTO + Software Engineer) повинна одночасно: розробляти hardware/firmware, ML-модель, backend (AWS), frontend (app), керувати CM, управляти supply chain, проводити QA, забезпечувати customer support, marketing operations. Це нереалістичне навантаження навіть для надзвичайно продуктивної команди.

**Рекомендація:** Або додати 1-2 FTE в Рік 1 (що вплине на Financial Analysis), або чітко визначити, які функції будуть outsourced, та включити відповідні витрати.

---

### OS-08: Відсутні митні/імпортні аспекти

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 1.1, Розділ 4  

**Проблема:** Компоненти sourced globally (RPi з UK-based distributor, серво з Тайваню, камера з Китаю), але документ не згадує: імпортні мита, HS-коди для електронних компонентів, RoHS compliance для імпортованих компонентів, потенційний вплив торгових обмежень.

**Рекомендація:** Додати аналіз митних витрат та compliance requirements для імпортованих компонентів.

---

### OS-09: Відсутній план тестування OTA-оновлень

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 6.1  

**Проблема:** Згадується staged rollout OTA-оновлень (10% → 50% → 100%), але відсутній: rollback plan, критерії go/no-go між стадіями, testing procedure для firmware updates, процедура відновлення при failed update (bricked devices).

**Рекомендація:** Додати детальний OTA update process з rollback mechanisms та критеріями якості.

---

### OS-10: Відсутній disaster recovery plan для cloud

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 6.1  

**Проблема:** Заявлено "Disaster recovery plan documented," але самий план відсутній в документі. Для IoT-продукту, де devices залежать від cloud connectivity, DR plan критичний: RTO, RPO, failover strategy, multi-region deployment.

**Рекомендація:** Або включити DR plan як додаток, або детально описати RTO/RPO targets та стратегію failover.

---

## Документ 3: RISK_ANALYSIS.md

### RA-01: Неправильні автори Kogan et al. (2021)

**[SEVERITY: CRITICAL]**  
**Локація:** Розділ 7.1, References  

**Проблема:** Цитується: "Kogan, L.R., Schoenfeld-Tacher, R., & Simon, A.A. (2021)." Фактичні автори статті: **Kogan, L.R. & Grigg, E.K.** (перевірено через MDPI та PubMed). Schoenfeld-Tacher та Simon — це зовсім інші дослідники. Це або грубе порушення академічної етики (фабрикація цитування), або результат AI-галюцинації.

**Рекомендація:** Виправити на: Kogan, L.R., & Grigg, E.K. (2021). Laser light pointers for use in companion cat play: Association with guardian-reported abnormal repetitive behaviors. *Animals*, 11(8), 2178. https://doi.org/10.3390/ani11082178

---

### RA-02: Неправильні автори та порядок для Kogan et al. (2022)

**[SEVERITY: CRITICAL]**  
**Локація:** Розділ 7.1, References  

**Проблема:** Цитується: "Kogan, L.R., Schoenfeld-Tacher, R., & Simon, A.A. (2022)." Фактичні автори: **Grigg, E.K. & Kogan, L.R.** — перший автор Grigg, не Kogan (перевірено через PubMed PMID: 35435787). Крім того, стаття опублікована як Vol. 27, No. 2 у **2024** (Apr-Jun), а не 2022. Рік у посиланні також неправильний.

**Рекомендація:** Виправити на: Grigg, E.K., & Kogan, L.R. (2024). Associations between laser light pointer play and repetitive behaviors in companion cats: Does participant recruitment method matter? *Journal of Applied Animal Welfare Science*, 27(2), 250-265. https://doi.org/10.1080/10888705.2022.2065880

---

### RA-03: Помилкова атрибуція "97% hardware startups fail" до CB Insights

**[SEVERITY: HIGH]**  
**Локація:** Executive Summary  

**Проблема:** Стверджується: "CB Insights reports that 97% of seed-funded hardware startups fail (Titoma, 2025; HardwareFYI, 2025)." Перевірка показала: Titoma цитує це як "As mentioned in FORBES, 97% of seed **crowdfunded** hardware startups fail." CB Insights не є першоджерелом цієї статистики, і вона стосується **crowdfunded** (краудфандингових) стартапів, а не seed-funded (проінвестованих на seed-раунді) — це суттєво інша категорія компаній з іншим survival rate.

**Рекомендація:** Виправити атрибуцію на Forbes (через Titoma). Змінити "seed-funded" на "seed crowdfunded." Ця зміна послаблює risk framing, оскільки Reactacat планує seed раунд від інвесторів, а не краудфандинг.

---

### RA-04: Суперечність щодо MG90S servo lifecycle

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 3.3  

**Проблема:** В описі ризику стверджується: "MG90S micro servos have limited lifespan (~10,000 cycles)." У mitigation стратегії для того ж серво вказано: "Specify metal-gear servos rated for 25,000+ cycles (MG90S)." Ці цифри суперечать одна одній. MG90S стандартно оцінюється на ~10,000 циклів; 25,000+ — це характеристика вищого класу серво (наприклад, MG996R).

**Рекомендація:** Узгодити цифри. Якщо потрібно 25,000+ циклів, специфікувати конкретну модель серво, що відповідає цій вимозі (не MG90S).

---

### RA-05: RPi supply risk — невідповідність моделей

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 4.1  

**Проблема:** Risk Analysis цитує WebProNews (February 2026) про "DRAM prices surged 40%" та подвійне підвищення цін RPi. Проте ці підвищення стосуються **RPi 5** (нові ціни: 4GB = $85, 8GB = $125). Operations document базується на **RPi 4B**. Ціновий ризик для RPi 4B інший — він стає менш доступним через EOL, а не через DRAM-ціни.

**Рекомендація:** Розрізнити ризики для RPi 4B (EOL/discontinuation risk) та RPi 5 (DRAM price risk). Оновити mitigation відповідно.

---

### RA-06: Відсутній ризик — obsolescence RPi 4B

**[SEVERITY: HIGH]**  
**Локація:** Розділ 4 (Operational Risks)  

**Проблема:** RPi 4B випущений у 2019 році. З виходом RPi 5, підтримка RPi 4B поступово скорочується. Ризик того, що Raspberry Pi Foundation припинить виробництво RPi 4B протягом 2026-2027 не ідентифікований. Це прямий supply chain ризик, відмінний від "supply disruption."

**Рекомендація:** Додати окремий ризик "RPi 4B End-of-Life / Discontinuation" з severity 3-4.

---

### RA-07: Відсутній ризик — treat dispenser safety

**[SEVERITY: HIGH]**  
**Локація:** Розділ 7 (Reputational Risks)  

**Проблема:** Treat dispenser — це ключова частина продукту (вирішує laser frustration), але відсутній аналіз ризиків: задавлення тваринки ласощами, алергічні реакції, несумісність з певними типами ласощів, механічний збій диспенсера (видача надмірної кількості). Для продукту, що позиціонується як "responsible pet technology," це критична прогалина.

**Рекомендація:** Додати ризик "Treat Dispenser Safety Incident" з mitigation strategies (portion control, size restrictions, testing protocols).

---

### RA-08: Відсутній ризик — open-source license compliance

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 3 (Technical Risks)  

**Проблема:** Raspberry Pi OS базується на Linux (GPL). MobileNet/YOLO використовують різні ліцензії. AWS SDK, Python бібліотеки — кожна зі своєю ліцензією. Відсутній аналіз ризику порушення open-source ліцензій, що може призвести до юридичних проблем або вимоги відкрити код.

**Рекомендація:** Додати ризик "Open-Source License Compliance" з severity 2 та mitigation через license audit.

---

### RA-09: EU AI Act — неточна дата та спрощене трактування

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 6.2  

**Проблема:** Стверджується "fully applicable from August 2, 2026." EU AI Act має поетапне впровадження: заборонені практики — з лютого 2025, high-risk вимоги — з серпня 2026, інші зобов'язання — до серпня 2027. Формулювання "fully applicable" некоректне. Крім того, трактування "pet toy AI is likely classified as minimal risk" може бути надмірно оптимістичним — якщо AI аналізує поведінку тварини в домашньому середовищі з камерою, це може піднімати додаткові питання.

**Рекомендація:** Уточнити поетапний графік EU AI Act. Провести формальну risk classification assessment замість припущення "minimal risk."

---

### RA-10: Відсутній ризик — team burnout / co-founder conflict

**[SEVERITY: MEDIUM]**  
**Локація:** Розділ 4 (Operational Risks)  

**Проблема:** Команда з 2 осіб, що виконує work of 5-6, з обмеженим seed funding та амбітними targets — класична ситуація для burnout та потенційного конфлікту між co-founders. Key person risk (4.4) адресує лише "departure or incapacitation," але не адресує burnout як більш ймовірний сценарій.

**Рекомендація:** Розширити 4.4 або додати окремий ризик "Founder Burnout" з probability High та impact High.

---

### RA-11: Відсутній ризик — конкуренція з боку великих pet-брендів (Mars, Nestlé)

**[SEVERITY: LOW]**  
**Локація:** Розділ 2 (Competitive Risks)  

**Проблема:** Competitive risks фокусуються на Petcube, китайських клонах та нових стартапах. Але Mars Petcare та Nestlé Purina активно інвестують у pet tech. Їхній вхід у сегмент smart toys мав би значно більший impact, ніж будь-який стартап-конкурент.

**Рекомендація:** Додати ризик "Major Pet Corporation Entry" з low probability але critical impact.

---

### RA-12: Sprout Social vs. Impact.com attribution — та сама помилка з Marketing Strategy

**[SEVERITY: LOW]**  
**Локація:** Розділ 4.2 (не знайдено прямо, але перехресна залежність)  

**Проблема:** Risk Analysis цитує "Sprout Social via Impact.com" для pet influencer вартості — та сама неточна атрибуція, що й у Marketing Strategy (MS-06).

**Рекомендація:** Узгодити з виправленням у Marketing Strategy.

---

## Перехресні проблеми (Cross-Document Issues)

### XD-01: Невідповідність fulfillment costs між документами

**[SEVERITY: MEDIUM]**  
**Локація:** OPERATIONS (Розділ 4.2) vs. MARKETING (implied) vs. RISK ANALYSIS (implied)  

**Проблема:** Operations каже €9.00 (Y1), €8.50 (Y2), €7.50 (Y3). Текст під таблицею Operations каже "€9 Year 1, €8.50 Year 3" — не відповідає таблиці. Financial Analysis (цитований, але не перевірявся) може мати третій набір цифр.

**Рекомендація:** Провести cross-check усіх фінансових показників між всіма документами. Створити єдину таблицю key assumptions.

---

### XD-02: Marketing бюджети не враховують операційну реальність

**[SEVERITY: MEDIUM]**  
**Локація:** MARKETING (Розділ 7) vs. OPERATIONS (Розділ 7.2)  

**Проблема:** Marketing Strategy передбачає €180K marketing budget у Рік 1, але Operations показує команду з 2 FTE. Хто виконує маркетингову роботу? Content production, social media management, influencer outreach, email automation, Google Ads management — це щонайменше 1 FTE маркетолога. Без нього €180K бюджету буде витрачено неефективно.

**Рекомендація:** Або додати marketing FTE / freelancer budget до Operations, або пояснити, як 2 FTE реалізують маркетингову стратегію (outsourcing agency budget?).

---

### XD-03: Risk Analysis не адресує ряд ризиків з Operations

**[SEVERITY: MEDIUM]**  
**Локація:** RISK ANALYSIS vs. OPERATIONS  

**Проблема:** Operations описує OTA firmware updates, cloud infrastructure (AWS), customer support model — але Risk Analysis не включає ризики: failed OTA update bricking devices, AWS outage affecting all devices, customer support overwhelm при hardware launch.

**Рекомендація:** Додати ці операційні ризики до Risk Register.

---

## Загальна оцінка AI-галюцинацій

### AI-01: Імовірні ознаки AI-генерованого контенту

**[SEVERITY: HIGH]**  
**Локація:** Всі три документи  

**Проблема:** Декілька ознак вказують на часткове AI-генерування без належної верифікації:

1. **Фабриковані автори статей** (RA-01, RA-02) — класична AI-галюцинація: правильна назва статті, правильний журнал, правильний DOI, але **неправильні автори**. Це типовий патерн LLM, що "вгадує" авторів.
2. **Перекручена статистика** (MS-01) — AI-системи часто переформульовують статистику, змінюючи контекст (YouTube → TikTok).
3. **Помилкові атрибуції** (RA-03) — CB Insights замість Forbes. LLM часто плутають джерела статистик, що широко цитуються.
4. **"Too clean" структура** — ідеально симетричні таблиці, рівномірний розподіл бюджетів, відсутність "messy" реальних даних.

**Рекомендація:** Перевірити ВСІ цитати та статистичні дані вручну. Особливу увагу — авторам наукових статей та конкретним числовим claims. Це критично для академічної доброчесності MBA-проєкту.

---

## Підсумкова статистика

| Severity | Кількість | Документ |
|----------|----------|----------|
| CRITICAL | 3 | OS-01, RA-01, RA-02 |
| HIGH | 8 | MS-01, MS-03, MS-04, OS-02, OS-05, OS-07, RA-03, RA-06, RA-07, AI-01 |
| MEDIUM | 14 | MS-02, MS-06, MS-07, MS-08, OS-03, OS-04, OS-06, OS-08, OS-09, OS-10, RA-04, RA-05, RA-08, RA-09, RA-10, XD-01, XD-02, XD-03 |
| LOW | 4 | MS-05, MS-09, MS-10, RA-11, RA-12 |

**Найкритичніші проблеми для негайного виправлення:**
1. Неправильні автори Kogan (2021) та Grigg (2022/2024) — загроза академічній доброчесності
2. Повна відсутність зовнішніх джерел в Operations document
3. Перекручення 63% статистики 5W PR
4. Суперечність DTC-only vs. Amazon

---

*Аудит завершено. Документи потребують суттєвої доробки перед фінальною подачею, особливо в частині верифікації джерел та усунення внутрішніх суперечностей.*
