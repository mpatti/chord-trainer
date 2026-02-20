# Chord Theory Trainer - Specification

## Project Overview
- **Name**: Chord Theory Trainer
- **Type**: Educational Web Game
- **Core Functionality**: Learn music theory by building chords - see a chord name, select the correct notes on a piano keyboard, hear it played back
- **Target Users**: Musicians who make music but don't understand theory

## UI/UX Specification

### Layout Structure
- **Header**: App title, current level/score
- **Main Area**: 
  - Challenge card showing target chord (e.g., "Cm7b5")
  - Piano keyboard for note selection
  - Submit button
- **Footer**: Streak counter, progress bar

### Visual Design
- **Color Palette**:
  - Background: #0a0a0f (deep dark)
  - Card background: #1a1a24
  - Primary accent: #6366f1 (indigo)
  - Success: #22c55e (green)
  - Error: #ef4444 (red)
  - Text primary: #f8fafc
  - Text secondary: #94a3b8
- **Typography**:
  - Headings: "Outfit" (bold, modern)
  - Body: "DM Sans"
- **Spacing**: 16px base unit
- **Effects**: Subtle glow on active notes, smooth transitions

### Components
1. **Chord Card**: Shows target chord name, level indicator
2. **Piano Keyboard**: 2 octaves (C3-C5), clickable keys, visual feedback
3. **Feedback Modal**: Correct/incorrect with explanation
4. **Progress Bar**: Shows current level progress
5. **Streak Counter**: Fire emoji + count

## Functionality Specification

### Core Features
1. **Chord Generation**: 
   - Level 1-3: Major/minor triads
   - Level 4-6: 7th chords (maj7, min7, dom7)
   - Level 7-10: Extended chords (9th, 11th, 13th)
   - Level 11+: Altered chords (7b9, #11, etc.)

2. **Note Selection**:
   - Click piano keys to toggle notes
   - Visual highlight on selected keys
   - Clear button to reset

3. **Audio Playback**:
   - Real-time synthesis via Tone.js
   - Play chord on submit
   - Arpeggio preview option

4. **Feedback System**:
   - Immediate correct/incorrect
   - Explanation: "Cm7b5 = C - Eb - Gb - Bb. You missed the b5!"
   - Show correct answer if wrong

5. **Progression**:
   - 5 questions per level
   - 4/5 to advance
   - Streak bonus XP

### Data Handling
- Local storage for progress (levels, XP, streaks)
- No backend required

## Acceptance Criteria
- [ ] Piano keyboard renders and is playable
- [ ] Chords generate at appropriate difficulty levels
- [ ] Tone.js plays selected notes
- [ ] Correct/incorrect feedback displays
- [ ] Progress saves to localStorage
- [ ] Levels advance correctly
