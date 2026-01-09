# Near Miss Data Analysis Dashboard

## 📊 Project Overview
An interactive web-based dashboard for analyzing near-miss incident data in construction companies. This dashboard processes and visualizes approximately 7,800+ incident records with multiple interactive charts and real-time statistics.

## 🎯 Features

### Data Visualization (7 Charts)
1. **Top Incident Categories** - Bar chart showing primary incident categories
2. **Severity Level Distribution** - Pie chart displaying severity levels (1-5)
3. **Monthly Incident Trend** - Area chart showing incident trends over 12 months
4. **Incidents by Region** - Horizontal bar chart of geographic distribution
5. **Behavior Type Analysis** - Pie chart analyzing At-Risk vs Safe vs Positive behaviors
6. **Unsafe Condition vs Behavior** - Bar chart comparing unsafe conditions and behaviors
7. **Business Unit (GBU) Distribution** - Bar chart showing incidents across business units

### Dashboard Features
- ✅ Real-time data loading from JSON files
- ✅ Sample data generator for testing
- ✅ Interactive charts with hover tooltips
- ✅ Responsive design (works on desktop, tablet, mobile)
- ✅ Error handling for invalid data
- ✅ Statistics cards showing key metrics
- ✅ Clean and modern UI with gradient design

## 🛠️ Technologies Used

- **Frontend Framework**: React 18
- **Charting Library**: Recharts
- **Styling**: Tailwind CSS
- **Icons**: Lucide React
- **Language**: JavaScript (ES6+)

## 📋 Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for loading CDN libraries)

## 🚀 Setup Instructions

### Method 1: Direct HTML File (Easiest)
1. Download the `index.html` file from this repository
2. Double-click the file to open it in your default browser
3. Click "Upload JSON" to load your near-miss data
4. Or click "Load Sample Data" to see demo visualizations

### Method 2: Local Web Server
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx http-server

# Then open browser to: http://localhost:8000
```

## 📁 Project Structure

```
near-miss-dashboard/
│
├── index.html           # Main HTML file with embedded React app
├── README.md           # This file
├── sample-data.json    # Sample near-miss data (optional)
└── screenshots/        # Dashboard screenshots (optional)
```

## 📊 Data Format

The dashboard expects JSON data with the following structure:

```json
[
  {
    "id": "135774577",
    "incident_number": "135774577",
    "primary_category": "Energy Isolation",
    "severity_level": 2,
    "behavior_type": "At-Risk",
    "region": "Asia (North Asia)",
    "gbu": "Energy",
    "location": "Area 42",
    "unsafe_condition_or_behavior": "Unsafe Condition",
    "month": 2,
    "year": 2024,
    "week": 5,
    "is_lcv": true,
    "company_type": "B"
  }
]
```

### Required Fields
- `primary_category`: String (incident category)
- `severity_level`: Number (1-5)
- `behavior_type`: String (At-Risk, Safe, Positive)
- `region`: String (geographic region)
- `gbu`: String (business unit)
- `month`: Number (1-12)
- `unsafe_condition_or_behavior`: String

### Optional Fields
- `location`, `year`, `week`, `is_lcv`, `company_type`, etc.

## 🎮 How to Use

1. **Load Data**
   - Click "Upload JSON" button
   - Select your JSON file (supports up to 10,000+ records)
   - Dashboard automatically processes and displays visualizations

2. **View Sample Data**
   - Click "Load Sample Data" to see demo with 200 sample records
   - Use this to understand the dashboard functionality

3. **Interact with Charts**
   - Hover over chart elements to see detailed tooltips
   - All charts are responsive and interactive

4. **View Statistics**
   - Top stat cards show: Total Incidents, High Severity, At-Risk Behaviors, Regions

## 📈 Chart Descriptions

### 1. Top Incident Categories
Shows the distribution of incidents across different categories like Energy Isolation, Fall Protection, Lifting Operations, etc.

### 2. Severity Level Distribution
Visualizes the breakdown of incidents by severity levels (1=Low to 5=Critical).

### 3. Monthly Incident Trend
Displays the trend of incidents over 12 months to identify patterns and seasonal variations.

### 4. Incidents by Region
Geographic distribution showing which regions have the most incidents.

### 5. Behavior Type Analysis
Analyzes whether incidents were due to At-Risk, Safe, or Positive behaviors.

### 6. Unsafe Condition vs Behavior
Compares incidents caused by unsafe conditions versus unsafe behaviors.

### 7. Business Unit Distribution
Shows incident distribution across different business units (Energy, Infrastructure, Mining, etc.).

## ⚠️ Assumptions and Limitations

### Assumptions
- JSON file is properly formatted and contains valid data
- Date fields are in millisecond timestamp format
- Severity levels range from 1 to 5
- Month values range from 1 to 12

### Limitations
- Maximum recommended file size: ~50MB (for browser performance)
- No data persistence (data is lost on page refresh)
- Requires modern browser with JavaScript enabled
- No backend server (client-side only)
- Cannot modify or export data (view-only dashboard)

## 🔧 Troubleshooting

### Issue: Charts not showing data
**Solution**: Ensure your JSON file matches the expected format. Check browser console for errors.

### Issue: File upload fails
**Solution**: Verify JSON file is valid. Use a JSON validator tool.

### Issue: Dashboard is slow
**Solution**: For very large datasets (>10,000 records), consider filtering data before upload.

## 🎨 Customization

To customize the dashboard:
1. Open `index.html` in a text editor
2. Modify the color schemes in the `COLORS` and `SEVERITY_COLORS` arrays
3. Adjust chart dimensions by changing `height` values in `ResponsiveContainer`
4. Add new charts by following the existing chart structure

## 📝 Development Notes

- Built with React functional components and hooks
- Uses Recharts library for all visualizations
- Tailwind CSS for responsive design
- No build process required (runs directly in browser)
- CDN-based dependencies for easy deployment

## 👨‍💻 Author

Created as part of the Near Miss Data Analysis assignment

## 📄 License

This project is created for educational purposes.

## 🙏 Acknowledgments

- Recharts for charting library
- Tailwind CSS for styling
- Lucide React for icons

---

**Last Updated**: January 2026

For questions or issues, please contact the repository owner.