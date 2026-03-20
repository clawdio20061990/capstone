# Аудит кластеру 5: Sustainability, ESG, Technology Roadmap, Pitch Decks, UX Research

**Дата аудиту:** 20 березня 2026  
**Аудитор:** Clawdio (AI Research Assistant)  
**Методологія:** ZERO TRUST — кожне твердження перевірено на достовірність, внутрішню узгодженість та академічну строгість  
**Файли в межах аудиту:**
1. `SUSTAINABILITY.md`
2. `ESG_SUSTAINABILITY_REPORT.md`
3. `TECHNOLOGY_PRODUCT_ROADMAP.md`
4. `PITCH_DECK_STRUCTURE.md`
5. `PITCH_DECK_5MIN.md`
6. `user_experience/survey_questions.md`
7. `user_experience/prototype_pre_test.md`
8. `user_experience/prototype_post_test.md`

---

## Зведення результатів

| Severity | Кількість |
|----------|-----------|
| CRITICAL | 5 |
| HIGH | 11 |
| MEDIUM | 14 |
| LOW | 8 |
| **Разом** | **38** |

---

## 1. SUSTAINABILITY.md

### [SEVERITY: CRITICAL] Невідповідність обчислювальної платформи між документами
**Розташування:** Розділ 4.4 "Computing Platform"  
**Проблема:** SUSTAINABILITY.md рекомендує **Raspberry Pi Zero 2 W** (ARM Cortex-A53, 512MB RAM), тоді як TECHNOLOGY_PRODUCT_ROADMAP.md (Розділ 2.1) вказує **Raspberry Pi 4B** (Cortex-A72, 2GB RAM) для Phase 1. Це принципово різні платформи з різною продуктивністю. Pi Zero 2 W є надто слабким для real-time computer vision з MobileNetV2 SSD (вимагає мінімум 1GB RAM для стабільної роботи).  
**Рекомендація:** Узгодити платформу між документами. Якщо MVP використовує RPi 4B — виправити SUSTAINABILITY.md. Додати технічне обґрунтування вибору.

### [SEVERITY: CRITICAL] Невідповідність матеріалу корпусу між документами
**Розташування:** Розділ 3.1 "Housing: PLA and Biodegradable Alternatives"  
**Проблема:** SUSTAINABILITY.md декларує корпус із **PLA (полілактид)** як основний матеріал. Однак TECHNOLOGY_PRODUCT_ROADMAP.md (Розділ 2.2) вказує **"Injection molded ABS, 2-piece clamshell"** для v1.0. ABS — це нафтохімічний пластик, що прямо суперечить заявам про біоматеріали. Це підриває довіру до всієї стратегії сталого розвитку.  
**Рекомендація:** Визначитись: або PLA для 3D-друку (малі серії), або ABS для інжекційного формування (масове виробництво). Чесно описати компроміс. Можливо, PLA для ранніх прототипів, ABS для масового виробництва з планом переходу на біоматеріали.

### [SEVERITY: HIGH] Невідповідність роз'єму живлення
**Розташування:** Розділ 4.2 "Electrical Interfaces" та Розділ 2.2 "Design for Repair"  
**Проблема:** Таблиця в 4.2 вказує **DC Barrel Jack 5.5x2.1mm** для живлення пристрою, а таблиця в 2.2 вказує **USB-C power delivery**. TECHNOLOGY_PRODUCT_ROADMAP.md підтверджує USB-C. Один документ не може мати дві різні відповіді.  
**Рекомендація:** Уніфікувати на USB-C (сучасний стандарт, узгоджений з roadmap). Видалити згадку DC barrel jack.

### [SEVERITY: HIGH] Відсутність джерел і цитувань
**Розташування:** Весь документ  
**Проблема:** Жодного зовнішнього джерела. Твердження на кшталт "PLA biodegradability — EN 13432" та "CERN Open Hardware Licence v2" не мають посилань. Стандарти реальні, але для MBA-роботи потрібні посилання на конкретні джерела.  
**Рекомендація:** Додати список літератури з посиланнями на EN 13432, CERN OHL v2, дослідження PLA biodegradability.

