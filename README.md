# פרויקטים שבניתי עם AI · AI-Built Projects Portfolio

ריכוז של מוצרים שתכננתי ובניתי בשנה האחרונה, מהרעיון ועד פריסה לאוויר. AI משמש בהם בשני תפקידים: **כחלק מהמוצר** (סוכנים, סיווג, חילוץ מידע, כתיבת תוכן) וגם **ככלי הפיתוח** (Claude Code, סוכנים שמריצים בדיקות, פריסה ותיקון תקלות).

הקוד עצמו נשאר בריפוזיטוריז פרטיים. כאן יש הסבר על כל פרויקט: איזו בעיה הוא פותר, איך הוא עובד, ארכיטקטורה, טכנולוגיות, פריסה, מצב נוכחי, תמונות וסרטונים. **גישה לקוד או הדגמה חיה — לפי בקשה.**

**In English:** a portfolio of products I designed and shipped over the last year with AI — both as a product capability (agents, classification, extraction, content generation) and as the engineering workflow (Claude Code agents that build, test, deploy and self-heal). Source code stays private; each page covers the problem, how it works, architecture, stack, deployment and status. Code walkthroughs and live demos on request.

![מגדל הערפל](assets/migdal-haarafel/teaser.gif)

---

## במספרים

| | |
|---|---|
| **מוצרים** | 9 מרכזיים + 3 קטנים — רובם חיים באוויר או בשימוש יומיומי |
| **קומיטים** | ~3,600 |
| **Pull requests** | ~2,500 — כל שינוי בענף משלו, עם בדיקות ותצוגה מקדימה |
| **קבצי בדיקות** | ~1,300 (יחידה, רכיבים, E2E, evals, בוטים שמשחקים) |
| **פלטפורמות** | ווב/PWA, iOS (SwiftUI + Capacitor), Android, Apple Watch, WebXR, טלגרם, וואטסאפ |

---

## הפרויקטים המרכזיים

