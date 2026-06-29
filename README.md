# Prytulok

Сайт для притулку тварин. Спрощує усиновлення і керування базою тварин.

**→ [Research: конкуренти, бенчмарк, патерни, висновки](https://htmlpreview.github.io/?https://github.com/yuliabokova/prytulok/blob/main/research/research.html)**

---

## Структура репо

| Папка | Що тут |
|---|---|
| [`research/`](./research/) | Аналіз аудиторії, конкурентів, інсайти. Скриншоти — у `research/screens/` |
| [`wireframes/`](./wireframes/) | Вайрфрейми всіх екранів |
| [`concept/`](./concept/) | Мудборди, концептуальний напрям, варіанти стилю |
| [`tokens/`](./tokens/) | Дизайн-токени: кольори, типографіка, spacing, радіуси |
| [`components/`](./components/) | Специфікації окремих компонентів |
| [`design-system/`](./design-system/) | Документація дизайн-системи, принципи, патерни |
| [`handoff/`](./handoff/) | Специфікації для розробки: сторінки, стани, assets |

---

## Продукт

Prytulok знімає бар'єр між людиною, що хоче взяти тварину, і притулком. Замість телефонного дзвінка — зручний каталог, картка тварини з усіма деталями і форма заявки прямо на сайті. Для волонтерів — проста адмін-панель без технічного бар'єру.

### Публічна частина

- **Каталог** — сітка тварин з фільтрами: вид, вік, розмір, стать, сумісність (діти / інші тварини / квартира)
- **Картка тварини** — фото-галерея, опис характеру від волонтера, медичні дані (щеплення, стерилізація), мітки сумісності, статус
- **Форма заявки** — ім'я, телефон, email, коротко про себе; підтвердження одразу на пошту
- **Як допомогти** — контакти притулку + форма для волонтерів

### Адмін-панель (`/admin`)

- Додавання і редагування тварин із завантаженням фото
- Зміна статусу одним кліком
- Перегляд заявок із контактами заявника

### Статуси тварин

| Статус | Значення |
|---|---|
| `available` | Шукає дім |
| `pending` | Є заявка |
| `adopted` | Знайшов дім |

---

## Люди

Чотири персони на основі user research (червень 2025). Деталі з підтвердженнями — у [personas.md](./research/personas.md) і [jtbd.md](./research/jtbd.md).

| Персона | Ситуація | Роль |
|---|---|---|
| Маша | Хоче першу тварину — прийшла з Instagram, ще не певна | **PRIMARY** |
| Олег і Катя | Хоче першу тварину — вже вирішили, шукають по критеріях | Secondary |
| Діана | Вже є кішка — головний страх: конфлікт між тваринами | Secondary |
| Ірина | Не може взяти — хоче допомогти як волонтер або донатор | Secondary |

**Main job:** отримати відповідь «моя / не моя» без дзвінків і невизначеності.

**Топ-3 jobs для MVP:**
- **R2** Named caretaker — «Волонтер Оля знає Мурку 3 тижні» замість шаблонного «ласкава і грайлива»
- **R4** Підтвердження після форми — хто і коли зв'яжеться; UA-ринок не закриває
- **R1** Compatibility-мітки на картці — квартира / діти / інші тварини прямо в сітці

→ [▸ Personas & JTBD HTML](https://htmlpreview.github.io/?https://github.com/yuliabokova/prytulok/blob/main/research/personas.html)

---

## Стек

Next.js · TypeScript · Tailwind · Supabase · Resend · Vercel

---

## Запуск

```bash
npm install
npm run dev
```

Створи `.env.local` і заповни змінні (перелік у [CLAUDE.md](./CLAUDE.md#environment-variables)).

Детальний контекст для розробки — у [CLAUDE.md](./CLAUDE.md).

---

## Прогрес

| Етап | Статус |
|---|---|
| Research | [▸ Research HTML](https://htmlpreview.github.io/?https://github.com/yuliabokova/prytulok/blob/main/research/research.html) · [▸ Personas & JTBD HTML](https://htmlpreview.github.io/?https://github.com/yuliabokova/prytulok/blob/main/research/personas.html) · [Зведений research](./research/research.md) · [Конкурентний аналіз](./research/competitive-analysis.md) · [Аналіз довіри до профілю](./research/trust-profile-analysis.md) · [Персони](./research/personas.md) · [JTBD](./research/jtbd.md) |
| Wireframes | — |
| Concept | — |
| Tokens | [Чернетка](./tokens/tokens.md) |
| Components | — |
| Design system | — |
| Handoff | — |
| Development | — |