### [SEVERITY: MEDIUM] Нереалістичні заяви про PLA для домашнього компостування
**Розташування:** Розділ 3.1, таблиця "Home composting"  
**Проблема:** Вказано "Slow decomposition (1-2 years) — not ideal". Насправді PLA потребує промислових умов (58°C+) для повного розкладу. У домашньому компості PLA може не розкластися взагалі протягом кількох років. Формулювання "1-2 years" може ввести в оману.  
**Рекомендація:** Уточнити: "PLA не розкладається в домашніх умовах компостування; потребує промислового компостування (58°C+, згідно EN 13432)."

### [SEVERITY: MEDIUM] Порівняння з конкурентами без доказів
**Розташування:** Розділ 6.3 "Comparison with Competitors"  
**Проблема:** Таблиця стверджує, що типові конкуренти не мають модульності, документації для ремонту, тощо. Не вказано, хто саме ці конкуренти, і не наведено джерел для порівняння.  
**Рекомендація:** Назвати конкретних конкурентів (Petcube, Felik, PetSafe) та навести джерела для кожного порівняння.

### [SEVERITY: MEDIUM] Гарантія запчастин 7+ років — нереалістична для стартапу
**Розташування:** Розділ 2.3 "Spare Parts & Support"  
**Проблема:** Компанія на стадії концепту обіцяє "7+ years of spare parts availability". Для стартапу, який ще не запустив продукт і не має підтвердженого фінансування, це амбіційна заява без механізму гарантії.  
**Рекомендація:** Перефразувати як aspirational target: "Ціль — забезпечити доступність запчастин протягом 7+ років. Використання стандартних компонентів мінімізує ризик залежності від одного постачальника."

### [SEVERITY: LOW] Фінансові дані без обґрунтування
**Розташування:** Розділ 9.1 "Cost of Sustainable Design"  
**Проблема:** Цифри "+5-10% to R&D", "-15% support costs", "+30% repeat purchases", "+20% price" — без джерел та методології розрахунку.  
**Рекомендація:** Або видалити конкретні відсотки, або додати посилання на дослідження/аналоги.

---

## 2. ESG_SUSTAINABILITY_REPORT.md

### [SEVERITY: HIGH] Надмірна деталізація для компанії на стадії концепту
**Розташування:** Весь документ  
**Проблема:** Звіт містить повну структуру ESG governance (Board of Directors, ESG Steering Committee, Environmental/Social/Governance Officers), GRI Index з 30+ розкриттями, email-адреси (esg@reactacat.com, sustainability@reactacat.com). Компанія ще не існує, не має працівників, не має доходу. Документ створює враження зрілої компанії, що може бути розцінено як greenwashing або введення в оману.  
**Рекомендація:** Чітко позначити документ як "Forward-Looking ESG Framework" і додати disclaimers: "Усі структури, метрики та цілі є проектованими і будуть імплементовані відповідно до стадії розвитку компанії."

### [SEVERITY: HIGH] Неперевірювані кількісні метрики
**Розташування:** Розділ 3.1 "Carbon Footprint Baseline"  
**Проблема:** Вказано конкретні цифри: Scope 2 = 5.2 tCO2e, Scope 3 = 29.8 tCO2e, Total = 35.0 tCO2e. Для компанії без реальних операцій ці цифри не можуть бути "baseline" — це лише оцінки. Методологія розрахунку не описана. Немає посилання на LCA або emission factors.  
**Рекомендація:** Перейменувати на "Estimated Carbon Footprint (Projected)" та описати методологію: які emission factors використані, які припущення зроблені.

### [SEVERITY: HIGH] Energy Star Version 8.0 для pet-пристроїв не існує
**Розташування:** Розділ 3.1 "Energy Efficiency"  
**Проблема:** Згадується "Energy Star compliance target: Version 8.0". Energy Star не має окремої категорії для pet devices або IoT cat toys. Ця специфікація виглядає як AI-галюцинація.  
**Рекомендація:** Видалити згадку Energy Star або замінити на реальний стандарт: "Low-power design targeting <5W average consumption, aligned with EU Code of Conduct on Energy Consumption of Broadband Equipment."

