# abc_isfor_xyz Inventory Management System

A complete, modern inventory management system built for GitHub Pages hosting with barcode generation, sales tracking, and comprehensive reporting.

## Features

✅ **Inventory Management**
- Add, edit, and delete inventory items
- Track quantity in stock and items sold
- Real-time inventory updates

✅ **Barcode Generation**
- Generate unique barcodes for each item with "abc_isfor_xyz" branding
- Print individual barcodes
- CODE128 barcode format

✅ **Sales Tracking**
- Record sales and automatically update inventory
- Track quantity sold per item
- Prevent overselling with validation

✅ **Comprehensive Reports**
- Inventory by category
- In-stock items report
- Sold items report
- Export reports to CSV

✅ **Data Management**
- Export inventory to JSON for GitHub storage
- Import inventory from JSON files
- Local browser storage for quick access
- Backup and restore functionality

✅ **Search & Filter**
- Real-time search across all inventory
- Filter by category, brand, description

## GitHub Pages Setup

### Step 1: Create a New Repository

1. Go to [GitHub](https://github.com) and log in
2. Click the **+** icon in the top right and select **New repository**
3. Name your repository (e.g., `abc-inventory-system`)
4. Make it **Public** (required for GitHub Pages)
5. Click **Create repository**

### Step 2: Upload Files

1. Click **uploading an existing file** or **Add file** → **Upload files**
2. Upload the `index.html` file
3. Upload `sample-inventory.json` (optional - for testing)
4. Commit the changes

### Step 3: Enable GitHub Pages

1. Go to your repository **Settings**
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Select **main** branch and **/ (root)** folder
5. Click **Save**
6. Your site will be live at: `https://yourusername.github.io/repository-name/`

## Using the System

### Dashboard
- View key statistics (total items, in stock, sold, categories)
- Quick search through recent inventory
- Real-time status updates

### Adding Items
1. Click the **Add Item** tab
2. Fill in the form:
   - **Category**: Product category (e.g., Electronics, Clothing)
   - **Description**: Detailed item description
   - **Brand**: Manufacturer or brand name
   - **Price**: Item price in dollars
   - **Initial Quantity**: Starting stock quantity
3. Click **Add Item**

### Managing Inventory
1. Go to the **Inventory** tab
2. Use the search box to find items
3. Available actions for each item:
   - **Barcode**: Generate and print barcode
   - **Edit**: Modify item details
   - **Sell**: Record a sale
   - **Delete**: Remove item

### Recording Sales
1. Click the **Sell** button next to an item
2. Enter the quantity sold
3. The system will:
   - Reduce available quantity
   - Increase sold count
   - Update all reports

### Viewing Reports
1. Click the **Reports** tab to see:
   - Inventory grouped by category
   - All in-stock items
   - All sold items
2. Use **Print Reports** to print
3. Use **Export to CSV** to download data

### Data Management

#### Exporting Inventory (Recommended for GitHub Storage)
1. Go to **Data Management** tab
2. Click **Export to JSON**
3. Save the file (e.g., `inventory_2025-11-03.json`)
4. Upload this file to your GitHub repository for backup

#### Importing Inventory
1. Go to **Data Management** tab
2. Click **Choose File** under Import section
3. Select your JSON file
4. Click **Import from JSON**
5. Confirm the replacement

#### GitHub Storage Workflow
To keep your inventory backed up on GitHub:

1. **Export regularly**: Download your inventory JSON
2. **Commit to GitHub**: 
   ```bash
   git add inventory_backup.json
   git commit -m "Update inventory backup"
   git push
   ```
3. **Restore when needed**: Download from GitHub and import

## File Structure

```
your-repository/
├── index.html                 # Main application file
├── README.md                  # This file
└── sample-inventory.json      # Sample data (optional)
```

## Features Breakdown

### Form Fields
- **Category**: Groups items for reporting
- **Description**: Full item details
- **Brand**: Manufacturer/brand name
- **Price**: Cost per unit
- **Quantity**: Stock on hand
- **Sold**: Automatically tracked

### Barcode System
- Unique ID assigned to each item
- Format: `ABC-{ItemID}`
- Displays "abc_isfor_xyz" branding
- Printable for labeling

### Storage
- **Browser Local Storage**: Quick access, persists across sessions
- **JSON Export**: Backup to GitHub or local system
- **No Database Required**: Pure client-side solution

## Browser Compatibility

Works on all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

## Tips for Best Results

1. **Regular Backups**: Export your inventory weekly
2. **Category Naming**: Use consistent category names
3. **Search Function**: Use keywords to find items quickly
4. **Print Reports**: Generate monthly reports for records
5. **Barcode Printing**: Use a label printer for best results

## Troubleshooting

**Problem**: Data disappeared after clearing browser cache
**Solution**: Import your latest JSON backup from GitHub

**Problem**: Barcodes not displaying
**Solution**: Ensure JavaScript is enabled and you're using a modern browser

**Problem**: Can't sell more than available quantity
**Solution**: This is a safety feature - update quantity first if needed

## Data Format

The JSON export follows this structure:
```json
[
  {
    "id": 1,
    "category": "Electronics",
    "description": "Wireless Mouse",
    "brand": "Logitech",
    "price": 29.99,
    "quantity": 50,
    "sold": 5,
    "dateAdded": "2025-11-03T12:00:00.000Z"
  }
]
```

## Advanced: Automatic GitHub Sync

For advanced users wanting automatic GitHub synchronization:

1. Use GitHub Actions to commit exported JSON
2. Use the GitHub API to fetch/update inventory
3. Consider using GitHub's REST API with authentication

*(Note: This requires additional JavaScript code and GitHub personal access tokens)*

## Security Notes

- All data is stored locally in the browser
- No server-side processing
- JSON exports contain all inventory data - store securely
- GitHub repositories can be public or private

## Support

For issues or questions:
1. Check this README
2. Review your browser console for errors
3. Ensure you're using a supported browser
4. Try exporting and re-importing your data

## License

Free to use and modify for personal and commercial purposes.

---

**Built for abc_isfor_xyz** | Powered by GitHub Pages
