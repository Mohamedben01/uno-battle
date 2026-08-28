# Build a Fun UNO Match Tracker Mobile App
Build a complete, functional, modern, playful mobile application for tracking UNO matches with friends.

The application should be extremely simple to use: users create a match, choose the number of rounds, add players, and after every round simply select who lost.

The app automatically tracks losses, calculates the ranking, assigns fun animal emojis and titles, and displays the final results.

The application must support **Moroccan Darija (Darija), English, Standard Arabic, and French**.

---

# 1. APP CONCEPT
The app is a lightweight entertainment companion for UNO games between friends.

The main purpose is:

**Track who loses each round.**

Do NOT create a complicated UNO scoring system.

There should be:

- No card tracking.
- No complicated points.
- No need to enter card values.
- No account required.
- No mandatory internet connection.
- No complicated statistics.
The basic flow is:

**Open app → New Match → Choose number of rounds → Add players → Start → Select the loser after each round → Continue → Final ranking.**

---

# 2. HOME SCREEN
Create a modern, colorful and playful home screen.

Display:

### 🎮 UNO Battle
Main button:

**🎮 New Match**

Secondary button:

**📜 Match History**

Additional button:

**⚙️ Settings**

Optional small information/about section.

## Design
The design should feel like a casual party game.

Use colors inspired by UNO:

- Red
- Yellow
- Green
- Blue
Use:

- Rounded cards
- Large buttons
- Large emojis
- Smooth animations
- Playful typography
- Clean spacing
- Modern mobile UI
The application should be **mobile-first** and optimized for one-handed use.

---

# 3. CREATE A NEW MATCH
When the user taps:

**🎮 New Match**

Open the match setup screen.

## Number of rounds
Allow the user to select how many rounds the match will contain.

Quick options:

- 3 rounds
- 5 rounds
- 10 rounds
- 15 rounds
- 20 rounds
Also provide:

**Custom number of rounds**

The user can enter any valid number.

Example:

> How many rounds?
> 10

---

# 4. ADD PLAYERS
Allow users to add between **2 and 10 players**.

Each player needs:

- Player name
- Player ID
- Loss count
- Dynamic animal emoji
- Dynamic title
Allow the user to:

- Add a player
- Edit a player
- Delete a player
Do not allow the match to start with fewer than 2 players.

Example:

### Players
🧑 Yassine
🧑 Adam
🧑 Sara
🧑 Mehdi

Button:

**+ Add Player**

Primary button:

### ▶️ Start Match

---

# 5. MATCH SCREEN
After starting the match, display a very simple game interface.

At the top:

# Round 1 / 10
Then:

## Who lost this round?
Display every player as a large clickable card.

Example:

### 🦁 Yassine
0 losses

### 🐯 Adam
0 losses

### 🦊 Sara
0 losses

### 🐢 Mehdi
0 losses

The player cards must be large and easy to tap.

---

# 6. RECORDING THE LOSER
When the user taps a player, immediately register that player as the loser of the current round.

Example:

### 💀 Mehdi lost this round!
Then display:

**🫏 Mehdi**

**1 loss**

Show a short fun animation.

Then display:

### ➡️ Next Round
Important:

- Only ONE player can lose each round.
- Once a loser is selected, prevent another player from being selected for that round.
- Automatically increase the selected player's loss count.
- Save the result immediately.
- Update the ranking.
- Update the animal emojis.
- Update the titles.

---

# 7. UNDO LAST ROUND
Add an option:

### ↩️ Undo Last Round
This is important in case the wrong player was selected.

When the user taps Undo:

1. Ask for confirmation.
2. Remove the last round result.
3. Decrease that player's loss count.
4. Recalculate the ranking.
5. Recalculate the animal emoji.
6. Recalculate the title.
7. Return to the previous round.
Example confirmation:

> Are you sure you want to undo the last round?
Buttons:

**Cancel**

**Undo**

---

# 8. ANIMAL RANKING SYSTEM
Create a dynamic animal ranking system based on the player's current number of losses.