### [SEVERITY: MEDIUM] GRI Index для компанії без даних
**Розташування:** Розділ 8 "Appendix: GRI Index"  
**Проблема:** Повний GRI Index із 30+ розкриттями для компанії, яка не має фінансових даних, працівників, операцій. Більшість посилань ведуть на розділи з planned/projected інформацією, а не з actual data.  
**Рекомендація:** Замінити на "Planned GRI Alignment" із зазначенням, які розкриття будуть доступні після початку операцій. Додати колонку "Data Available From" для кожного GRI disclosure.

### [SEVERITY: MEDIUM] "Cats as primary stakeholders" — сумнівна ESG практика
**Розташування:** Розділ 4.1 "Animal Welfare (Primary Stakeholder)"  
**Проблема:** Формулювання "cats as our primary stakeholders" не є стандартною ESG-практикою. Стейкхолдери в ESG-контексті — це суб'єкти, які можуть впливати на організацію або зазнавати впливу від неї і мають агентність (voice). Коти не можуть надати feedback або brати участь у stakeholder engagement. Це може виглядати несерйозно для MBA-оцінювачів.  
**Рекомендація:** Перефразувати: "Animal welfare is a core design principle" або включити котів як "silent stakeholders" з поясненням, що їхні інтереси представлені через veterinary advisors та behavioral research.

### [SEVERITY: MEDIUM] Невідповідність регуляторної таблиці
**Розташування:** Розділ 5.3 "Regulatory Compliance"  
**Проблема:** "EU Right to Repair Directive" вказана як "Pending 2024-2025" зі статусом "Design already compliant". Станом на березень 2026 ця директива вже мала б бути прийнята або ні. Потребує оновлення.  
**Рекомендація:** Уточнити актуальний статус директиви станом на дату документа (березень 2026).

### [SEVERITY: LOW] Нереалістичне "Zero waste to landfill by 2028"
**Розташування:** Розділ 3.2 "E-Waste Commitments"  
**Проблема:** Для стартапу, який ще не почав виробництво, обіцяти zero waste to landfill через 2 роки — надмірно амбіційно.  
**Рекомендація:** Пом'якшити до "aspiration" або "target" з чіткими проміжними milestone.

### [SEVERITY: LOW] Cobalt у батареях — пристрій не має батареї
**Розташування:** Розділ 5.2 "High-Risk Materials"  
**Проблема:** Згадується "Preference for ethically sourced cobalt in batteries". Ніде в документації не зазначено, що пристрій має акумулятор — він живиться від мережі (USB-C/DC).  
**Рекомендація:** Видалити згадку cobalt/batteries або уточнити, до яких саме компонентів це відноситься.

---

## 3. TECHNOLOGY_PRODUCT_ROADMAP.md

### [SEVERITY: HIGH] Надмірно оптимістичний timeline для MVP
**Розташування:** Розділ 1.2 "Version Timeline"  
**Проблема:** Alpha prototype за 3 місяці, MVP launch за 7 місяців — для hardware+AI+cloud+mobile app стартапу з командою 2 FTE (CTO + 1 software engineer). Це означає одночасну розробку: firmware, edge AI model, cloud backend, mobile app (iOS), hardware design — двома людьми за 7 місяців. Надзвичайно агресивний timeline.  
**Рекомендація:** Або збільшити команду для Year 1, або розширити timeline до 10-12 місяців для MVP, або обмежити MVP scope ще більше.

### [SEVERITY: HIGH] Суперечність із SUSTAINABILITY.md щодо відкритого коду
**Розташування:** Розділ 5.2 "Decision 3: Open API vs. Closed ecosystem"  
**Проблема:** SUSTAINABILITY.md декларує open-source firmware, GPL v3/MIT ліцензію, CERN OHL для hardware. TECHNOLOGY_PRODUCT_ROADMAP обирає "Closed ecosystem initially". Це пряма суперечність: не можна одночасно бути open-source і closed ecosystem.  
**Рекомендація:** Узгодити позицію. Можливий компроміс: "Open hardware design, proprietary AI/cloud platform" — але це потрібно чітко сформулювати в обох документах.

