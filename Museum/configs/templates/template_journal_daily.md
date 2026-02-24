---
date: 2026-02-24
type: journal
mood: 5
meditation_mins: 0
gratitude: ""
fajr-dua: ""
fajr-sunnah: false
fajr-fardh: false
read-quran-fajr: false
dhuhr-dua: ""
dhuhr-sunnah-b: false
dhuhr-fardh: false
dhuhr-sunnah-a: false
dhuhr-nafl: false
read-quran-dhuhr: false
asr-dua: ""
asr-sunnah: false
asr-fardh: false
read-quran-asr: false
maghrib-dua: ""
maghrib-fardh: false
maghrib-sunnah: false
maghrib-nafl: false
read-quran-maghrib: false
isha-dua: ""
isha-sunnah-b: false
isha-fardh: false
isha-sunnah-a: false
isha-nafl-b: false
isha-witr: false
isha-nafl-a: false
read-quran-isha: false
tahajjud-dua: ""
tahajjud-nafl: false
read-quran-tahajjud: false
ishraq-dua: ""
ishraq-nafl: false
read-quran-ishraq: false
family_time: ""
sleep_hours: 0
sleep_quality: 
bedtime: 
waketime: 
water_glasses: 0
water_goal: false
breakfast: ""
lunch: ""
dinner: ""
snacks: ""
fasting: false
workout: ""
workout_duration: 0
workout_intensity: 
steps: 0
learned_today: ""
skills_practiced: ""
money_spent: 0
purchases: ""
work_achievements: ""
study_topics: ""
people_met: ""
movies_watched: ""
games_played: ""
movie: ""
rate_movie: 0
thought_movie: ""
series: ""
rate_series: 0
thought_series: ""
anime: ""
rate_anime: 0
thought_anime: ""
comic: ""
rate_comic: 0
thought_comic: ""
video: ""
rate_video: 0
thought_video: ""
book: ""
rate_book: 0
thought_book: ""
game: ""
rate_game: 0
thought_game: ""
audio: ""
rate_audio: 0
thought_audio: ""
Calendar Title: "[[Museum/configs/templates/template_journal_daily|template_journal_daily]]"
---

# <% tp.date.now("dddd, Do MMM YYYY") %>

> [!example] Navigation
> [[<% tp.date.now("YYYY-MM-DD", -1) %>|Yesterday]] | [[<% tp.date.now("YYYY-MM-DD", 1) %>|Tomorrow]]

---
# Lifestyle

> [!tip] What's your mood today?
> `INPUT[slider(addLabels):mood]`

# Spirituality

>[!tip] Gratitude
> `INPUT[textArea(placeholder("What are the Gratitudes you want to express today?")):gratitude]`

## Prayer

> [!question] Daily Practices
> 
> #### Fajr
> *What have you asked?* `INPUT[text(placeholder(Dua)):fajr-dua]`
> `2R Sunnah` `INPUT[toggle:fajr-sunnah]` `2R Fardh` `INPUT[toggle:fajr-fardh]` `Read-Quran` `INPUT[toggle:read-quran-fajr]`
> 
> #### Dhuhr
> *What have you asked?* `INPUT[text(placeholder(Dua)):dhuhr-dua]`
> `4R Sunnah` `INPUT[toggle:dhuhr-sunnah-b]` `4R Fardh` `INPUT[toggle:dhuhr-fardh]` `2R Sunnah` `INPUT[toggle:dhuhr-sunnah-a]` `2R Nafl` `INPUT[toggle:dhuhr-nafl]` `Read-Quran` `INPUT[toggle:read-quran-dhuhr]`
> 
> #### Asr
> *What have you asked?* `INPUT[text(placeholder(Dua)):asr-dua]`
> `4R Sunnah` `INPUT[toggle:asr-sunnah]` `4R Fardh` `INPUT[toggle:asr-fardh]` `Read-Quran` `INPUT[toggle:read-quran-asr]`
> 
> #### Maghrib
> *What have you asked?* `INPUT[text(placeholder(Dua)):maghrib-dua]`
> `3R Fardh` `INPUT[toggle:maghrib-fardh]` `2R Sunnah` `INPUT[toggle:maghrib-sunnah]` `2R Nafl` `INPUT[toggle:maghrib-nafl]` `Read-Quran` `INPUT[toggle:read-quran-maghrib]`
> 
> #### Isha
> *What have you asked?* `INPUT[text(placeholder(Dua)):isha-dua]`
> `4R Sunnah` `INPUT[toggle:isha-sunnah-b]` `4R Fardh` `INPUT[toggle:isha-fardh]` `2R Sunnah` `INPUT[toggle:isha-sunnah-a]` `2R Nafl` `INPUT[toggle:isha-nafl-b]` `3R Witr` `INPUT[toggle:isha-witr]` `2R Nafl` `INPUT[toggle:isha-nafl-a]` `Read-Quran` `INPUT[toggle:read-quran-isha]`
> 
> #### Tahajjud
> *What have you asked?* `INPUT[text(placeholder(Dua)):tahajjud-dua]`
> `Nafl` `INPUT[toggle:tahajjud-nafl]` `Read-Quran` `INPUT[toggle:read-quran-tahajjud]`
> 
> #### Ishraq
> *What have you asked?* `INPUT[text(placeholder(Dua)):ishraq-dua]`
> `Nafl` `INPUT[toggle:ishraq-nafl]` `Read-Quran` `INPUT[toggle:read-quran-ishraq]`
> 
> **How much time did you meditate today?**
> `INPUT[number:meditation_mins]` minutes

# Presence & Connection