The player with the **fewest losses** should have the best animal.

Example:

🥇 🦁 Lion — 1st place
🥈 🐯 Tiger — 2nd place
🥉 🦊 Fox — 3rd place
🐺 Wolf — 4th place
🐒 Monkey — 5th place
🐢 Turtle — 6th place
🐔 Chicken — 7th place
🫏 Donkey — Last place

Add more animal emojis if there are more players.

## Important
The animal must NOT be permanently assigned to the player.

It should change dynamically based on the player's current ranking.

Example:

If Yassine starts in 1st place:

🦁 Yassine

But after several rounds, if he moves to 3rd:

🦊 Yassine

The application should automatically update this.

---

# 9. ANIMAL TITLES
Each animal should have a fun title.

Examples:

🦁 **King of UNO 👑**

🐯 **The Challenger 🔥**

🦊 **The Clever Fox 😏**

🐺 **The Wolf 🐺**

🐒 **The Wild One 😂**

🐢 **The Turtle 🐢**

🐔 **The Rookie 😂**

🫏 **Last Place 😂**

These titles are intended to be humorous and friendly between friends.

Keep them playful rather than offensive.

---

# 10. LIVE LEADERBOARD
During the match, display a live ranking.

Example:

# 🏆 Current Ranking
🥇 🦁 Yassine — 1 loss

🥈 🐯 Adam — 2 losses

🥉 🦊 Sara — 3 losses

4️⃣ 🫏 Mehdi — 4 losses

Ranking rules:

**Fewer losses = better ranking.**

**More losses = lower ranking.**

Update the ranking automatically after every round.

---

# 11. TIE SYSTEM
If two or more players have the same number of losses:

Do not randomly choose a winner.

Show the same ranking position.

Example:

🥇 🦁 Yassine — 2 losses
🥇 🦁 Sara — 2 losses
🥉 🐯 Adam — 3 losses

Display:

### 🔥 It's a Tie!
The system should handle ties consistently.

---

# 12. ROUND HISTORY
Display a simple history of every completed round.

Example:

# Round History
Round 1 → 🫏 Mehdi

Round 2 → 🦊 Sara

Round 3 → 🫏 Mehdi

Round 4 → 🐯 Adam

Round 5 → 🫏 Mehdi

Each round should clearly show:

- Round number
- Loser
- Loser's animal at that moment
Allow users to scroll through the history.

---

# 13. FINAL RESULTS
After the final round, automatically open the final results screen.

Title:

# 🏆 Match Finished!
Display the winner.

The winner is the player with the **fewest total losses**.

Example:

## 🏆 Winner
🦁 **Yassine**

### King of UNO 👑
Then show:

🥇 🦁 Yassine — 1 loss

🥈 🐯 Adam — 2 losses

🥉 🦊 Sara — 3 losses

4️⃣ 🫏 Mehdi — 5 losses

Add a fun celebration animation.

Possible animations:

- Confetti
- Emoji effects
- Winner card animation
- Small fireworks
- Cards bouncing
Keep animations smooth and lightweight.

---

# 14. END MATCH EARLY
Allow users to end a match before all rounds are completed.

Button:

### 🛑 End Match
Ask for confirmation:

> Are you sure you want to end the match?
Buttons:

**Cancel**

**End Match**

If confirmed, show results based on the rounds already completed.

---

# 15. MATCH HISTORY
Save completed matches locally on the device.

Each saved match should contain:

- Match ID
- Date
- Number of rounds
- Player names
- Round results
- Final ranking
- Total losses
- Final animal
- Final title
The user can open an old match and view all details.

Example:

### 📜 Match History
**UNO Match — Aug 28, 2026**

10 rounds
4 players

🦁 Yassine — 1 loss
🐯 Adam — 2 losses
🦊 Sara — 3 losses
🫏 Mehdi — 4 losses

---

# 16. OFFLINE FIRST
The application must work completely offline.

The core game must NOT depend on an internet connection.

Store locally:

