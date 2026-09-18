# دوز سه‌بعدی ایرانی 🇮🇷 | Persian 3D Dooz

<div align="center">

**بازی سنتی ایرانی دوز — بازآفرینی دیجیتال مدرن با فرش دستباف، ترنج و بته‌جقه**

*A premium bilingual (FA/EN) 3D reinterpretation of the traditional Iranian Dooz board game.*

![HTML5](https://img.shields.io/badge/HTML5-single--file-E34F26?logo=html5&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-0.160-000000?logo=three.js&logoColor=white)
![Bilingual](https://img.shields.io/badge/lang-فارسی_%7C_English-d4af37)
![No Build](https://img.shields.io/badge/build-none_needed-1fb6a6)
![License](https://img.shields.io/badge/license-MIT-blue)

[🇮🇷 فارسی](#-معرفی) • [🇬🇧 English](#-english-overview)

</div>

---

## 📖 معرفی

**دوز سه‌بعدی ایرانی** یک بازی سه‌بعدی دوزبانه (فارسی/انگلیسی) دونفره است که روی یک فایل `index.html` اجرا می‌شود — بدون نیاز به نصب، بیلد یا سرور.

بازی دو حالت کاملاً مجزا دارد:

| حالت | توضیح |
|------|-------|
| 🟫 **دوز سه‌تایی** (3-Piece Dooz) | صفحه کلاسیک ۳×۳ تا ۶×۶، سه مهره در یک ردیف |
| 🟨 **دوز دوازده‌تایی** (12-Piece Dooz) | صفحه سنتی ۲۴ نقطه‌ای (سه مربع تودرتو)، ۱۲ مهره برای هر بازیکن، با فاز نشستن و حرکت |

### ✨ ویژگی‌های کلیدی

- 🎮 **دو حالت بازی** با منوی اصلی و تعویض زنده حالت
- 🌍 **کاملاً دوزبانه** — فارسی (راست‌به‌چپ) و انگلیسی (چپ‌به‌راست) با ذخیره خودکار زبان
- 🧶 **هویت بصری ایرانی** — بافت فرش procedural، **ترنج** مرکزی، نوار **بته‌جقه**، گل شاه‌عباسی، لچک، قاب چوب گردویی و تزئینات طلایی
- 🎲 **مهره‌های سه‌بعدی دست‌ساز** — ✕ طلایی (فلز صیقلی + نگین فیروزه) و ○ فیروزه‌ای (سرامیک لعابدار + حلقه طلا)
- 💡 نورپردازی سینمایی، سایه نرم، ذرات غبار طلایی، دوربین مداری تطبیقی
- 🔊 افکت‌های صوتی سنتزشده (WebAudio) — بدون هیچ فایل صوتی
- 📊 امتیاز جداگانه برای هر حالت + ذخیره در `localStorage`
- 📱 تمام‌صفحه و ریسپانسیو — دسکتاپ، تبلت و موبایل
- ⚙️ تنظیمات کامل: حالت، اندازه زمین، شرط برد، قانون پرش، صدا، انیمیشن، راهنما، زبان

---

## 🚀 اجرا

### روش ۱ — باز کردن مستقیم (پیشنهادی)

روی فایل دابل‌کلیک کنید:

```
dooz/index.html
```

> برای لود کتابخانه Three.js و فونت، اتصال اینترنت لازم است.

### روش ۲ — سرور محلی

```bash
cd dooz
python -m http.server 8000
# سپس در مرورگر: http://localhost:8000
```

### روش ۳ — انتشار در GitHub Pages

۱. محتویات پوشه را در یک ریپوی گیت‌هاب بریزید (فایل اصلی باید `index.html` در ریشه باشد).
۲. از بخش `Settings → Pages` گزینه **Deploy from a branch** و شاخه `main` را انتخاب کنید.
۳. بازی روی آدرس `https://<username>.github.io/<repo>/` در دسترس قرار می‌گیرد.

---

## 🟫 حالت ۱ — دوز سه‌تایی

همان دوز/تیک‌تک‌تو کلاسیک با پوسته فرش ایرانی:

- 📐 اندازه زمین: **۳×۳، ۴×۴، ۵×۵، ۶×۶** (بافت فرش با تراکم متناسب هر سایز بازتولید می‌شود، نه کش‌آمدن ساده)
- 🎚️ درجه سختی: آسان (۳×۳ برد ۳تایی) • متوسط (۴×۴ برد ۴تایی) • سخت (۵×۵ برد ۴تایی) • حرفه‌ای (۶×۶ برد ۵تایی) — اندازه و شرط برد مستقل هم قابل انتخاب‌اند
- 🏆 تشخیص خودکار برد (افقی/عمودی/قطری)، مساوی، هایلایت ترکیب برنده با پرتو نورانی
- 📷 دوربین تطبیقی: هرچه زمین بزرگ‌تر، نما خودکار بازتر

---

## 🟨 حالت ۲ — دوز دوازده‌تایی

بازسازی وفادار دوز سنتی ایرانی روی **گراف ۲۴ گرهی**:

```
■ □ □ □ □ □ ■      ← مربع بیرونی (۸ نقطه)
□ ■ □ □ □ ■ □
□ □ ■ □ ■ □ □      ← مربع میانی (۸ نقطه)
□ □ □ ■ □ □ □ ── اتصالات شعاعی وسط‌ضلع‌ها
□ □ ■ □ ■ □ □      ← مربع درونی (۸ نقطه)
□ ■ □ □ □ ■ □
■ □ □ □ □ □ ■      ＋ اتصالات قطری گوشه‌ها
```

- 🔢 دقیقاً **۲۴ نقطه** قابل بازی (۳ مربع × ۸ نقطه) — **بدون گره مرکزی**
- 🔗 **۴۰ یال**: محیط هر سه مربع + ۴ مسیر شعاعی + ۴ مسیر قطری
- 🎯 **۲۰ خط دوز معتبر** (۱۲ ضلع + ۴ شعاعی + ۴ قطری) — تشخیص فقط روی خطوط واقعی توپولوژی
- **فاز ۱ — نشستن:** هر بازیکن ۱۲ مهره به‌نوبت روی نقاط خالی می‌نشاند
- **تشکیل دوز → حذف:** سه مهره پشت سر هم = دوز؛ انیمیشن جشن + حذف یک مهره حریف (مهره‌های داخل دوز حریف تا وقتی مهره آزاد دارد محافظت می‌شوند)
- **فاز ۲ — حرکت:** شروع خودکار پس از پایان نشستن؛ حرکت فقط به نقطه خالیِ **متصل**
- 🕊️ **قانون پرش مهره** (قابل تنظیم): بازیکنِ دارای دقیقاً ۳ مهره می‌تواند به هر نقطه خالی بپرد
- ☠️ پایان: بازیکنی که به **۲ مهره** برسد یا **حرکت قانونی** نداشته باشد می‌بازد

---

## ⚙️ تنظیمات

| تنظیم | گزینه‌ها |
|-------|----------|
| حالت بازی | دوز سه‌تایی / دوز دوازده‌تایی |
| اندازه زمین (حالت ۱) | ۳×۳ تا ۶×۶ |
| شرط برد (حالت ۱) | ۳ / ۴ / ۵ تایی (نامعتبرها خودکار غیرفعال) |
| قانون پرش (حالت ۲) | روشن / خاموش |
| صدا، انیمیشن، نمایش خودکار راهنما، زبان | روشن / خاموش |
| امتیاز | صفر کردن (جداگانه برای هر حالت) |

تغییر حالت/اندازه/شرط برد یک دست تازه شروع می‌کند؛ **امتیازها حفظ می‌شوند**.

---

## 🛠️ تکنولوژی‌ها

| لایه | ابزار |
|------|-------|
| رندر سه‌بعدی | [Three.js 0.160](https://threejs.org) (CDN، ماژول ES) |
| بافت‌ها | procedural روی `<canvas>` — بدون هیچ فایل تصویری |
| صدا | WebAudio API سنتزشده — بدون هیچ فایل صوتی |
| فونت | وزیرمتن (Vazirmatn) از Google Fonts |
| ذخیره‌سازی | `localStorage` (زبان، حالت، تنظیمات، امتیازها) |
| ساختار | تک‌فایل `index.html` — بدون بیلد، بدون وابستگی نصبی |

### ساختار پروژه

```
dooz/
├── index.html      # 🎮 بازی کامل دوحالته (نسخه اصلی)
├── README.md       # همین فایل
└── others/
    └── index.html  # نسخه قدیمی تک‌حالته (آرشیو)
```

### کلیدهای localStorage

| کلید | کاربرد |
|------|--------|
| `dooz_lang` | زبان (`fa`/`en`) |
| `dooz_mode` | حالت (`3`/`12`) |
| `dooz_cfg` | اندازه/برد/سختی حالت سه‌تایی |
| `dooz_fly` | قانون پرش |
| `dooz_anim` / `dooz_showr` / `dooz_sound` | انیمیشن / راهنما / صدا |
| `dooz_score` | امتیاز هر دو حالت + شماره دست |

---

## 🧪 تست توپولوژی

منطق گراف صفحه ۱۲تایی (۲۴ گره، ۴۰ یال، ۲۰ میل، اتصال کامل، هم‌خطی هندسی، قانون محافظت میل، همسایگی حرکت، شرط پایان) قابل اعتبارسنجی خودکار است — همه ۲۱ تست پاس می‌شوند.

---

## 🗺️ نقشه راه

- [ ] حالت تک‌نفره با هوش مصنوعی (minimax برای ۳×۳، heuristic برای ۱۲تایی)
- [ ] ثبت رکورد و تاریخچه دست‌ها
- [ ] تایمر نوبت و حالت تورنمنت
- [ ] تم روشن/تیره و پوسته‌های فرش بیشتر (تبریز، کاشان، قم)
- [ ] PWA (نصب و اجرای آفلاین کامل)

---

## 🤝 مشارکت

۱. ریپو را Fork کنید
۲. برنچ بسازید (`git checkout -b feature/xyz`)
۳. کامیت و Pull Request بفرستید

چون پروژه تک‌فایل است، لطفاً تغییرها را کوچک و تست‌شده نگه دارید.

## 📄 لایسنس

MIT — آزاد برای استفاده، تغییر و انتشار. 🙏 اگر از پروژه استفاده کردید، یک ستاره ⭐ فراموش نشود!

---

## 🇬🇧 English Overview

**Persian 3D Dooz** — a premium bilingual (Persian/English, RTL/LTR) two-player 3D board game in a single `index.html`. No install, no build, no server needed — just open the file (internet required for Three.js CDN + font).

**Two modes:**
1. **3-Piece Dooz** — classic Tic-Tac-Toe on 3×3–6×6 Persian-carpet boards with scalable win conditions (3/4/5 in a row), difficulty presets, draw detection, and an adaptive cinematic camera.
2. **12-Piece Dooz** — authentic traditional Iranian Dooz on an exact **24-node graph** (three nested squares × 8 points, no center node, 40 edges: perimeters + radial midpoints + diagonal corners, 20 valid mill lines). Two phases: **placement** (12 pieces each) → **movement** along graph edges, with mill formation → opponent-piece removal (protected-mill rule), optional **Flying Rule** (jump anywhere with exactly 3 pieces), losing at 2 pieces or no legal moves.

**Highlights:** fully procedural Persian carpet textures (Toranj medallion, Boteh Jegheh band, Shah Abbasi flowers), handcrafted gold/turquoise 3D pieces, synthesized WebAudio SFX (no audio files), per-mode scoreboards persisted in `localStorage`, fullscreen floating HUD, responsive down to mobile, extended settings (mode, board size, win length, flying, sound, animations, rules, language).

**Run:** double-click `index.html`, or `python -m http.server 8000`, or deploy to GitHub Pages (`Settings → Pages → Deploy from a branch`).

**License:** MIT.
</div>