> [!heart] **Relationships & Social**
> `Quality Time` `INPUT[textArea(placeholder("Family/Partner context")):family_time]`
> `Social Log` `INPUT[textArea(placeholder("Who did you meet/talk to?")):people_met]`

> [!todo] **Family Interaction**
> ```tasks
> filename includes relationship.md
> heading includes Family
> happens <% tp.date.now("YYYY-MM-DD") %>
> short mode
> ```

# Health

> [!quote] **Sleep & Recovery**
> `Hours` `INPUT[number:sleep_hours]` `Quality` `INPUT[inlineSelect(option(😫 Poor), option(😐 Fair), option(🙂 Good), option(🤩 Excellent)):sleep_quality]`
> `Bedtime` `INPUT[text(placeholder("11:00 PM")):bedtime]` `Wake Up` `INPUT[text(placeholder("06:00 AM")):waketime]`

> [!food] **Nutrition & Hydration**
> `Fasting?` `INPUT[toggle:fasting]` `Water (Glasses)` `INPUT[number:water_glasses]` `Goal?` `INPUT[toggle:water_goal]`
> `Breakfast` `INPUT[text:breakfast]`
> `Lunch` `INPUT[text:lunch]`
> `Dinner` `INPUT[text:dinner]`
> `Snacks/Other` `INPUT[text:snacks]`

> [!exercise] **Movement & Fitness**
> `Workout` `INPUT[text(placeholder("Type of exercise")):workout]`
> `Duration (min)` `INPUT[number:workout_duration]` `Intensity` `INPUT[inlineSelect(option(Low), option(Moderate), option(High)):workout_intensity]`
> `Steps` `INPUT[number:steps]`

# Growth Hub

> [!brain] **Knowledge & Skills**
> `Learned Today` `INPUT[textArea(placeholder("Distilled insights...")):learned_today]`
> `Skills Practiced` `INPUT[text(placeholder("Coding, Art, Language, etc.")):skills_practiced]`

> [!info] **Academic Focus**
> `Topics Studied` `INPUT[textArea(placeholder("Modules, Chapters, Papers...")):study_topics]`

# Capital & Output

> [!money] **Finance Tracker**
> `Money Spent` $`INPUT[number:money_spent]`
> `Purchases` `INPUT[textArea(placeholder("List items bought")):purchases]`

> [!star] **Career & Achievements**
> `Wins & Focus` `INPUT[textArea(placeholder("Professional milestones or focus area")):work_achievements]`

# Entertainment

### Movie

> [!tip] What movie did you consume today to entertain yourself?
> `Name`  `INPUT[text(placeholder(Name of watched movie)):movie]`
>
> `Rating` `INPUT[slider(addLabels):rate_movie]`
>
> `Thoughts`
>
> `INPUT[textArea(placeholder(What are your thoughts on the movie?)):thought_movie]`
> 

### Series

> [!tip] What series did you consume today to entertain yourself?
> `Name` `INPUT[text(placeholder(Name of watched series)):series]`
> 
> `Rating` `INPUT[slider(addLabels):rate_series]`
> 
> `Thoughts`
> 
> `INPUT[textArea(placeholder(What are your thoughts on the series?)):thought_series]`

### Anime

> [!tip] What anime did you consume today to entertain yourself?
> `Name` `INPUT[text(placeholder(Name of watched anime)):anime]`
> 
> `Rating` `INPUT[slider(addLabels):rate_anime]`
> 
> `Thoughts`
> 
> `INPUT[textArea(placeholder(What are your thoughts on the anime?)):thought_anime]`

### Comic

> [!tip] What comic did you consume today to entertain yourself?
> `Name` `INPUT[text(placeholder(Name of read comic)):comic]`
> 
> `Rating` `INPUT[slider(addLabels):rate_comic]`
> 
> `Thoughts`
> 
> `INPUT[textArea(placeholder(What are your thoughts on the comic?)):thought_comic]`

### Book

> [!tip] What book did you read today to entertain yourself?
> `Name` `INPUT[text(placeholder(What are you reading?)):book]`
> 
> `Rating` `INPUT[slider(addLabels):rate_book]`
> 
> `Thoughts`
> 
> `INPUT[textArea(placeholder(What are your thoughts on the book?)):thought_book]`

### Game

> [!tip] What game did you play today to entertain yourself?
> `Name` `INPUT[text(placeholder(What did you play?)):game]`
> 
> `Rating` `INPUT[slider(addLabels):rate_game]`
> 
> `Thoughts`
> 
> `INPUT[textArea(placeholder(What are your thoughts on the game?)):thought_game]`

### Video

> [!tip] What video did you watch today to entertain yourself?
> `Name` `INPUT[text(placeholder(Name of watched video?)):video]`
> 
> `Rating` `INPUT[slider(addLabels):rate_video]`
> 
> `Thoughts`
> 
> `INPUT[textArea(placeholder(What did you watch?)):thought_video]`

### Audio

> [!tip] What audio (podcast/music) did you listen to today to entertain yourself?
> `Name` `INPUT[text(placeholder(Podcasts/Music name?)):audio]`
> 
> `Rating` `INPUT[slider(addLabels):rate_audio]`
> 
> `Thoughts`
> 
> `INPUT[textArea(placeholder(What are your thoughts?)):thought_audio]`
---

# Daily Summary

## Notes Created Today

```dataview
LIST 
WHERE file.cday = date("<% tp.date.now("YYYY-MM-DD") %>") AND file.name != this.file.name
```

## Tasks Completed Today

```dataview
TASK 
WHERE completed AND completion = date("<% tp.date.now("YYYY-MM-DD") %>")
```
