# Gym Manager - Excel Database Guide

## Overview
Your Gym Manager app now uses **Excel as a local database** stored in your system's AppData folder. All data (members, payments, attendance, weight logs, classes) is automatically saved to an Excel workbook.

## Data Location
Excel file location: `C:\Users\YourUsername\AppData\Local\GymManager\gym_manager_data.xlsx`

You can access this folder directly from the app by clicking the **Excel icon** (📄) in the top-right header.

## Excel Sheets
The workbook contains the following sheets:

1. **Members** - All gym members with registration details
   - Columns: ID, Name, Expiry, Type, Status, Classes, DOB, Created At

2. **Payments** - All payment transactions
   - Columns: ID, Member ID, Member Name, Amount, Months, Date, Expiry Date

3. **Attendance** - Daily check-ins and attendance records
   - Columns: ID, Member ID, Member Name, Timestamp

4. **Weight Logs** - Member weight tracking data
   - Columns: ID, Member ID, Member Name, Weight, Date

5. **Classes** - Available class types
   - Columns: ID, Name

6. **Class Participation** - Member class attendance
   - Columns: ID, Member ID, Member Name, Class ID, Class Name, Timestamp

## How It Works

### Data Sync
- **When you run the app**: All data from Excel is automatically loaded into memory
- **When you add/update/delete records**: Changes are saved to both Excel and localStorage (for backup)
- **Excel is the source of truth**: If you manually edit the Excel file, restart the app to see updates

### Real-time Database
- The app uses Excel as a persistent database
- All your records are preserved even after closing the app
- No internet connection needed

## Using the Data

### View Data
1. Click the **Excel icon (📄)** in the top-right to open the data folder
2. Open `gym_manager_data.xlsx` with Microsoft Excel, Google Sheets, or any spreadsheet app

### Edit Data Manually
You can directly edit the Excel file:
1. Open `gym_manager_data.xlsx`
2. Make changes directly in the spreadsheet
3. Save the file
4. **Restart the app** to load the updated data

### Export Data
The app data is already in Excel format. You can:
- Copy sheets to create reports
- Use Excel charts and pivot tables for analysis
- Share specific sheets with management

### Delete Records
To delete records:
- Use the app's delete buttons (recommended - ensures consistency)
- Or delete rows in Excel and restart the app

## Troubleshooting

**Q: Changes aren't showing up in Excel?**
- The app syncs to Excel automatically. Check the file location and make sure Excel isn't locked.

**Q: Excel file is locked?**
- Close the Excel file before using the app, or use the app to manage data instead of manually editing.

**Q: Want to reset all data?**
- Delete `gym_manager_data.xlsx` and restart the app (creates a fresh file)
- Or clear the file by deleting all data rows (keeping headers)

## Tips

✅ **Do:**
- Use the app to add/edit/delete data (most reliable)
- Keep the Excel file in the AppData folder
- Backup the Excel file regularly if it's important data
- Use Excel for reporting and analysis

❌ **Don't:**
- Edit the Excel file while the app is running
- Delete the header row
- Move the Excel file to a different location (the app expects it in AppData)
- Share the file via sync services (Dropbox, OneDrive) while the app is running

---

**Happy managing!** 💪
