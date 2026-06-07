# ================================================================================
TAPTALK — MY PERSONAL DEV WORKFLOW

# This file is for ME only. Not a prompt. Not rules for Cursor or any AI.
AI should ignore this file entirely.
This is my step-by-step process so I never get lost or skip something.

## RULE ZERO

I do not let any AI write, generate, create, rename, delete, or move anything
unless I have typed the exact instruction myself in that moment.
No "while I'm at it" additions. No assumed next steps. One task at a time.
If I did not ask for it, it does not get built.

# ================================================================================
PHASE 1 — DESIGN (FIGMA)

I do not touch Cursor until Figma is done and I am happy with it.

STEP 1.1 — SCREENS
  [ ] Talk screen (AAC board + TalkBoard keyboard)
  [ ] Today screen (daily planning)
  [ ] First-Then tool
  [ ] List tool
  [ ] Activities screen
  [ ] Progress / Goal Tracker
  [ ] Me / Settings
  [ ] Docs / Library
  [ ] Onboarding flow (splash → questions → done)
  [ ] Tab bar and navigation

STEP 1.2 — COMPONENTS
  [ ] Symbol cell (AAC button)
  [ ] Message bar
  [ ] 3D button (primary, secondary, destructive)
  [ ] Card
  [ ] Tab bar
  [ ] Header
  [ ] Input field

STEP 1.3 — DESIGN SIGN-OFF CHECKLIST
  Before I export anything I confirm:
  [ ] Colours match the locked palette (indigo, amber, semantic only)
  [ ] No red or green used as branding
  [ ] All text is readable (contrast passes)
  [ ] Buttons are large enough (minimum 44px, 60px for AAC)
  [ ] iPhone proportions used (not iPad)
  [ ] No emoji anywhere in the design
  [ ] I am actually happy with it — not just "good enough"

  Only when every box above is ticked do I move to Phase 2.

# ================================================================================
PHASE 2 — REPO & PROJECT SETUP

I do this once. I do not redo it unless something breaks.

STEP 2.1 — GITHUB
  [ ] Repo exists: CavenLink-Dev/TapTalk.v2
  [ ] Main branch is set
  [ ] TAPTALK_GUIDELINES.md is in root
  [ ] .cursorrules is in root

STEP 2.2 — EXPO PROJECT
  [ ] expo init done with SDK 54
  [ ] Expo Router installed and working
  [ ] EAS connected (eas build runs without error)
  [ ] app.json has correct bundleIdentifier and name
  [ ] Expo Go on my iPhone can scan and load the app

STEP 2.3 — CONSTANTS FILES
  I create these myself before asking Cursor to build any screen.
  [ ] constants/colors.ts — all palette values
  [ ] constants/typography.ts — all font sizes and weights
  [ ] constants/spacing.ts — xs sm md lg xl xxl
  [ ] constants/layout.ts — breakpoints, safe area values

  I do not start building screens until these files exist.

STEP 2.4 — FOLDER STRUCTURE
  [ ] app/(tabs)/ exists with placeholder files
  [ ] components/aac/ exists
  [ ] components/shared/ exists
  [ ] services/ exists
  [ ] hooks/ exists
  [ ] assets/symbols/ exists (even if empty)

# ================================================================================
PHASE 3 — IPHONE BUILD (CURSOR + EXPO GO)

One screen at a time. I do not start the next screen until the current one
works in Expo Go on my actual iPhone and I am happy with it.

MY ORDER:
  [ ] 1. Tab bar and navigation skeleton (all tabs present, no content)
  [ ] 2. Talk screen — symbol board only (no TalkBoard yet)
  [ ] 3. Talk screen — MessageBar
  [ ] 4. Talk screen — TalkBoard keyboard
  [ ] 5. Talk screen — TTS (speak button works)
  [ ] 6. Today screen
  [ ] 7. First-Then tool
  [ ] 8. List tool (basic, no reminders yet)
  [ ] 9. List tool — reminders
  [ ] 10. Activities screen (grid only, no content yet)
  [ ] 11. Progress / Goal Tracker
  [ ] 12. Me / Settings
  [ ] 13. Docs / Library
  [ ] 14. Onboarding flow
  [ ] 15. Full app pass — fix anything broken

