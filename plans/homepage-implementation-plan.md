# Homepage Implementation Plan

## Objective
Create a completed homepage (index.html) based on UI/code.html template with navigation links to snake.html and eluosi.html game files.

## Current State Analysis
- **Game Files**: `snake.html` (贪吃蛇游戏) and `eluosi.html` (俄罗斯方块) exist in root directory
- **Homepage Template**: `UI/code.html` contains a beautiful homepage design with two game card placeholders
- **Missing**: `index.html` file in root directory with proper game links

## Implementation Steps

### 1. Create index.html from UI/code.html
Copy the entire content of `UI/code.html` to create `index.html` in the root directory.

### 2. Update Game Card 1: "Silly Snake" → snake.html
**Location**: Lines 156-159 in the original UI/code.html
**Current Code**:
```html
<button class="mt-4 flex w-full items-center justify-center gap-2 rounded-full bg-primary py-4 text-base font-bold text-white shadow-lg transition-all hover:bg-primary/90">
<span class="material-symbols-outlined">play_arrow</span>
                            Start Game
                        </button>
```

**Required Change**: Convert button to anchor tag linking to `snake.html`
```html
<a href="snake.html" class="mt-4 flex w-full items-center justify-center gap-2 rounded-full bg-primary py-4 text-base font-bold text-white shadow-lg transition-all hover:bg-primary/90">
<span class="material-symbols-outlined">play_arrow</span>
                            Start Game
                        </a>
```

### 3. Update Game Card 2: "Dreamy Blocks" → eluosi.html
**Location**: Lines 196-199 in the original UI/code.html
**Current Code**:
```html
<button class="mt-4 flex w-full items-center justify-center gap-2 rounded-full bg-blue-500 py-4 text-base font-bold text-white shadow-lg transition-all hover:bg-blue-600">
<span class="material-symbols-outlined">play_arrow</span>
                            Start Game
                        </button>
```

**Required Change**: Convert button to anchor tag linking to `eluosi.html`
```html
<a href="eluosi.html" class="mt-4 flex w-full items-center justify-center gap-2 rounded-full bg-blue-500 py-4 text-base font-bold text-white shadow-lg transition-all hover:bg-blue-600">
<span class="material-symbols-outlined">play_arrow</span>
                            Start Game
                        </a>
```

### 4. Optional Enhancements (Recommended)
1. **Update game descriptions** to better match actual games:
   - "Silly Snake": Change description to match actual snake game
   - "Dreamy Blocks": Change description to match Russian Tetris game

2. **Update navigation links** in header:
   - Games link could scroll to game section
   - Leaderboard link could be functional

3. **Update "Play Now" button** in header to link to games section

## File Structure After Implementation
```
helloworld/
├── index.html (new homepage)
├── snake.html (贪吃蛇游戏)
├── eluosi.html (俄罗斯方块)
├── UI/
│   ├── code.html (original template)
│   └── screen.png
└── plans/
    └── homepage-implementation-plan.md (this file)
```

## Testing Checklist
- [ ] index.html loads correctly in browser
- [ ] "Silly Snake" card links to snake.html
- [ ] "Dreamy Blocks" card links to eluosi.html
- [ ] Both game pages load correctly from homepage
- [ ] Responsive design works on mobile/tablet/desktop
- [ ] All visual elements display correctly

## Notes
- The existing UI/code.html has excellent visual design with pastel colors, glassmorphism effects, and responsive layout
- No major design changes are needed per user request
- The implementation is straightforward: copy template and update two button links