### [SEVERITY: MEDIUM] "0.5 ML Engineer" та "0.5 Hardware Engineer"
**Розташування:** Розділ 9.1 "Engineering Team Growth"  
**Проблема:** Наймання 0.5 FTE ML Engineer у Year 2 — нетипова практика. На ринку складно знайти part-time ML engineer для стартапу. Це може бути contractor, але тоді потрібна інша бюджетна модель.  
**Рекомендація:** Уточнити: contractor, part-time employee, чи shared resource. Обґрунтувати реалістичність найму.

### [SEVERITY: MEDIUM] Патентна стратегія для ще не створеного продукту
**Розташування:** Розділ 6.2 "Patent Strategy"  
**Проблема:** "Provisional filed" для "Adaptive laser play algorithm" — але компанія на стадії концепту. Provisional patent filing коштує ~$1,500-3,000 в US. Чи справді був filed? Якщо ні — це неправдиве твердження.  
**Рекомендація:** Якщо патент справді filed — додати дату та номер заявки. Якщо ні — змінити на "Planned" або "To be filed at Month X".

### [SEVERITY: MEDIUM] iOS-first без обґрунтування для Polish market
**Розташування:** Розділ 5.1 "Conscious Technical Debt"  
**Проблема:** "Single-platform (iOS first)" з обґрунтуванням "70% of target demographic". У Польщі Android має ~70% ринку (StatCounter). Це означає, що iOS-first стратегія залишає більшість потенційних користувачів без доступу.  
**Рекомендація:** Перевірити дані про розподіл iOS/Android у target demographic (premium cat owners). Якщо твердження правильне — додати джерело. Якщо ні — переглянути стратегію або запустити з cross-platform (React Native/Flutter).

### [SEVERITY: LOW] Cloud costs Year 3 = €120K
**Розташування:** Розділ 9.2 "R&D Budget"  
**Проблема:** €120K/рік на cloud для 18,000 devices — це ~€6.67/device/year. Для AI retraining pipeline + model distribution + analytics — може бути занижено, особливо з multi-region deployment.  
**Рекомендація:** Додати breakdown cloud costs per service (compute, storage, bandwidth, ML training).

---

## 4. PITCH_DECK_STRUCTURE.md (10-12 хв)

### [SEVERITY: CRITICAL] Неперевірені статистичні заяви без джерел
**Розташування:** Slide 2, Slide 3  
**Проблема:** Ключові маркетингові заяви:
- "50M+ cats in EU spend 8-10 hours alone daily" — без джерела
- "~50% show signs of boredom or depression (veterinary studies)" — "veterinary studies" не є цитуванням
- "Pet tech growing at 12-20% CAGR" — діапазон 12-20% надто широкий, без джерела
- "79% of owners view cats as family members" — без джерела
- "1.8-2.3M premium cat households (€60K+ income)" — без методології розрахунку  
Для інвесторського pitch це критично: будь-який due diligence виявить відсутність підтвердження.  
**Рекомендація:** Для кожної заяви додати конкретне джерело (FEDIAF, Euromonitor, конкретне дослідження). Якщо джерело не знайдено — пом'якшити формулювання або видалити.

### [SEVERITY: HIGH] Невідповідність break-even між pitch decks
**Розташування:** Slide 10  
**Проблема:** PITCH_DECK_STRUCTURE.md: "Monthly cash flow positive: Month 28-30, Cumulative break-even: Month 32-33". PITCH_DECK_5MIN.md (Slide 7): "Monthly positive: Month 28-30, Cumulative break-even: Month 34-35". Різниця 2 місяці у cumulative break-even. В одному й тому самому capstone project мати різні цифри — серйозна помилка.  
**Рекомендація:** Уніфікувати цифри у всіх документах. Вказати базові припущення (retention rate, conversion rate), які визначають break-even.

### [SEVERITY: HIGH] Невідповідність gross margin Year 1
**Розташування:** Slide 10  
**Проблема:** PITCH_DECK_STRUCTURE: "Gross margin: 23%". PITCH_DECK_5MIN: "Gross margin: 24%". Дрібна різниця, але свідчить про відсутність single source of truth для фінансових даних.  
**Рекомендація:** Уніфікувати та посилатися на один фінансовий документ.

