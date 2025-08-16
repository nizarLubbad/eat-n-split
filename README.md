# 🍽️ Eat N Split

A simple and intuitive React application for splitting bills and managing expenses with friends. Keep track of who owes what and settle debts easily!

## ✨ Features

- **Friend Management**: Add and manage your friends list
- **Bill Splitting**: Split bills between you and your friends
- **Balance Tracking**: Keep track of who owes money and who is owed money
- **Visual Indicators**: Color-coded balance display (green for money owed to you, red for money you owe)
- **Responsive Design**: Clean and modern user interface
- **Real-time Updates**: Instant balance calculations and updates

## 🚀 Demo

Check out the live demo: [Eat N Split](https://nizarlubbad.github.io/eat-n-split)

## 🛠️ Technologies Used

- **React 19.1.1** - Frontend framework
- **JavaScript (ES6+)** - Programming language
- **CSS3** - Styling and responsive design
- **Create React App** - Project setup and build tools
- **GitHub Pages** - Deployment platform

## ⚡ Quick Start

### Prerequisites

Make sure you have Node.js installed on your machine.

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/nizarLubbad/eat-n-split.git
   cd eat-n-split
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Start the development server**

   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000) to view the app.

## 📱 How to Use

### Adding Friends

1. Click the "Add Friend" button
2. Enter your friend's name
3. Optionally add a custom profile image URL (uses Pravatar by default)
4. Click "Add" to add them to your friends list

### Splitting Bills

1. Select a friend from your friends list
2. Enter the total bill amount
3. Enter how much you paid
4. The app automatically calculates your friend's portion
5. Select who is paying the bill
6. Click "Split Bill" to update balances

### Understanding Balances

- **Green text**: Your friend owes you money
- **Red text**: You owe your friend money
- **Gray text**: You and your friend are even

## 🏗️ Project Structure

```
src/
├── components/
│   ├── Button.js          # Reusable button component
│   ├── FormAddFriend.js   # Form for adding new friends
│   ├── FormSplitBill.js   # Form for splitting bills
│   ├── Friend.js          # Individual friend list item
│   └── FriendList.js      # Friends list container
├── App.js                 # Main application component
├── index.js               # React DOM entry point
└── index.css              # Global styles
```

## 🎨 Key Features Breakdown

### State Management

- Uses React hooks (`useState`) for local state management
- Manages friends list, form visibility, and selected friend state

### Component Architecture

- Modular component design with clear separation of concerns
- Reusable Button component used throughout the app
- Props-based communication between components

### Form Handling

- Controlled components for all form inputs
- Form validation to prevent empty submissions
- Automatic balance calculations

## 📦 Available Scripts

### Development

- `npm start` - Runs the app in development mode
- `npm test` - Launches the test runner
- `npm run build` - Builds the app for production

### Deployment

- `npm run predeploy` - Builds the app before deployment
- `npm run deploy` - Deploys to GitHub Pages

## 🌟 Code Highlights

### Smart Balance Calculation

The app automatically calculates balances based on who paid what:

```javascript
function handleSplitBill(value) {
  setFriends((friends) =>
    friends.map((friend) =>
      friend.id === selectedFriend.id
        ? { ...friend, balance: friend.balance + value }
        : friend
    )
  );
}
```

### Dynamic Friend Selection

Toggle between friends with smooth state management:

```javascript
function handleSelection(friend) {
  setSelectedFriend((current) => (current?.id === friend.id ? null : friend));
}
```

## 👨‍💻 Author

**Nizar Lubbad**

- GitHub: [@nizarLubbad](https://github.com/nizarLubbad)
- LinkedIn: [@nizar-lubbad](http://linkedin.com/in/nizar-lubbad)

---

Made with ❤️ using React