| | פרויקט | במשפט אחד | AI במוצר | מצב |
|---|---|---|---|---|
| 1 | [**מגדל הערפל**](projects/01-tower-of-mist-game.md) | משחק הרפתקאות ולמידה לילדים בשלוש שפות, 2D, 3D ו-VR | נבנה בעבודה עם סוכני קוד, כולל בוטים שמשחקים ובודקים כל שלב | 🟢 [חי באתר](https://migdal-haarafel.vercel.app) · 🟡 בדרך לחנויות |
| 2 | [**Chief-of-Staff AI**](projects/02-chief-of-staff-agent.md) | סוכן אישי לעסק: פגישות, מיילים, יומן, CRM, קבלות ומשימות, דרך טלגרם וקונסולה | Gemini (הבנה, סיווג, ראייה, סיכום) + תיקון תקלות אוטומטי ע"י Claude Code | 🟢 בייצור, שימוש יומיומי |
| 3 | [**השנה שלנו**](projects/03-family-year-planner.md) | כל שנת המשפחה מראש, עם קליטה אוטומטית מקבוצות ווטסאפ | Claude מחלץ מועמדים, קוד מחליט מה נכנס | 🟢 חי למשפחה ראשונה |
| 4 | [**Growth Engine**](projects/04-growth-engine.md) | מערכת שיווק לארגונים: קמפיינים, דפי נחיתה ו-A/B, רשתות חברתיות | LLM כותב וריאנטים, מעקות דטרמיניסטיים, Thompson sampling | 🟢 באוויר בהדגמה · 🟡 לפני ספקים חיים |
| 5 | [**App Growth Kit**](projects/05-app-growth-kit.md) | ערכת קידום אורגני לאפליקציה שמורצת ע"י Claude Code כל שעה | סוכן שמפעיל דפדפן: רילס, פניות, מדידה, יומן החלטות | 🟢 [קוד פתוח](https://github.com/danidliod/app-growth-kit) |
| 6 | [**imhungry**](projects/06-imhungry.md) | "מה אפשר לאכול עכשיו?" — חוסכת כסף על ידי צמצום בזבוז מזון | Gemini: מתכונים מהמזווה, קבלות, חיי מדף, רשימות | 🟢 [חי](https://imhungry.appnest.fyi) · iOS, Android, Watch |
| 7 | [**לצמוח מבפנים**](projects/07-growing-from-within.md) | ליווי בצומת מקצועית: אבחון, דוח, בוט מלווה, קו"ח, נטוורקינג וראיונות | בוט ב-5 הקשרים, דוחות, התאמת קו"ח, טיוטות פנייה | 🟡 בפיתוח מתקדם |
| 8 | [**Mosquito Radar**](projects/08-mosquito-radar.md) | אפליקציית iOS כנה ליתושים: מזהה את רחש הכנפיים בלילה ומעירה | DSP על המכשיר בלבד; נבנה וכויל עם סוכן קוד | 🟡 TestFlight |
| 9 | [**HitDeck**](projects/09-hitdeck.md) | סורקת קלפי משחק מוזיקה ומנגנת את השיר ב-Apple Music | — (פענוח שרשרת נתונים ציבורית) | 🟢 [ב-App Store](https://apps.apple.com/app/id6801653040) |

### עוד פרויקטים

| פרויקט | מה זה | טכנולוגיה | מצב |
|---|---|---|---|
| **שומר השקט** | מזהה נביחות של הכלב (טביעת קול ב-24 פסי תדר), משמיע קול קטיעה ומתגמל שקט, עם יומן נביחות. [אתר](https://shomer-sheket.vercel.app) | PWA + שירות רקע נייטיב באנדרואיד (Java); APK נבנה ונחתם ב-GitHub Actions | 🟢 חי |
| **chatdigest** | סיכומים יומיים של קבוצות ווטסאפ ישר מהמאגר המקומי ב-Mac, כולל תמלול הודעות קוליות, וגישה מהטלפון | Python, SQLite, whisper.cpp, Claude CLI, Tailscale, Supabase Edge Function (טקסט מוצפן בלבד) | 🟢 בשימוש אישי |
| **מונה חשמלי לרכב** | אפליקציה לניהול מוני טעינה לרכבים חשמליים + מערכת בקאופיס | Flutter, Firebase, Brevo | 🟡 |

---

## איך אני עובד/ת עם AI

| שלב | מה AI עושה | מה נשאר אצלי |
|---|---|---|
| מחקר ואפיון | סקירת שוק ומתחרים, היתכנות טכנית ורגולטורית (למשל: למה אפליקציות "דוחה יתושים" הן הונאה מתועדת) | בחירת הבעיה, הגדרת "מה נחשב הצלחה" |
| תכנון | מסמכי החלטות (ADR), roadmap, מודל איום, מפת סיכונים | אישור כיוון, סדר עדיפויות |
| בנייה | Claude Code כותב קוד בסבבים קטנים על ענפים, עם תצוגה מקדימה לכל סבב; סוכנים ייעודיים למימוש, תיקון באגים, סקירת קוד ושחרור גרסאות | "תעלה" — שום דבר לא עולה לייצור בלי אישור |
| בדיקות | בדיקות יחידה, Playwright, evals לחילוץ, בוטים שמשחקים את המשחק, בדיקות RLS על Postgres אמיתי | הגדרת מה בודקים ולמה |
| תפעול | זיהוי תקלה → סוכן מנתח, מתקן, בודק, פורס ומדווח בטלגרם | אישור החלטות בלתי הפיכות |

**עקרונות שחוזרים בכל הפרויקטים**
- **אדם באמצע:** AI מציע, אדם מאשר — אירועים ביומן, הודעות שיווק, פעולות CRM. מה שאוטומטי מסומן וניתן לביטול.
- **המודל לא מחליט:** הוא מחזיר מועמדים, וקוד דטרמיניסטי מחליט מה עובר.
- **רק טענות אמיתיות:** מעקות שחוסמים מספר, מחיר או דחיפות שלא קיימים בעובדות.
- **פרטיות כברירת מחדל:** עיבוד על המכשיר כשאפשר, לוגים בלי תוכן, סודות רק בצד השרת, הגנה מיוחדת על מידע של ילדים.
- **מדידה של מה שחשוב:** משלמים ולא לייקים, קבוצת ביקורת ולא רק המרות, evals ולא תחושה.
- **באג שחוזר שלוש פעמים מקבל בדיקה אוטומטית**, לא עוד פסקה בתיעוד.

## טכנולוגיות (רוחבי)

**AI:** Claude (Claude Code, Claude Code GitHub Action, Claude API), Google Gemini (כולל Vertex AI), Whisper · **Web:** Next.js, React 19, TypeScript, Tailwind, Vite · **Mobile:** SwiftUI, Capacitor (iOS/Android), Flutter, Java · **Games & graphics:** Phaser 4, Three.js, WebXR, Web Audio · **Data:** Supabase/Postgres + RLS, Cloudflare D1, Firebase · **Automation:** n8n · **Infra:** Vercel, Cloudflare Workers, AWS EC2 + Docker Compose, GitHub Actions · **Integrations:** Telegram, WhatsApp (Meta Cloud API + מכשיר מקושר), Gmail/Calendar/Tasks/Drive, Resend, Twilio, StoreKit 2, MusicKit, RevenueCat · **Testing:** Vitest, Playwright, XCTest, evals

---

ליצירת קשר — דרך הפרופיל בלינקדאין. גישה לקוד או הדגמה חיה — לפי בקשה.