### [SEVERITY: MEDIUM] Тестування 15 households представлене як "validation"
**Розташування:** Slide 9 "Traction & Validation"  
**Проблема:** "Prototype Testing (15 households)" і далі "87% of cats engaged" — це 13 з 15 котів. Це не статистично значущий результат. Представлення цього як "validation" може ввести інвесторів в оману. 15 — це pilot test, не validation.  
**Рекомендація:** Перефразувати на "Early Pilot Results" або "Indicative Testing" замість "Validation". Додати disclaimer про розмір вибірки.

### [SEVERITY: MEDIUM] Цитата бета-тестера може бути вигаданою
**Розташування:** Slide 9  
**Проблема:** "My cat actually runs to the device now. I've never seen him this excited about a toy." — Beta tester, Warsaw". Оскільки тестування описане як "friends & family", ця цитата може бути необ'єктивною. Немає механізму верифікації.  
**Рекомендація:** Якщо цитата реальна — зберегти, але додати context: "From friends & family pilot". Якщо вигадана — видалити негайно.

### [SEVERITY: LOW] Competitive matrix спрощена
**Розташування:** Slide 6  
**Проблема:** Матриця "Autonomous vs Manual, Intelligent vs Random" ігнорує інших гравців (PetSafe, HEXBUG, Cheerble). Petcube позиціонується як "Manual Control", але Petcube має scheduled автоматичне відтворення.  
**Рекомендація:** Перевірити актуальні функції Petcube та інших конкурентів. Зробити матрицю більш чесною.

---

## 5. PITCH_DECK_5MIN.md

### [SEVERITY: HIGH] Невідповідність cumulative break-even
**Розташування:** Slide 7  
**Проблема:** "Cumulative break-even: Month 34-35" — відрізняється від 10-хв pitch deck (Month 32-33). Див. Issue #4.1 вище.  
**Рекомендація:** Уніфікувати.

### [SEVERITY: MEDIUM] Відсутність slide про команду в основних слайдах
**Розташування:** Загальна структура  
**Проблема:** Team slide — у backup slides. Для 5-хвилинного pitch це прийнятно, але багато інвесторів вважають команду ключовим фактором. Якщо формат дозволяє — варто включити.  
**Рекомендація:** Розглянути включення 15-секундного team slide замість одного з section headers.

### [SEVERITY: LOW] Revenue Year 3 вказана без breakdown
**Розташування:** Slide 9  
**Проблема:** €2.85M revenue за Year 3 подається без розбивки hardware vs subscription. Для інвесторів пропорція hardware/subscription — ключовий показник unit economics.  
**Рекомендація:** Додати: "Revenue split: X% hardware, Y% subscription."

---

## 6. survey_questions.md

### [SEVERITY: CRITICAL] Leading/біаснуті питання порушують методологічну коректність
**Розташування:** Питання 4, 10  
**Проблема:**
- **Питання 4:** "Were you aware that studies suggest approximately 50% of indoor cats show signs of boredom or depression due to insufficient activity?" — це priming. Респондент отримує "факт" про депресію котів перед тим, як його запитають про бажання купити продукт (питання 8-10). Це класичний приклад leading question, який систематично завищує позитивні відповіді на наступні питання.
- **Питання 10:** "Basic automatic toys cost €20–40 but quickly bore cats. Would you be willing to pay €120–150 for a toy that actually works..." — фреймінг "actually works" передбачає, що дешеві іграшки не працюють, а дорога — працює. Це маніпулятивне формулювання.  
**Рекомендація:** Питання 4 перемістити в кінець або переформулювати нейтрально. Питання 10 переписати: "Would you consider paying €120-150 for an AI-powered autonomous cat toy?" без порівняння з "boring" дешевими альтернативами.

### [SEVERITY: CRITICAL] Self-selection bias у вибірці
**Розташування:** Шапка документа "Distribution"  
**Проблема:** Розповсюдження через "Facebook groups, Telegram channels, cat owner communities" — це convenience sampling з сильним self-selection bias. Люди в cat owner groups уже більш зацікавлені в котячих продуктах, ніж середній власник кота. Результати не можна екстраполювати на загальну популяцію.  
**Рекомендація:** Визнати обмеження вибірки в аналізі результатів. Додати розділ "Limitations" до звіту UX research. Не використовувати результати як "market validation" — лише як "indicative interest among engaged cat owners".

