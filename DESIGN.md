---
name: לפי הכריכה
description: אפליקציית web אינטראקטיבית לגילוי כריכת ספר אישית
colors:
  ink: "#111111"
  signal-yellow: "#fff200"
  paper: "#FFFAF1"
  gray-mid: "#d1d3d4"
  gray-warm: "#9A9288"
  gray-dark: "#343434"
typography:
  display:
    fontFamily: "'Rapida', serif"
    fontSize: "clamp(28px, 3.5vw, 48px)"
    fontWeight: 300
    lineHeight: 1.2
    letterSpacing: "4px"
  body:
    fontFamily: "'Arbel', sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "'Arbel', sans-serif"
    fontSize: "13px"
    letterSpacing: "0.05em"
rounded:
  none: "0px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "32px"
  lg: "48px"
components:
  button-primary:
    backgroundColor: "{colors.signal-yellow}"
    textColor: "{colors.ink}"
    rounded: "{rounded.none}"
    padding: "10px 28px"
  button-primary-hover:
    backgroundColor: "transparent"
    textColor: "{colors.signal-yellow}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.signal-yellow}"
    rounded: "{rounded.none}"
    padding: "10px 28px"
---

# Design System: לפי הכריכה

## 1. Overview

**Creative North Star: "הסטודיו השחור"**

מערכת עיצוב ישראלית, נועזת, לא מתנצלת. הרקע השחור הוא לא בחירת ברירת מחדל — הוא הצהרה: אנחנו עובדים כאן, זה סטודיו, לא חנות. הצהוב (`#fff200`) הוא האות, לא הקישוט. כל מסך הוא רגע עיצובי בפני עצמו — לא שלב בטופס.

הטיפוגרפיה בעברית היא מרכזית, לא אחרי-מחשבה. Rapida לשאלות, Arbel לממשק — שניהם גופנים עם אישיות ישראלית ברורה. שמונה גופנים נוספים מוצגים בתוך הספרים עצמם, כחלק מחוויית הגילוי.

המערכת דוחה: פורמליות בירוקרטית, כלי עיצוב גנריים (Canva/Figma), e-commerce סטנדרטי. אם זה נראה כמו טופס ממשלתי, זה נכשל.

**Key Characteristics:**
- שחור מוחלט כרקע ראשי — לא אפור כהה, לא navy
- צהוב (`#fff200`) כקול יחיד ונועז — לא accent עדין
- פינות חדות בכל מקום — אפס עיגולים
- RTL מלא, עברית first
- אנימציות מכוונות — כל תנועה מספרת משהו

## 2. Colors: פלטת הסטודיו

פלטה של שני קולות: שחור שקט כבסיס, צהוב חריף כאות.

### Primary
- **Signal Yellow** (`#fff200`): הצהוב של שלטי האזהרה ופסי הכביש. משמש לכפתורים, כותרות שאלות, אלמנטי ניווט. נוכחותו נדירה מספיק שכל הופעה שלו חדה.

### Neutral
- **Studio Black** (`#111111`): רקע ברוב המסכים. לא שחור מוחלט — קצת נשימה. משמש גם כ-`--cream` בקוד (שמות המשתנים הפוכים בכוונה).
- **Paper White** (`#FFFAF1`): צבע הטקסט הראשי על רקע שחור. גם `--black` בקוד. לבן חמימות קלה.
- **Mid Gray** (`#d1d3d4`): טקסט משני, רקע טקסט ברקע מסך 2. מושתק אבל קריא.
- **Warm Gray** (`#9A9288`): גוונים נייטרלים בפלטות הצבע של מסך 6.
- **Dark Gray** (`#343434`): מקום שצריך כהה אבל לא שחור — משמש בפלטות הנייטרליות.

### Named Rules

**The One Signal Rule.** הצהוב מופיע על ≤20% מכל מסך. רוב המסך שחור. הצהוב מרוויח את הקריאה ממרחוק בגלל שהוא נדיר.

**The No Warm Tint Rule.** הרקע הוא `#111111` — לא `#1a1a1a` עם גוון חם, לא navy. שחור קריר וישיר.

## 3. Typography: גופנים עם עמדה

**Display Font:** Rapida (serif עברי — serif קלאסי, weight 300)
**Body Font:** Arbel (sans-serif עברי — נקי, קריא, ישראלי)
**Book Fonts:** OHSalmanHabaka, FlamingoBM, IndexDL, HadasBau, NarkisBlockStudio, Liebling, HaimG — שמונה גופנים עבריים המשמשים בתצוגת הכריכות בלבד

**Character:** Rapida מביאה כובד ספרותי לשאלות — כאילו הדפסת קטלוג גלריה. Arbel שומרת על הממשק קריא ולא מתחרה. לא עושים שימוש בגופני Google Fonts — כל הגופנים עבריים ומוטמעים.

### Hierarchy

- **Display** (300, 32–48px, line-height 1.2, letter-spacing 4px): שאלות המסכים ("איזה ז'אנר הכי קורא לך?"). Rapida. קו-הפעולה של כל מסך.
- **Headline** (300, 24px, letter-spacing 4px): כותרות משניות. Rapida.
- **Body** (400, 15–17px, line-height 1.6): ממשק, תוויות, תיאורים. Arbel.
- **Label** (400, 13px, letter-spacing 0.05em): טקסטים מושתקים ברקע, הנחיות קטנות. Arbel.

