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

**Публічна частина** — каталог тварин з фільтрами (вид, вік, розмір, стать), картка тварини з фото-галереєю і описом, форма заявки на усиновлення, сторінка як допомогти (контакти + форма для волонтерів).

**Адмін-панель** (`/admin`) — додавання і редагування тварин, зміна статусу, перегляд заявок.

### Статуси тварин

| Статус | Значення |
|---|---|
| `available` | Шукає дім |
| `pending` | Є заявка |
| `adopted` | Знайшов дім |

---

## Стек

Next.js · TypeScript · Tailwind · Supabase · Resend · Vercel

---

## Запуск

```bash
npm install
cp .env.example .env.local   # заповнити змінні середовища
npm run dev
```

Детальний контекст для розробки — у [CLAUDE.md](./CLAUDE.md).

---

## Прогрес

| Етап | Статус |
|---|---|
| Research | [▸ HTML](https://htmlpreview.github.io/?https://github.com/yuliabokova/prytulok/blob/main/research/research.html) · [Зведений research](./research/research.md) · [Конкурентний аналіз](./research/competitive-analysis.md) · [Аналіз довіри до профілю](./research/trust-profile-analysis.md) |
| Wireframes | — |
| Concept | — |
| Tokens | Чернетка |
| Components | — |
| Design system | — |
| Handoff | — |
| Development | — |