- Current match
- Players
- Losses
- Round history
- Completed matches
- Settings
- Selected language
If the user closes the app during a match, the match should still be there when they reopen the application.

---

# 17. START A NEW MATCH
After finishing a match, provide:

### 🎮 New Match
The user can immediately create another match.

If a match is currently in progress and the user tries to start another match, show a warning.

Example:

> You have a match in progress. Start a new match?
Buttons:

**Continue Current Match**

**Start New Match**

---

# 18. LANGUAGE SUPPORT
The application must support four languages:

### 🇲🇦 Moroccan Darija

### 🇬🇧 English

### 🇸🇦 Standard Arabic

### 🇫🇷 French
The default language can be based on the device language, but the user must be able to manually change it.

---

# 19. MOROCCAN DARIJA
Moroccan Darija is an important part of this application.

Do NOT simply translate Standard Arabic word-for-word.

Use natural Moroccan Darija that friends would actually use when playing UNO.

The Darija should feel:

- Casual
- Funny
- Friendly
- Natural
- Moroccan
- Easy to understand
Use Arabic script for Darija.

Common gaming words such as UNO, Match, etc. can remain in Latin characters when natural.

## Darija examples
Home:

**ماتش جديد 🎮**

**الماتشات السابقة 📜**

**الإعدادات ⚙️**

Match setup:

**شحال من جولة؟**

**زيد اللاعبين**

**سمي اللاعب**

**بدا الماتش ▶️**

During the match:

**الجولة 1 من 10**

**شكون خسر هاد الجولة؟**

**الجولة الجاية ➡️**

**تراجع على آخر جولة ↩️**

When someone loses:

**💀 فلان خسر هاد الجولة!**

**وااااا الحمار 😂**

Final results:

**سالينا الماتش 🏆**

**الرابح ديال الماتش!**

**أقل خسارات**

**تعادل 🔥**

**عاود ماتش جديد 🎮**

---

# 20. DARIJA ANIMAL TITLES
Create natural Moroccan Darija versions of the animal titles.

Examples:

🦁 Lion:

**ملك UNO 👑**

🐯 Tiger:

**المنافس القوي 🔥**

🦊 Fox:

**الثعلب المكار 😏**

🐺 Wolf:

**الذيب 🐺**

🐒 Monkey:

**القرد المشاغب 😂**

🐢 Turtle:

**السلحفاة 🐢**

🐔 Chicken:

**الدجاجة 😂**

🫏 Donkey:

**الحمار ديال الجولة 😂**

These are meant as jokes between friends.

Keep the language playful and humorous.

---

# 21. LANGUAGE SWITCHER
Add a language selector inside Settings.

Example:

## Language / اللغة
🇲🇦 Darija

🇬🇧 English

🇸🇦 العربية

🇫🇷 Français

When the user changes the language:

- Update the entire interface.
- Update buttons.
- Update menus.
- Update messages.
- Update animal titles.
- Update result screens.
- Save the language locally.
- Remember the selected language after restarting the app.

---

# 22. LOCALIZATION ARCHITECTURE
Do NOT hard-code text directly inside UI components.

Create a proper localization system.

Use translation keys such as:

`app_name`

`new_match`

`match_history`

`settings`

`start_match`

`number_of_rounds`

`add_player`

`current_round`

`who_lost`

`next_round`

`undo`

`undo_last_round`

`end_match`

`match_finished`

`winner`

`tie`

`new_game`

`losses`

`round_history`

`language`

Each key must have translations for:

- Darija
- English
- Standard Arabic
- French
Make it easy to add additional languages later.

---

# 23. DARIJA TRANSLATION QUALITY
Do not use machine-like literal translations.

For example:

Prefer:

**"شكون خسر هاد الجولة؟"**

instead of:

**"من خسر هذه الجولة؟"**

Prefer:

**"الجولة الجاية"**

instead of:

**"الجولة التالية"**

Prefer:

**"بدا الماتش"**

instead of:

**"ابدأ المباراة"**

The Darija version should feel like a Moroccan friend is talking to the user.

---