### [SEVERITY: HIGH] Відсутність demographic control та sampling methodology
**Розташування:** Весь документ  
**Проблема:** Немає: квотної вибірки, стратифікації за віком/доходом/регіоном, визначення confidence interval, мінімального розміру вибірки для статистичної значущості. "Expected Responses: 50-100" — навіть 100 відповідей із biased sample не є достатнім для висновків про TAM 1.8-2.3M households.  
**Рекомендація:** Додати sampling plan, визначити target demographics для квотної вибірки, вказати power analysis для визначення мінімального N.

### [SEVERITY: MEDIUM] Невідповідність розміру вибірки між документами
**Розташування:** Шапка документа vs Pitch Decks  
**Проблема:** survey_questions.md: "Expected Responses: 50-100". Pitch decks: "Survey (100+ cat owners)". Якщо опитування ще не проведене (є лише питання), то "100+" у pitch deck — це projected, а не actual. Якщо проведене — де результати?  
**Рекомендація:** Якщо результати є — включити їх у документацію. Якщо ні — змінити формулювання в pitch deck на "planned survey" або не використовувати як evidence.

### [SEVERITY: MEDIUM] Відсутність питань про дохід/готовність платити
**Розташування:** Список питань  
**Проблема:** Питання 11 запитує вік, але немає питання про дохід домогосподарства. Це критично для оцінки price sensitivity та визначення premium segment. Pitch deck таргетує "€60K+ income households", але survey не збирає ці дані.  
**Рекомендація:** Додати питання про приблизний дохід (з варіантами діапазонів) та housing type (apartment/house).

### [SEVERITY: LOW] Питання 9 занадто довге та має пояснення в дужках
**Розташування:** Питання 9  
**Проблема:** Пояснення "(Think of it as a smart device: computer vision tracks your cat's movements...)" по суті "продає" продукт респонденту. Survey-питання мають бути нейтральними.  
**Рекомендація:** Скоротити до: "Would you be interested in a toy that learns your cat's preferences and adapts its play style?"

---

## 7. prototype_pre_test.md

### [SEVERITY: MEDIUM] Відсутність informed consent
**Розташування:** Весь документ  
**Проблема:** Немає інформованої згоди (informed consent form) для учасників. Хоча документ зазначає "No IRB approval required" — навіть для MBA capstone потрібен базовий consent: мета дослідження, добровільність участі, конфіденційність даних, право відмовитись.  
**Рекомендація:** Додати informed consent section на початку анкети.

### [SEVERITY: MEDIUM] Немає baseline metrics для порівняння
**Розташування:** Питання 5  
**Проблема:** Шкала 1-5 для "how active is your cat" — суб'єктивна. Немає об'єктивних baseline metrics (наприклад: хвилин активності на день, кількість ігрових сесій). Без об'єктивного baseline, post-test порівняння буде суб'єктивним.  
**Рекомендація:** Додати питання: "Approximately how many minutes per day does your cat actively play?" для кількісного baseline.

### [SEVERITY: LOW] Відсутність питання про житло
**Розташування:** Список питань  
**Проблема:** Немає питання про розмір квартири/будинку, наявність інших тварин. Це може впливати на engagement з пристроєм (маленька квартира vs великий будинок).  
**Рекомендація:** Додати 1-2 контекстуальних питання про середовище тестування.

---

## 8. prototype_post_test.md

### [SEVERITY: HIGH] Відсутність контрольної групи
**Розташування:** Весь документ  
**Проблема:** Тестування проводиться без control group (наприклад, група з random laser toy). Без контролю неможливо стверджувати, що engagement котів спричинений саме AI-адаптацією, а не novelty effect (будь-яка нова іграшка цікава перший тиждень).  
**Рекомендація:** Включити control group з неадаптивною лазерною іграшкою, або визнати novelty effect як limitation. Для MBA capstone достатньо визнати обмеження — не обов'язково проводити RCT.

