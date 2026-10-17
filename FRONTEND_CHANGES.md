# ExpenseWise frontend update

This package contains the updated frontend only. The backend was not included in the uploaded ZIP, so backend/database changes could not be made or verified.

## Updated files
- `src/pages/customer/Register.jsx` — adds a birthday date picker, derives age from the selected birthday, validates birthday/password/account fields, and adds ExpenseWise branding and a cleaner registration card. The birthday is sent as `birthday` in the registration request.
- `src/pages/customer/Login.jsx` — replaces the dark photo-led login background with a light, minimal layout and a simple ExpenseWise mark.
- `src/pages/customer/Expenses.jsx` — uses predefined expense-category dropdowns for add/edit and filters, validates the selected category, makes rows expandable for record details, and groups Edit/Delete under a compact native menu.
- `src/pages/customer/Income.jsx` — uses predefined income-category dropdowns, validates the selected category, applies consistent green income styling, makes rows expandable, and groups Edit/Delete under a compact native menu.
- `src/components/AdminNav.jsx` — changes Admin navigation to a light brand style and removes the Manage Categories link.
- `src/App.jsx` — removes the Admin Categories route.
- `src/components/CustomerNav.jsx` — changes the navigation bar to a light, minimal style and adds the brand mark.
- `src/components/CustomerLayout.jsx` — removes decorative emoji icons from the customer navigation and adds the brand mark.
- `src/theme.css`, `src/design.css`, `src/index.css` — establishes a consistent light green/neutral theme, reduces decoration, and styles row details and compact action menus.

## Important backend note
The uploaded archive contained the frontend, not the Flask/API backend. The frontend sends the birthday field, but it will only be saved to the database if the backend registration endpoint and database schema support `birthday`. Existing backend support for profile uniqueness and category validation also needs to remain enforced server-side. No database schema or API code was changed here.

## Run
1. Extract this folder.
2. Open a terminal in the project folder.
3. Run `npm install`.
4. Run `npm run dev`.
