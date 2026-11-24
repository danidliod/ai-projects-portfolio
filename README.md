# פרויקטים שבניתי עם AI · AI-Built Projects Portfolio

> **טיוטה** — לפני פרסום: לעבור על [`PUBLISHING-CHECKLIST.md`](PUBLISHING-CHECKLIST.md) ולהוסיף מדיה לפי [`MEDIA-CHECKLIST.md`](MEDIA-CHECKLIST.md).

ריכוז של מוצרים שתכננתי ובניתי בשנה האחרונה, מהרעיון ועד פריסה לאוויר, כש-AI משמש גם **כחלק מהמוצר** (סוכנים, סיווג, חילוץ מידע, כתיבת תוכן) וגם **ככלי הפיתוח** (Claude Code, סוכנים שמריצים בדיקות, פריסה ותיקון תקלות).

הקוד עצמו נשאר בריפוזיטוריז פרטיים. כאן יש הסבר על כל פרויקט: איזו בעיה הוא פותר, איך הוא עובד, ארכיטקטורה, טכנולוגיות, פריסה, מצב נוכחי, תמונות וסרטונים. אפשר לתת גישה לקוד לפי בקשה.

**In English:** a portfolio of products I designed and shipped over the last year with AI, both as a product capability (agents, classification, extraction, content generation) and as the engineering workflow (Claude Code agents that build, test, deploy and self-heal). Source code stays private; each page explains the problem, how it works, architecture, stack, deployment and status. Code walkthroughs available on request.

---

## הפרויקטים המרכזיים

| | פרויקט | במשפט אחד | AI במוצר | מצב |
|---|---|---|---|---|
| 1 | [**Chief-of-Staff AI**](projects/01-chief-of-staff-agent.md) | סוכן אישי לעסק: פגישות, מיילים, יומן, CRM ומשימות, דרך טלגרם וקונסולת ניהול | Gemini (הבנה, סיווג, ראייה, סיכום) + תיקון תקלות אוטומטי ע"י Claude Code | 🟢 בייצור, שימוש יומיומי |
| 2 | [**השנה שלנו**](projects/02-family-year-planner.md) | כל שנת המשפחה מראש: לוח משרד החינוך, חגים, ימי הולדת, חידושי מסמכים, קליטה מווטסאפ וצילום | חילוץ אירועים מטקסט/תמונה/קול כהצעות שאדם מאשר | 🟢 חי למשפחה ראשונה |
| 3 | [**מגדל הערפל**](projects/03-tower-of-mist-game.md) | משחק הרפתקאות ולמידה לילדים בעברית, אנגלית וספרדית, 2D ו-3D | נבנה כמעט כולו בעבודה עם סוכני קוד, כולל בוטים שמשחקים ובודקים כל שלב | 🟢 אתר חי · 🟡 בדרך לחנויות |
| 4 | [**Growth Engine**](projects/04-growth-engine.md) | מנוע קמפיינים לארגונים: תוכן שנכתב, נבדק ומשתפר לבד, תחת שליטת איש השיווק | LLM כותב וריאנטים, מעקות בטיחות דטרמיניסטיים, Thompson sampling | 🟡 ליבה + אפליקציה מוכנות, לפני ספקים חיים |
| 5 | [**App Growth Kit**](projects/05-app-growth-kit.md) | ערכת קידום אורגני לאפליקציה שמורצת ע"י Claude Code כל שעה | סוכן שמפעיל דפדפן: רילס, פניות, מדידה, יומן החלטות | 🟢 בשימוש · [קוד פתוח](https://github.com/danidliod/app-growth-kit) |
| 6 | [**imhungry**](projects/06-imhungry.md) | "מה אפשר לאכול עכשיו?" — עוזר אוכל משפחתי, וואטסאפ-תחילה + ווב | Gemini לנרמול וסיווג מוצרים (לא לאלרגנים) | 🟡 MVP |
| 7 | [**לצמוח מבפנים**](projects/07-growing-from-within.md) | PWA ואפליקציה לליווי אנשים בצומת מקצועית: אבחון, דוח, בוט מלווה, התאמת קו"ח | בוט שיחה עם 5 הקשרים, דוחות אבחון, התאמת קורות חיים למשרה | 🟡 בפיתוח מתקדם |
| 8 | [**Mosquito Radar**](projects/08-mosquito-radar.md) | אפליקציית iOS כנה ליתושים: מזהה את רחש הכנפיים בלילה ומעירה | DSP על המכשיר בלבד (בלי ענן); נבנה וכויל עם סוכן קוד | 🟡 TestFlight |
| 9 | [**HitDeck**](projects/09-hitdeck.md) | אפליקציית iOS שסורקת קלפי משחק מוזיקה ומנגנת את השיר ב-Apple Music | — (פענוח שרשרת נתונים ציבורית) | 🟢 ב-App Store |

