<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Gym Manager - Professional Management System

A desktop application for managing gym memberships, attendance, payments, and member tracking with **Excel-based local database**.

## Features

✅ **Member Management** - Register members with flexible pricing (monthly/daily)
✅ **Attendance Tracking** - Real-time check-ins with hourly analytics
✅ **Payment Processing** - Track all transactions and renewals
✅ **Weight Tracking** - Monitor member progress over time
✅ **Class Management** - Manage classes and participation
✅ **Excel Database** - All data stored locally in Excel spreadsheets
✅ **Dark/Light Mode** - Comfortable viewing in any lighting
✅ **Desktop App** - Electron-based standalone application

## Data Storage

All data is automatically saved to Excel:
- **Location**: `C:\Users\YourUsername\AppData\Local\GymManager\gym_manager_data.xlsx`
- **Sheets**: Members, Payments, Attendance, Weight Logs, Classes, Class Participation
- **Access**: Click the Excel icon (📄) in the app to view the data folder

For detailed guide, see [EXCEL_DATABASE_GUIDE.md](EXCEL_DATABASE_GUIDE.md)

## Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- npm

### Run Locally

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Set the `GEMINI_API_KEY` in [.env.local](.env.local)** (optional for AI features)
   ```
   GEMINI_API_KEY=your_api_key_here
   ```

3. **Run the app:**
   ```bash
   npm run dev
   ```

### Build Desktop Executable

Create a standalone Windows executable:

```bash
npm run electron-build
```

The installer will be created in the `dist` folder.

## Scripts

- `npm run dev` - Run development server with Vite
- `npm run build` - Build production bundle
- `npm run preview` - Preview production build
- `npm run electron-dev` - Run Electron development mode
- `npm run electron-build` - Build Windows installer (.exe)
- `npm run lint` - Check TypeScript

## Project Structure

```
gym-manager/
├── src/
│   ├── services/
│   │   ├── gymService.ts - Core business logic
│   │   └── excelService.ts - Excel database integration
│   ├── App.tsx - Main application component
│   ├── main.tsx - React entry point
│   └── index.css - Styling
├── public/
│   ├── main.js - Electron main process
│   └── preload.js - Electron IPC bridges
├── dist/ - Production build output
├── gym_manager_data.xlsx - Local Excel database
└── package.json - Dependencies & build config
```

## Using the App

### Dashboard
- View overview of members, payments, and revenue
- See expiring memberships
- Quick statistics

### Members
- Register new members (monthly/daily plans)
- Renew memberships
- View all members with filtering
- Toggle member status (active/inactive)
- Delete members

### Attendance
- Check-in members
- View today's attendance
- Hourly attendance charts

### Weight Tracker
- Log member weight
- View progress over time
- Delete logs

### Classes
- Create class types (Yoga, HIIT, etc.)
- Record class participation
- View today's classes

## Technology Stack

- **Frontend**: React 19 + TypeScript
- **Desktop**: Electron 31
- **Build**: Vite 6
- **Styling**: Tailwind CSS 4
- **Database**: Excel (ExcelJS)
- **Charts**: Recharts
- **Icons**: Lucide React

## Excel Database

All app data is stored in a local Excel workbook:

### Members Sheet
Stores all member information with registration dates and types

### Payments Sheet
Complete payment history with amounts, dates, and expiry information

### Attendance Sheet
Daily check-in records with timestamps

### Weight Logs Sheet
Member progress tracking data

### Classes Sheet
Available class types in the gym

### Class Participation Sheet
Records of members attending classes

**To access data folder**: Click the Excel icon (📄) in the app header

## Tips

- **Backup regularly**: Export your Excel file regularly
- **Don't edit while running**: Close the app before editing Excel manually
- **Restart to reload**: If you edit the Excel file manually, restart the app
- **Use app to edit**: Always use the app interface for adding/updating data

## Troubleshooting

**App won't start?**
- Check Node.js is installed: `node --version`
- Clear node_modules and reinstall: `rm -r node_modules && npm install`

**Excel file not showing?**
- Check AppData folder: `C:\Users\YourUsername\AppData\Local\GymManager`
- Make sure the app has write permissions to AppData

**Data not persisting?**
- Verify the Excel file exists in the AppData folder
- Check that the app has permissions to access the folder

## License

Open source for educational and personal use.

---

**Built with ❤️ for gym managers**
