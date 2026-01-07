# 💰 Personal Budget Tracker

A sleek, lightweight, and responsive web application designed to help users manage their finances by tracking income, monitoring expenses, and maintaining a real-time balance overview.

---

## 🌟 Key Features

* **Real-Time Calculations**: Automatically updates Total Balance, Income, and Expenses as entries are added or removed.
* **Persistent Storage**: Utilizes `localStorage` to ensure financial data remains saved even after the browser is refreshed or closed.
* **Transaction History**: Provides a clean, color-coded list of all previous entries (green for income, red for expenses).
* **Unique ID Generation**: Each transaction is assigned a random ID to ensure accurate tracking and deletion.
* **Mobile-First Design**: Built with a responsive layout that works seamlessly on desktops and mobile devices.

---

## 🛠️ Technical Stack

This project is a high-performance application built using **Vanilla Web Technologies**:

* **HTML5**: Provides the semantic structure for the dashboard.
* **CSS3**: Uses CSS Variables (Custom Properties) for theme management and Flexbox for a centered, modern layout.
* **JavaScript (ES6+)**: Employs high-order functions like `.map()`, `.filter()`, and `.reduce()` for efficient data processing and DOM manipulation.

---

## 🚀 How to Use

1.  **Add Income**: Enter a description in the "Text" field and a positive number in the "Amount" field (e.g., `Salary`, `5000`).
2.  **Add Expense**: Enter a description and a negative number (e.g., `Rent`, `-1200`).
3.  **Monitor Dashboard**: Watch the Balance, Income, and Expense totals update instantly.
4.  **Delete Entries**: Hover over any item in the History list and click the "x" button to remove it from your records.

---
## 📸 Screenshot

Screenshots of my tested devices. <br>
Iphone 12 Pro

<img width="450" height="980" alt="Screenshot 2026-01-05 165551" src="https://github.com/user-attachments/assets/44d61edb-5585-4550-92ac-0804314f171d" />

Omnibook X 16 inches

<img width="1900" height="1090" alt="Screenshot 2026-01-05 165748" src="https://github.com/user-attachments/assets/8fdcd16b-b0e0-4068-8984-b41428f3fa51" />


---

## 🧠 Core Logic Overview

The application processes data using functional programming patterns to ensure accuracy:

```javascript
// Example of how totals are calculated within the app
function updateValues() {
    const amounts = transactions.map(transaction => transaction.amount);
    const total = amounts.reduce((acc, item) => (acc += item), 0).toFixed(2);
    // ... logic for income and expense filtering
}