# 24. MAIN NAVIGATION
Keep navigation simple.

## Home
→ New Match

→ Match History

→ Settings

## New Match
→ Choose rounds

→ Add players

→ Start Match

## Match
→ Current round

→ Select loser

→ Current ranking

→ Round history

## Final Results
→ Winner

→ Final ranking

→ Match details

→ New Match

---

# 25. DATA MODEL
Use a clean data structure.

## Match

- matchId
- createdAt
- totalRounds
- currentRound
- players
- roundHistory
- status
- language

## Player

- playerId
- name
- losses

## Round

- roundNumber
- loserId
- timestamp
The ranking and animal should be calculated dynamically from the loss count.

Do NOT manually store ranking positions if they can be calculated.

---

# 26. TECHNICAL ARCHITECTURE
Choose the best modern cross-platform technology for Android and iOS.

The app should have a clean, scalable architecture.

Separate:

- UI
- Game logic
- Ranking logic
- Animal assignment logic
- Local storage
- Match history
- Localization
Create reusable components for:

- Player cards
- Ranking cards
- Animal badges
- Round indicators
- Buttons
- Confirmation dialogs
- Result animations
- Language selector

---

# 27. RESPONSIVE DESIGN
The application must work well on different phone sizes.

Test:

- Small phones
- Normal phones
- Large phones
- Portrait orientation
Use responsive layouts.

Do not allow important buttons or player cards to become too small.

---

# 28. ACCESSIBILITY
Make the application easy to use.

Use:

- Large touch targets
- Good text contrast
- Clear visual hierarchy
- Readable fonts
- Icons + text where useful
- Avoid relying only on color to communicate information
Animal emojis should be large enough to recognize easily.

---

# 29. PERFORMANCE
The application should open quickly.

Avoid unnecessary network requests.

The main match screen should feel instant.

Selecting a loser should update the UI immediately.

Animations should be lightweight.

Local data should load quickly.

---

# 30. IMPORTANT EDGE CASES
Test all of the following:

### Test 1
2 players, 1 round.

### Test 2
10 players, 20 rounds.

### Test 3
Multiple players with the same number of losses.

### Test 4
One player loses several rounds in a row.

### Test 5
Undo the last round.

### Test 6
Close the app during an active match and reopen it.

### Test 7
End the match early.

### Test 8
Delete a player before starting the match.

### Test 9
Start a new match after completing the previous match.

### Test 10
Open an old match from Match History.

### Test 11
Change the language during the application.

### Test 12
Use Moroccan Darija throughout the complete application.

### Test 13
Switch from Darija to English and verify every screen updates correctly.

### Test 14
Tie between two players.

### Test 15
Tie between three or more players.

---

# 31. FINAL PRODUCT REQUIREMENTS
Do not build only a static prototype.

Build a fully functional application with:

- Complete navigation
- New Match flow
- Round selection
- Player management
- Loss tracking
- Dynamic ranking
- Dynamic animal system
- Animal titles
- Round history
- Undo functionality
- Early match ending
- Final results
- Tie handling
- Match history
- Local storage
- Offline functionality
- Automatic recovery of an active match
- Darija localization
- English localization
- Standard Arabic localization
- French localization
- Language switching
- Responsive mobile UI
- Smooth animations
- Clean architecture

---

# 32. CORE USER EXPERIENCE
The entire application should revolve around this extremely simple experience:

**Open the app**

↓

**🎮 New Match**

↓

**Choose number of rounds**

↓

**Add players**

↓

**▶️ Start Match**

↓

**"شكون خسر هاد الجولة؟"**

↓

**Tap the loser**

↓

**The app records +1 loss**

↓

**Ranking and animals update automatically**

↓

**➡️ Next Round**

↓

**Repeat until the final round**

↓

**🏆 Final Results**

↓

**Show winner, rankings, losses, animals and titles**

↓

**🎮 New Match**

The final application should feel like a **fun Moroccan UNO companion app for friends**, with a strong focus on simplicity, humor, fast interaction, and a natural Moroccan Darija experience.