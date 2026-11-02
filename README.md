# BudgetWin

A simple, easy-to-use personal budget application with a clean GUI.

## Project Goals

- **Easy to use** — minimal learning curve; core tasks (add income, add expense, view balance) should take seconds.
- **Good GUI** — modern, uncluttered interface that feels native and responsive.
- **Fast** — instant feedback on every action; no loading spinners for local operations.

## Application Steps / Roadmap

### Phase 1 — Core Functionality (MVP)

1. **Define data model**
   - Transactions: id, date, amount, type (income/expense), category, note
   - Categories: predefined + user-customizable
   - Budgets: monthly limit per category (optional)

2. **Choose tech stack for GUI**
   - Evaluate options: Electron + React, Tauri + Svelte, or native (WPF / Flutter)
   - Prioritize: cross-platform support, small binary size, modern look

3. **Design the main screen layout**
   - Top bar: current balance, month selector
   - Center: transaction list (grouped by date or category)
   - Bottom/side: quick-add form (amount, type, category, note)
   - Keep it to one primary view — no deep navigation in MVP

4. **Implement CRUD for transactions**
   - Add income / expense
   - Edit existing entry
   - Delete with confirmation
   - Local persistence (SQLite or JSON file)

5. **Basic summary dashboard**
   - Total income, total expenses, net balance for selected month
   - Simple bar or donut chart: spending by category

### Phase 2 — Polish & Usability

6. **GUI refinements**
   - Dark / light theme toggle
   - Keyboard shortcuts (e.g., `N` = new transaction)
   - Smooth animations on add/delete
   - Responsive layout for different window sizes

7. **Search & filter**
   - Filter by date range, category, type
   - Text search in notes

8. **Budget alerts**
   - Visual indicator when a category exceeds its budget
   - Optional desktop notification

### Phase 3 — Advanced Features

9. **Recurring transactions** (subscriptions, salary)
10. **Export / import** (CSV, PDF statement)
11. **Multiple accounts / wallets**
12. **Cloud sync** (optional; local-first by default)

## Design Principles

| Principle | Guideline |
|-----------|-----------|
| Simplicity | One screen for 90% of tasks. No hidden menus. |
| Speed | All local operations < 50 ms perceived latency. |
| Clarity | Numbers are large, labels are short, colors mean something (green = in, red = out). |
| Forgiveness | Undo on delete; inline validation instead of error dialogs. |
| Native feel | Follow OS conventions for window chrome, fonts, and shortcuts. |

## Tech Stack (TBD)

> Decision pending — see Phase 1, step 2.

- **Frontend / GUI:** _to be decided_
- **Backend / Logic:** local-first, no server required
- **Storage:** SQLite (preferred) or structured JSON
- **Packaging:** single installer or portable executable

## Repository Structure (planned)

```
BudgetWin/
├── README.md
├── src/
│   ├── main/          # app entry point
│   ├── components/    # UI components
│   ├── services/      # business logic, storage
│   └── assets/        # icons, styles
├── docs/              # design notes, mockups
└── tests/
```

## Contributing

- Branch naming: `alpha001`, `beta001`, `feature/<name>`
- Keep PRs small and focused
- No external dependencies without discussion

---

*Branch: alpha001 — initial planning document.*
