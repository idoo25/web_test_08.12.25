# Graphical User Interface Guide

## 🎨 Integrated Tabbed Interface

The Plant Disease Monitoring System now includes a comprehensive graphical user interface that combines all features in a single, professional tabbed interface.

## 📍 Location in Notebook

The integrated UI is located near the end of the notebook (cells 31-32), after all individual feature implementations.

## 🎯 Features

### Tab 1: 🔍 Search
**RAG-Powered Document Search**
- Search academic articles about plant diseases
- Input: Text query
- Output: Ranked results with matched terms and previews
- Example queries:
  - "deep learning disease detection"
  - "IoT sensors monitoring"
  - "fungal infection treatment"

### Tab 2: 🖼️ Upload
**Plant Image Upload**
- Upload plant photos for analysis
- Supports common image formats (JPG, PNG)
- Displays image metadata and preview
- Ready for disease detection integration

### Tab 3: 🌡️ Sensors
**Real-Time IoT Sensor Data**
- Current readings from Adafruit IO
- Three sensors: Temperature, Humidity, Soil Moisture
- Health status indicators:
  - ✅ Optimal
  - ⚠️ Acceptable
  - ❌ Critical
- One-click refresh

### Tab 4: 📡 Query
**MQTT Data Query Interface**
- Query historical sensor data
- Filters:
  - Sensor type (dropdown)
  - Time range (1-168 hours slider)
- Displays:
  - Statistical summary (mean, min, max, std dev)
  - Latest readings table
  - Time range information

### Tab 5: 📊 Dashboard
**Interactive Visual Dashboard**
- Time range selection (6-168 hours)
- Four-panel Plotly visualization:
  1. Temperature trend line chart
  2. Humidity trend line chart
  3. Soil moisture trend line chart
  4. Plant health score gauge (0-100)
- Real-time chart generation
- Interactive zoom, pan, and hover

### Tab 6: ⚡ Anomaly
**Smart Anomaly Detection**
- Real-time threshold monitoring
- Statistical trend analysis (μ ± 2σ)
- Three severity levels:
  - 🔴 **Critical** - Immediate action required
  - 🟡 **Warning** - Monitor closely
  - 🟠 **Anomaly** - Unusual pattern detected
- Actionable recommendations
- Alert history and summary

## 💡 Usage

### Quick Start
1. Run all notebook cells in order
2. Scroll to the "Integrated Graphical User Interface" section
3. Click on any tab to access that feature
4. Use the buttons and controls within each tab

### Navigation
- Click on tab headers to switch between features
- Each tab maintains its own state
- Outputs appear within the selected tab

### Tips
- Start with the **Sensors** tab to check system connectivity
- Use **Search** to find relevant plant disease information
- Generate **Dashboard** for visual presentation
- Run **Anomaly** detection to check plant health status

## 🎓 Benefits for Presentation

### Classroom Demo
- Single interface for all features
- Easy navigation during presentation
- Professional appearance
- No scrolling through notebook cells

### User Experience
- Organized layout
- Clear visual hierarchy
- Consistent design language
- Intuitive controls

### Flexibility
- Can use integrated UI or individual UIs
- Original feature cells still available
- Best of both worlds

## 🔧 Technical Details

### Implementation
- Built with `ipywidgets.Tab` component
- Uses `VBox` and `HBox` for layouts
- Separate `Output` widgets for each tab
- Event handlers for all buttons

### Dependencies
- ipywidgets
- IPython.display
- All feature functions from earlier cells

### Code Structure
```python
# Create tab content for each feature
search_tab_content = VBox([...])
upload_tab_content = VBox([...])
# ... (other tabs)

# Combine into Tab widget
main_ui = Tab()
main_ui.children = [search_tab_content, upload_tab_content, ...]
main_ui.set_title(0, '🔍 Search')
# ... (other titles)

# Display
display(main_ui)
```

## 📊 Comparison: Before vs After

### Before (Individual UIs)
- Features scattered across notebook
- Need to scroll to find each feature
- Multiple buttons at different locations
- Good for development, less ideal for demos

### After (Integrated UI)
- All features in one location
- Tabbed navigation
- Single control panel
- Perfect for presentations and user interaction

### Both Available!
The integrated UI complements (doesn't replace) the individual UIs. Use whichever works best for your needs.

## 🎨 Visual Design

### Color Scheme
- **Success** (Green): Refresh, Go actions
- **Primary** (Blue): Query, Database operations
- **Warning** (Orange): Dashboard generation
- **Danger** (Red): Anomaly detection
- **Info** (Light Blue): Upload operations

### Icons
- 🔍 Search
- 🖼️ Image/Upload
- 🌡️ Temperature/Sensors
- 📡 Communication/Query
- 📊 Charts/Dashboard
- ⚡ Lightning/Alerts

## 📝 Notes

- The UI requires all previous cells to be executed first
- Adafruit IO connection must be established
- All helper functions must be defined before using the UI
- Works best in Google Colab environment

## 🚀 Future Enhancements

Potential improvements for future versions:
- Add progress bars for long operations
- Include data export functionality
- Add real-time auto-refresh option
- Implement user preferences/settings tab
- Add help/documentation tab

---

**Created for:** Cloud Computing Course HW2  
**Institution:** Braude Academic College of Engineering  
**Date:** December 2025
