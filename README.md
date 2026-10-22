# Monster Slayer (Vue.js Game)

A small browser game built with Vue.js where you battle a monster by attacking, using special attacks, and healing until one side's health reaches zero.

![Vue.js](https://img.shields.io/badge/Vue.js-2-4FC08D?logo=vuedotjs&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black) ![Foundation](https://img.shields.io/badge/Foundation-CSS-1779BA)

## Overview

Built in 2021 as a learning project while studying Vue.js fundamentals (data binding, event handling, conditional rendering, and style binding). "Monster Slayer" is the classic exercise from Maximilian Schwarzmüller's Vue.js course.

## Features

- Start a new game with both player and monster at 100 health
- Attack: deals random damage to the monster, then the monster strikes back
- Special attack: deals higher random damage to the monster
- Heal: restores up to 10 health points (capped at 100)
- Give up: ends the current game
- Health bars whose width updates reactively via `:style` binding
- Win/lose detection with a confirm dialog to start a new round
- Controls toggle between "Start New Game" and action buttons with `v-if` / `v-else`

## Tech Stack

- Vue.js 2 (loaded from CDN)
- JavaScript (ES5)
- Foundation CSS
- HTML5, CSS3

## Getting Started

No build tools are needed.

```bash
git clone https://github.com/coderasraf/GameDevelopmentVue.js.git
cd GameDevelopmentVue.js
```

Open `index.html` in your browser.

> Note: `index.html` loads Vue from `https://npmcdn.com/vue/dist/vue.js` without a version. That unversioned URL now resolves to Vue 3, which does not support the `new Vue()` API. Pin Vue 2 instead, for example:
>
> ```html
> <script src="https://unpkg.com/vue@2.7.16/dist/vue.js"></script>
> ```

## Project Structure

```text
GameDevelopmentVue.js/
├── index.html            # Game layout and Vue template
├── app.js                # Vue instance: state, game logic
└── css/
    ├── app.css           # Game styles
    └── foundation.min.css
```

## Known Limitations

- The battle log section is present in the markup but not populated yet.
- The Heal action calls `this.monsterHealth()` instead of `this.monsterAttack()`, which throws an error after healing.

## Author

Built by **Ashraf Siddik**, Shopify developer & CRO specialist.
- Website: [ashraf-siddik.com](https://ashraf-siddik.com)
- GitHub: [@coderasraf](https://github.com/coderasraf)
