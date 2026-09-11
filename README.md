# SpendWise – Week 2 Assignment

A simple budget tracker web page, built on top of the Week 1 project. This week adds a proper expense table, an upgraded add-expense form, multimedia content, an interactive collapsible section, and advanced CSS selectors.

## Files

- `index.html` – page structure and content
- `styles.css` – all styling
- `README.md` – this file

## What was built

### 1. Expense Table
The old "No expenses yet" placeholder is replaced with a real `<table>` using `<thead>` (Name, Amount, Category, Date headers) and `<tbody>` with 5 hardcoded rows of sample expenses, plus a `<tfoot>` showing the total. The table is styled with `border-collapse: collapse`, cell padding, a dark header row, and alternating row colors via `tr:nth-child(even)`.

### 2. Add Expense Form
A new "Add Expense" section wraps all inputs in a `<form>`:
- `#expense-name` – text input for the expense name
- `#expense-amount` – number input for the amount
- `#expense-category` – a `<select>` dropdown with 5 options (Food, Transport, Rent, Entertainment, Other)
- `#expense-date` – date input
- `#add-expense-btn` – a `<button type="button">` labeled "Add Expense" (not wired up yet — that comes in Week 7 with JavaScript)

Every input has a unique, descriptive `id` so it can be targeted by JavaScript later.

### 3. Multimedia
- An `<img>` logo icon sits next to the main heading, with `src`, `alt`, and `width` attributes.
- Two `<iframe>` embeds: a Google Maps location and a YouTube video, each with `width`, `height`, `title` (video)/appropriate attributes, and `frameborder`/`style="border:0"`.

### 4. Interactive Elements
- A `<details>`/`<summary>` block titled "How to use this tracker" explains what the form and table do, and is collapsed by default.
- Table rows use a `:hover` style to lighten on mouseover.
- The "Add Expense" button uses `cursor: pointer`.

### 5. Advanced CSS Selectors
At least three selectors from the course list are used:
- **Descendant selector** – `.add-expense-section input, .add-expense-section select`
- **Direct child selector** – `.add-expense-section form > *`
- **Pseudo-class based on position** – `tbody tr:first-child` and `tbody tr:nth-child(even)`
- **Negation pseudo-class** – `.add-expense-section form :not(button)`
- **Focus state** – `.add-expense-section input:focus, .add-expense-section select:focus`

## Notes
- The form button does not yet do anything — functionality is added in Week 7 once JavaScript is introduced.
- Sample expense data is hardcoded for now; it will later be generated dynamically.