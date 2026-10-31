# Arcwell: an interior design studio site with Formgong forms

**Live demo:** https://arcwell.formgong.com · Download: the [latest release](https://github.com/formgong/arcwell-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/arcwell-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Farcwell-template&project-name=arcwell&repository-name=arcwell)

Each button copies the site to your GitHub and publishes it. Then replace every `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Сайт студії дизайну інтер'єру з формами Формгонг

A one-page template for an interior design or renovation studio, in a single `index.html`. The demo studio, Arcwell, its address, prices and projects are fictional.

- **Header.** A thin top bar with the phone number, a centred logo with the menu below it, and social icons on the right. Over the photos it is transparent. Once you scroll it turns white and gets shorter. On phones it becomes a menu button.
- **Hero.** Three full-screen photos that cross-fade every 5 seconds, with dots to pick one. A large uppercase title, a line of text and two buttons drop in from the top.
- **About.** A centred title and two paragraphs.
- **Services.** A black band and three columns (Design project, Renovation & supervision, Furnishing), each with a list and an outline button.
- **Order.** A short list beside a three-field order form.
- **Why us.** Six reasons with icons.
- **Quote.** A full questionnaire (name, email, phone, city, type, area, renovation, notes) beside a photo.
- **Estimate.** A light blue band that explains the renovation estimate, with a sample-estimate form.
- **Recent projects.** Eight photos in grey that turn to colour on hover, and a wide black button.
- **FAQ.** Five questions on a timeline of black icon circles.
- **Contact.** The studio address and hours, then a call-back form with a privacy note.

The four forms are order, quote, sample estimate and call back. Each sends a hidden `request` field, so you can tell them apart in one inbox. "Powered by Formgong" sits under the quote and call-back forms.

## English

**Set up the forms**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace every `fk_your_access_key` with that key. There are four forms; use find and replace.
3. A form shows thanks only when Formgong answers `success: true`. If the answer is anything else, it shows the error and keeps what was typed.

**Edit**

- Colours and widths are at the top of the styles: `--blue` for the estimate band, `--soft` and `--line` for the fields, and `--wrap` for the content width.
- The logo is one SVG `<symbol id="mark">` near the top of `<body>`. The favicon has its own copy in `<link rel="icon">`.
- The hero changes photos every 5000 ms (`setInterval` in the script). With `prefers-reduced-motion: reduce` it stays on the first photo and nothing fades in.

**Images.** The twelve photos were generated for this template with ChatGPT image generation (OpenAI) and saved as WebP, about 1.3 MB in all. You may use them in your own site. Replace them with your own projects, keeping the file names.

The "Powered by Formgong" links point to `https://formgong.com/review-page/fk_your_access_key`, so the same find and replace covers them. Once your key is in, the first click from your published site makes your own public review page on Formgong, where clients read and leave reviews, and every later click opens it. Switch the page off in Formgong (Reviews → your site → Settings) or change those links.

## Українська

Односторінковий шаблон для студії дизайну інтер'єру або ремонту. Студія Arcwell, адреса, ціни й проєкти вигадані.

На сторінці по черзі:

- прозора шапка, що під час прокрутки стає білою;
- три фото на весь екран, що змінюються кожні 5 секунд;
- блок «про нас», чорна смуга і три колонки послуг;
- форма замовлення, шість переваг;
- анкета для розрахунку вартості;
- блакитний блок про кошторис ремонту з формою;
- галерея, що стає кольоровою під курсором;
- питання на таймлайні;
- адреса й форма зворотного дзвінка.

**Налаштування.** Створіть форму в кабінеті Formgong і замініть усі `fk_your_access_key` у `index.html` на свій ключ (форм чотири). Кожна форма надсилає приховане поле `request`. Подяка з'являється лише тоді, коли Formgong відповідає `success: true`.

**Зображення:** дванадцять фото згенеровано для цього шаблону в ChatGPT (OpenAI) і збережено у WebP, разом близько 1,3 МБ. Їх можна використовувати на своєму сайті.

MIT license.

Посилання «Powered by Formgong» ведуть на `https://formgong.com/review-page/fk_your_access_key`, тож та сама заміна ключа оновить і їх. Коли ключ стоїть, перший перехід з вашого опублікованого сайту створює вашу публічну сторінку відгуків на Formgong, де клієнти читають і залишають відгуки; далі посилання відкриває її. Вимкнути сторінку можна у Formgong (Відгуки → ваш сайт → Налаштування) або змінити ці посилання.