**עוד פרויקטים קטנים** — [בסוף העמוד](#עוד-פרויקטים).

---

## איך אני עובד/ת עם AI

| שלב | מה AI עושה | מה נשאר אצלי |
|---|---|---|
| מחקר ואפיון | סקירת שוק, מתחרים, היתכנות טכנית ורגולטורית (למשל: למה אפליקציות "דוחה יתושים" הן הונאה מתועדת) | בחירת הבעיה, הגדרת "מה נחשב הצלחה" |
| תכנון | מסמכי החלטות (ADR), roadmap, מפת סיכונים | אישור כיוון, סדר עדיפויות |
| בנייה | Claude Code כותב קוד בסבבים קטנים על ענפים, עם תצוגה מקדימה לכל סבב | "תעלה" — שום דבר לא עולה לייצור בלי אישור |
| בדיקות | בדיקות יחידה, Playwright, בוטים שמשחקים את המשחק, בדיקות RLS על Postgres אמיתי | הגדרת מה בודקים ולמה |
| תפעול | זיהוי תקלה → סוכן מנתח, מתקן, בודק, פורס ומדווח בטלגרם | אישור החלטות בלתי הפיכות |

**עקרונות שחוזרים בכל הפרויקטים**
- **אדם באמצע:** AI מציע, אדם מאשר (אירועים ביומן, הודעות שיווק, פעולות CRM).
- **רק טענות אמיתיות:** מעקות בטיחות שחוסמים מספר, מחיר או דחיפות שלא קיימים בעובדות.
- **פרטיות כברירת מחדל:** עיבוד על המכשיר כשאפשר, לוגים בלי תוכן, סודות רק בצד השרת.
- **מדידה של מה שחשוב:** משלמים ולא לייקים, קבוצת ביקורת ולא רק המרות.

## טכנולוגיות (רוחבי)

**AI:** Claude (Claude Code, Claude Code GitHub Action), Google Gemini, Whisper · **Web:** Next.js, React, TypeScript, Tailwind, Vite · **Mobile:** SwiftUI, Capacitor (iOS/Android), Flutter, Java (Android service) · **Data:** Supabase/Postgres + RLS, Cloudflare D1, Firebase · **Automation:** n8n · **Infra:** Vercel, Cloudflare Workers, AWS EC2 + Docker Compose, GitHub Actions · **Integrations:** Telegram Bot API, WhatsApp (Meta Cloud API), Gmail/Calendar/Tasks/Drive, Resend, Twilio, StoreKit 2, MusicKit · **Graphics:** Three.js, Phaser 4 · **Testing:** Vitest, Playwright, XCTest

---

## עוד פרויקטים

| פרויקט | מה זה | טכנולוגיה | מצב |
|---|---|---|---|
| **שומר השקט** | אפליקציה שמזהה נביחות של הכלב (טביעת קול ב-24 פסי תדר), משמיעה קול קטיעה ומתגמלת שקט. [אתר](https://shomer-sheket.vercel.app) | PWA + שירות רקע נייטיב באנדרואיד (Java), APK נבנה ונחתם ב-GitHub Actions | 🟢 חי |
| **chatdigest** | סיכומים יומיים של קבוצות ווטסאפ ישר מהמאגר המקומי ב-Mac, כולל תמלול הודעות קוליות, וגישה מהטלפון | Python, SQLite, whisper.cpp, Claude CLI, Tailscale, Supabase Edge Function (טקסט מוצפן בלבד) | 🟢 בשימוש אישי |
| **מונה חשמלי לרכב** | אפליקציה לניהול מוני טעינה לרכבים חשמליים + מערכת בקאופיס | Flutter, Firebase, Brevo | 🟡 |

---

## יצירת קשר

[קישור לפרופיל לינקדאין] · [מייל] · גישה לקוד או הדגמה חיה — לפי בקשה.