### Named Rules

**The Hebrew First Rule.** לא מותקן גופן לטיני לתוכן ממשק. כל הטקסט בעברית — גופן עברי. fallback לsans-serif גנרי בלבד.

**The Spacing Rule.** letter-spacing של 4px על כותרות display — ישראלית, לא בלתי אפשרית. אל תרד מ-2px על Rapida.

## 4. Elevation

המערכת שטוחה לחלוטין. אין `box-shadow` על אלמנטי ממשק. עומק מושג דרך:

- **שכבות אטימות** — אלמנטים נעלמים ברקע ב-opacity נמוך
- **transform** — hover מעלה ב-`translateY(-15px)` על ספרים
- **z-index מסודר**: base → strips → question → modal/preview → cursor
- **filter: drop-shadow** על תמונות ספרים בלבד, בזמן hover

**The Flat Floor Rule.** כל המשטחים שקטים. shadow מופיע רק על ספרים שנמצאים ב-hover — כשהם "נרימים" מהמדף. ממשק = flat. ספרים = עם גוף.

## 5. Components

### Buttons

חדים ובטוחים בעצמם. אפס עיגולים. הכפתור לא מתנצל.

- **Shape:** פינות חדות (0px radius)
- **Primary:** רקע `#fff200`, טקסט `#111111`, padding `10px 28px`. border: `1px solid #fff200`
- **Hover:** רקע `transparent`, טקסט `#fff200`, border נשאר. transition 0.2s ease.
- **Disabled:** opacity 0.35, not-allowed cursor
- **Font:** Arbel, letter-spacing 1px, הגופן שנבחר למסך ב-`--font` custom property

### Navigation Buttons (Screen-to-Screen)

- `position: fixed; bottom: 10%–13%` — צמוד לתחתית הוויוופורט
- מיושרים למרכז בזוג, `gap: 32px`
- זהים לכפתורים ראשיים בצבע ובצורה

### Book Cards (מסך 5)

- לא כרטיסים קלאסיים — תמונות ספרים שמרחפות
- `animation: bookFloat` עם `--bf-dur`, `--bf-phase`, `--bf-y` כ-custom properties לאקראיות
- Hover: `animation: none` inline override, `translateY(-15px)`, `filter: drop-shadow`
- `z-index: 30` ב-hover כדי לעלות על שאר האלמנטים

### Color Strips (מסך 6)

- פסים אנכיים שממלאים את המסך מ-top: 78px
- `flex-grow` גדל ב-hover (2.8) וב-selected (2.2)
- cursor: מעויין צהוב מותאם (`url SVG`)
- כותרת: שחור מלא כ-overlay עם טקסט צהוב

### Genre Columns (מסך 4)

- עמודות שמתרחבות ב-hover
- תמונות SVG מפוזרות בתוך העמודה
- selected: border צהוב

### Input Fields (מסך 2)

- **Style:** `background: transparent`, `border: none`, `border-bottom: 1px solid #FFFAF1`
- **Focus:** ללא outline — המסגרת התחתונה מספיקה
- **Font:** Arbel, 24px, color `#FFFAF1`
- **Placeholder:** opacity 0.25

## 6. Do's and Don'ts

### Do:
- **Do** השתמשי ב-`#fff200` בלבד כ-accent. לא gradient, לא variant — אותו hex בכל מקום.
- **Do** שמרי על פינות חדות (0px) בכל רכיבי ממשק — כפתורים, שדות, containers.
- **Do** בכל מסך חדש — הצמידי את הכפתורים ל-`position: fixed; bottom: 10%` ויישרי למרכז.
- **Do** השתמשי ב-Rapida לשאלות הגדולות, Arbel לכל השאר.
- **Do** אנימציות תמיד עם `ease-in-out` ומשך 3.5s–5s לריחוף. לא bounce, לא elastic.
- **Do** הצגת הכריכה האישית היא רגע קולמינציה — תני לה מרחב, לא תסתכלי עליה כ-output.

### Don't:
- **Don't** תוסיפי border-radius לכפתורים, cards, או containers. אפס עיגולים זה הזהות.
- **Don't** תשתמשי בגופני Google Fonts לממשק. הפרויקט עברי, הגופנים עבריים.
- **Don't** תעצבי כמו אתר ממשלתי: אין טבלאות, אין שדות טפסים מסורתיים, אין breadcrumbs.
- **Don't** תעצבי כמו Canva/Figma: אין template pickers, אין grid ממוספר של אפשרויות זהות.
- **Don't** תעצבי כמו e-commerce: אין כפתורי "הוסף לסל", אין מחיר בולט, אין CTA אגרסיבי.
- **Don't** תוסיפי shadow לאלמנטי ממשק. shadow שמור לספרים ב-hover בלבד.
- **Don't** תשתמשי בצהוב כרקע של אלמנטים גדולים. הוא שמור לכפתורים, כותרות — לא לsections.
- **Don't** gradient text — צבע אחד, אחיד, תמיד.