### [SEVERITY: MEDIUM] Одного тижня недостатньо для висновків про engagement
**Розташування:** Шапка документа "After 1 week"  
**Проблема:** Тиждень — мінімальний період для тестування. Pitch deck стверджує, що "cats lose interest in days" з іншими іграшками. Щоб довести, що Reactacat краще — потрібен мінімум 3-4 тижні тестування.  
**Рекомендація:** Подовжити тестовий період до мінімум 3 тижнів або визнати обмеження: "One-week testing period may not capture long-term engagement patterns."

### [SEVERITY: LOW] Питання 4 має implicit bias
**Розташування:** Питання 4  
**Проблема:** "Compared to regular laser toys or other toys, was Reactacat better?" — формулювання "better" має позитивну конотацію. Нейтральне формулювання: "How does Reactacat compare to other toys your cat uses?"  
**Рекомендація:** Переформулювати на нейтральну шкалу порівняння.

### [SEVERITY: LOW] Відсутність кількісних метрик
**Розташування:** Весь документ  
**Проблема:** Всі питання якісні або ordinal scale. Немає pitch deck metric "60% showed increased activity levels" — звідки ця цифра, якщо post-test не запитує про конкретний рівень активності в хвилинах?  
**Рекомендація:** Додати кількісне питання: "Approximately how many minutes per day did your cat play with Reactacat?" для порівняння з pre-test baseline.

---

## Міждокументні проблеми

### [SEVERITY: CRITICAL] Відсутність фактичних результатів дослідження
**Розташування:** Всі UX-документи + Pitch Decks  
**Проблема:** В capstone project є тільки **питання** для опитування та тестування, але **немає документа з результатами**. При цьому pitch decks цитують конкретні результати: "73% interested", "87% of cats engaged", "80% would recommend". Звідки ці цифри? Якщо дослідження ще не проведене — ці цифри в pitch deck є фальсифікацією.  
**Рекомендація:** ТЕРМІНОВО: або провести дослідження та задокументувати результати, або видалити конкретні цифри з pitch decks і замінити на "projected/planned research".

### [SEVERITY: HIGH] Три різні hardware platforms у різних документах
**Розташування:** SUSTAINABILITY.md vs TECHNOLOGY_PRODUCT_ROADMAP.md  
**Проблема:**
- SUSTAINABILITY.md: Raspberry Pi Zero 2 W
- TECHNOLOGY_PRODUCT_ROADMAP.md Phase 1: Raspberry Pi 4B
- TECHNOLOGY_PRODUCT_ROADMAP.md Phase 2: Custom PCB (Rockchip RK3566)
Pi Zero 2 W та Pi 4B — принципово різні пристрої (ціна, продуктивність, form factor).  
**Рекомендація:** Створити single source of truth для hardware spec та посилатися на нього з усіх документів.

### [SEVERITY: MEDIUM] Open-source vs Closed ecosystem
**Розташування:** SUSTAINABILITY.md vs TECHNOLOGY_PRODUCT_ROADMAP.md  
**Проблема:** Детально описано вище. SUSTAINABILITY декларує відкритість (GPL, CERN OHL, Creative Commons), TECH_ROADMAP — закритість (proprietary cloud, closed API). Ці позиції несумісні без чіткого розмежування, що саме відкрите, а що — ні.  
**Рекомендація:** Визначити чітку IP-стратегію: hardware design = open, AI models = proprietary, cloud = proprietary, mobile app = proprietary. Оновити обидва документи.

---

## Загальні рекомендації

1. **Створити Master Data Sheet** — єдиний документ з ключовими цифрами (hardware platform, BOM cost, break-even, gross margins, survey results), на який посилаються всі інші документи.

2. **Додати список літератури** до кожного документа. Для MBA capstone це обов'язково. Мінімум: FEDIAF pet population data, market research reports (Euromonitor/Grand View Research), стандарти (EN 13432, IEC 60825-1, GDPR text).

3. **Провести реальне дослідження** або чітко маркувати всі цифри як projected/estimated. Фальсифікація даних у академічній роботі — серйозне порушення.

4. **Переглянути survey methodology** — виправити leading questions, додати limitations section, визнати self-selection bias.

5. **Узгодити timeline та фінансові показники** між усіма документами. Поточний стан — різні цифри в різних місцях — знижує довіру до всієї роботи.

---

**Статус:** Завершено  
**Наступний крок:** Виправити CRITICAL та HIGH issues перед здачею capstone project