BEFORE I MARK ANY SCREEN DONE:
  [ ] It loads in Expo Go without crashing
  [ ] It looks correct on my iPhone
  [ ] All buttons are tappable and respond
  [ ] Haptics fire on taps
  [ ] No hardcoded colors or font sizes (I checked the file)
  [ ] accessibilityLabel exists on every touchable
  [ ] I pushed the commit to GitHub

# ================================================================================
PHASE 4 — IPAD VERSION

I do not start this phase until Phase 3 is fully complete and I have signed
off on the iPhone version.

STEP 4.1 — LAYOUT BREAKPOINTS
  [ ] Add iPad breakpoint logic using useWindowDimensions
  [ ] width > 768 = iPad layout
  [ ] width <= 768 = iPhone layout

STEP 4.2 — SCREEN ADJUSTMENTS FOR IPAD
  [ ] Talk screen — wider grid, more columns (5-6 vs 4)
  [ ] Today screen — two-column layout if space allows
  [ ] Activities — larger cards
  [ ] All other screens — check padding and font scaling

STEP 4.3 — IPAD SIGN-OFF
  [ ] Tested on iPad simulator in Xcode
  [ ] Tested on physical iPad if available
  [ ] Nothing broken from iPhone version
  [ ] I am happy with how it looks on both sizes

# ================================================================================
PHASE 5 — APP STORE SUBMISSION

I do not do this until Phase 4 is fully done.

  [ ] App icon created (all required sizes)
  [ ] Splash screen finalized
  [ ] App name confirmed: TapTalk
  [ ] Bundle ID confirmed in app.json
  [ ] Privacy policy URL ready
  [ ] App Store screenshots taken (iPhone + iPad)
  [ ] eas build --platform ios --profile production runs clean
  [ ] Build submitted via EAS Submit or uploaded manually in Transporter
  [ ] App Store Connect listing filled out
  [ ] Submitted for review

# ================================================================================
MY RULES FOR USING AI (CURSOR / CLAUDE)

1. I give one specific instruction at a time.
  Bad:  "Build the Talk screen"
   Good: "Create components/aac/SymbolCell.tsx — a single AAC symbol button
          with an image on top and a label below. Style using colors and
          typography from constants. No logic, just the component."
2. I read every line of code before I accept it.
  If I do not understand a line I ask what it does before moving on.
3. I never let AI decide what comes next.
  AI finishes the task. I decide what the next task is.
4. If AI adds something I did not ask for I delete it immediately.
  No exceptions. Even if it looks useful.
5. I commit to GitHub after every working feature.
  Not at the end of the day. After each feature.
6. If something breaks I fix it before moving forward.
  I do not stack broken things on top of each other.
7. I do not ask AI to "just finish it" or "keep going".
  Every task gets its own clear instruction.
8. I check Expo Go after every single change.
  If it crashes I fix it immediately.

# ================================================================================
MY QUICK DAILY CHECKLIST

Before I start a session:
  [ ] Pull latest from GitHub
  [ ] Expo Go is running on my iPhone
  [ ] I know exactly what ONE thing I am building today

During a session:
  [ ] One task at a time
  [ ] Read AI output before accepting
  [ ] Check Expo Go after each change

Before I finish a session:
  [ ] Everything I built today works in Expo Go
  [ ] Committed and pushed to GitHub
  [ ] I wrote down what I am doing next session

# ================================================================================
CURRENT STATUS — UPDATE THIS YOURSELF

Phase I am in:     [ ]
Last thing I did:  
Next thing to do:  
Blockers:          

# ================================================================================
END

