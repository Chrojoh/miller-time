# 🏆 CKC Grand Master Points Tracker

A comprehensive web application that extracts competition data from CanuckDogs and automatically calculates official CKC Grand Master championship points with title progression tracking.

## 📋 Table of Contents
- [Features](#features)
- [Recent Updates](#recent-updates)
- [Installation](#installation)
- [Usage](#usage)
- [CKC Points Formula](#ckc-points-formula)
- [Interface Overview](#interface-overview)
- [Data Sources](#data-sources)
- [Export Features](#export-features)
- [Technical Details](#technical-details)
- [Troubleshooting](#troubleshooting)
- [Disclaimer](#disclaimer)

## ✨ Features

### 🎯 Core Functionality
- **Complete CanuckDogs Data Extraction**: Pulls ALL competition results from CanuckDogs format (multiple lines per day)
- **Enhanced Points Parsing**: Extracts dogs beaten from point breakdowns like "4 (1-1-2-1)"
- **Real-Time CKC Points Calculation**: Applies official Canadian Kennel Club Grand Master points formula
- **Title Progression Tracking**: Monitors progress through CH → GCH → GCHX → GM → GMS
- **Year-by-Year Analysis**: Detailed breakdown of points earned each competition year
- **Comprehensive Reporting**: PDF export with calculations and supporting data

### 📊 Dashboard Features
- **Live Points Total**: Current Grand Master points with title status
- **Recent Results**: Latest competition results with detailed point calculations
- **Progress Indicators**: Visual tracking toward next title level
- **Summary Statistics**: Shows breakdown, averages, and totals

### 📈 Analytics
- **Formula Transparency**: Shows exact calculation for each result
- **Historical Tracking**: Multi-year progression analysis  
- **Performance Metrics**: Average points per show, win rates
- **Data Verification**: Cross-reference with raw CanuckDogs data

## 🆕 Recent Updates

### Version 1.1 - Enhanced Data Extraction
- **Multiple Results Per Day**: Now captures ALL lines from each show day
- **Improved Points Parsing**: Extracts dogs beaten from formats like "4 (1-1-2-1)"
- **Enhanced Calculations**: More accurate Grand Master point calculations
- **Better Formula Display**: Shows step-by-step calculation breakdowns
- **Complete Data Coverage**: No show results are missed during extraction

### Key Improvements
- **Regina KC Example**: Now captures 4 lines instead of 2 (Sunday: Group 3rd + BOB, Saturday: BOB + Select Dog)
- **Dogs Beaten Accuracy**: Extracts actual counts from CanuckDogs point breakdowns
- **Zero Point Handling**: Properly shows why certain results earned no points
- **Calculation Transparency**: Each result shows complete formula breakdown

## 🚀 Installation

### Quick Start
1. **Download the HTML file** (`ckc_master_tracker.html`)
2. **Open in any modern web browser** (Chrome, Firefox, Safari, Edge)
3. **No additional software required** - runs entirely in browser

### Requirements
- Modern web browser with JavaScript enabled
- Internet connection (for fonts and styling)
- No server setup needed - works as standalone HTML file

### File Structure
```
ckc_master_tracker.html    # Main application file
README.md                  # This documentation
```

## 📖 Usage

### Getting Started
1. **Open the application** in your web browser
2. **Enter the dog's registered name** in the search field
3. **Click "Extract & Calculate Points"** to process data
4. **Navigate through tabs** to explore different views

### Demo Mode
- Try entering **"Miller"** to see the system with sample data
- Demonstrates all features with realistic competition results
- Shows calculation formulas and title progression
- Includes multiple results per day examples

### Step-by-Step Workflow
```
Enter Dog Name → Extract All Data Lines → Calculate Points → Review Results → Export Reports
```

## 🧮 CKC Points Formula

### Base Points
| Achievement | Formula | Maximum |
|-------------|---------|---------|
| **Best of Breed** | min(dogs_defeated, 5) | 5 points |
| **Winners Dog/Bitch** | min(dogs_defeated, 5) | 5 points |

### Group Placement Bonuses
| Placement | Formula | Maximum |
|-----------|---------|---------|
| **Group 1st** | +min(dogs_defeated × 2, 40) | 40 points |
| **Group 2nd** | +min(dogs_defeated × 1.5, 30) | 30 points |
| **Group 3rd** | +min(dogs_defeated × 1, 20) | 20 points |
| **Group 4th** | +min(dogs_defeated × 0.5, 10) | 10 points |

### Special Bonuses
- **Best in Show**: +min(dogs_defeated × 5, 200) points
- **Specialty Shows**: ×1.5 multiplier on all points
- **All-Breed Shows**: Standard calculation

### Dogs Beaten Extraction
The system automatically extracts dogs beaten from CanuckDogs point formats:
- **"4 (1-1-2-1)"**: Sums breakdown = 5 dogs beaten
- **"13"**: Estimates dogs beaten for group placements
- **"N/A"**: Assigns 0 dogs beaten

### Title Thresholds
| Title | Points Required |
|-------|-----------------|
| **Champion (CH)** | Prerequisite |
| **Grand Champion (GCH)** | 20+ points |
| **Grand Champion Excellent (GCHX)** | 100+ points |
| **Grand Master (GM)** | 200+ points |
| **Grand Master Supreme (GMS)** | 400+ points |

## 🖥️ Interface Overview

### Tab Navigation
The application features four main sections:

#### 📊 Points Dashboard
- **Total Points Display**: Large, prominent points counter
- **Title Progress**: Visual indicators for each title level
- **Recent Results**: Latest 8 competition results with detailed calculations
- **Summary Statistics**: Key metrics and averages

#### 📅 Year-by-Year Progress
- **Year Cards**: Clickable cards showing annual point totals
- **Detailed Breakdown**: Complete results for selected year with ALL lines
- **Trend Analysis**: Progress tracking across multiple years
- **Performance Metrics**: Year-over-year comparisons

#### 📋 CanuckDogs Raw Data
- **Complete Data Table**: ALL extracted competition information
- **Sortable Columns**: Year, show, position, judge, points
- **Color Coding**: Highlights point-earning results
- **Data Verification**: Shows both raw CanuckDogs data and calculated points

#### 📄 Export Reports
- **PDF Generation**: Three report types available
- **Complete Documentation**: All calculations and supporting data
- **Professional Format**: Suitable for official submissions
- **Batch Export**: Multiple formats and detail levels

### Visual Elements
- **Color-Coded Results**: Green for points earned, gray for no points
- **Progress Bars**: Visual title progression indicators
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Professional Styling**: Clean, modern interface

## 📊 Data Sources

### Primary Input
- **CanuckDogs Format**: Extracts from standard CanuckDogs result displays
- **Multiple Lines Per Day**: Captures every result line for each competition day
- **Competition Categories**: Conformation, Obedience, Rally Obedience
- **Multi-Year Support**: Handles results across multiple competition years

### Data Fields Extracted
- Show name and date range
- Judge information
- Placement/position achieved
- Competition day (Friday/Saturday/Sunday)
- Raw points from CanuckDogs display
- Dogs defeated (extracted from point breakdown formats)
- All result lines per day (not just summary)

### Enhanced Data Processing
- **Complete Line Extraction**: Every CanuckDogs result line is captured
- **Smart Points Parsing**: Handles formats like "4 (1-1-2-1)", "13", "N/A"
- **Automatic Dog Count**: Extracts actual dogs beaten from point breakdowns
- **Point Calculation**: Applies CKC formula to each individual result
- **Data Validation**: Checks for consistency and completeness
- **Error Handling**: Graceful handling of missing or invalid data

## 📋 Export Features

### Report Types

#### 1. Complete Championship Report
- **Full Competition History**: ALL results with calculations
- **Multiple Lines Per Show**: Every result line included
- **Title Progress Timeline**: Achievement dates and progression
- **Formula Documentation**: CKC points calculation reference
- **Summary Statistics**: Totals, averages, and metrics

#### 2. Year-by-Year Progress Report
- **Annual Breakdowns**: Detailed yearly analysis with all results
- **Show-by-Show Details**: Every line item included
- **Trend Visualization**: Progress tracking over time
- **Performance Comparison**: Year-over-year metrics
- **Goal Tracking**: Points needed for next title level

#### 3. Points Verification Report
- **Calculation Transparency**: Result-by-result formula breakdown
- **Source Data**: Raw CanuckDogs information included
- **Dogs Beaten Details**: Shows extraction from point breakdowns
- **Audit Trail**: Complete calculation methodology
- **Official Reference**: CKC formula documentation

### Export Formats
- **PDF-Ready HTML**: Opens in new window for easy printing
- **Downloadable Files**: Automatically named with dog name and date
- **Professional Layout**: Suitable for official submissions
- **Print Optimization**: Formatted for standard paper sizes

## 🔧 Technical Details

### Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: CSS Grid, Flexbox, CSS Animations
- **Data Processing**: Pure JavaScript (no external dependencies)
- **Export**: HTML-to-PDF conversion ready

### Enhanced Data Processing
- **Multi-Line Extraction**: Captures all results per competition day
- **Point Format Parsing**: Handles various CanuckDogs point display formats
- **Dogs Beaten Calculation**: Extracts from breakdown strings
- **Formula Application**: Individual calculation for each result line

### Browser Compatibility
- **Chrome/Edge**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Full support
- **Mobile Browsers**: Responsive design support

### Performance
- **Lightweight**: Single HTML file under 60KB
- **Fast Loading**: No external dependencies
- **Offline Capable**: Works without internet after initial load
- **Memory Efficient**: Optimized for large datasets with multiple lines

### Data Security
- **Local Processing**: All calculations performed in browser
- **No Data Transmission**: Information stays on your device
- **Privacy Focused**: No tracking or analytics
- **Secure**: No server-side vulnerabilities

## 🛠️ Troubleshooting

### Common Issues

#### Data Not Loading
- **Check Dog Name**: Ensure exact registered name spelling
- **Try Demo Mode**: Use "Miller" to test functionality
- **Browser Compatibility**: Use modern browser version
- **JavaScript Enabled**: Verify JavaScript is not blocked

#### Missing Results
- **Multiple Lines**: Ensure all lines per day are being captured
- **Point Formats**: Verify various point display formats are handled
- **Date Ranges**: Check that multi-day shows are properly processed

#### Incorrect Point Calculations
- **Dogs Beaten**: Verify extraction from point breakdown strings like "(1-1-2-1)"
- **Formula Application**: Check against official CKC documentation
- **Multiple Results**: Ensure each line gets individual calculation
- **Manual Verification**: Cross-check with CKC official records

#### Export Problems
- **Popup Blockers**: Disable for report generation
- **PDF Printing**: Use browser's print-to-PDF function
- **File Download**: Check download folder for exported files
- **Browser Settings**: Ensure downloads are enabled

### Data Quality
- **Complete Extraction**: Verify all CanuckDogs result lines are captured
- **Point Format Consistency**: Check various point display formats
- **Date Formatting**: Ensure consistent date formats
- **Judge Names**: Check for spelling consistency
- **Show Names**: Verify complete show information

### Performance Issues
- **Large Datasets**: May slow with 200+ individual results
- **Browser Memory**: Close other tabs for better performance
- **Mobile Devices**: May require horizontal orientation
- **Refresh Browser**: Clear cache if issues persist

## ⚠️ Disclaimer

### Important Notices

#### Official Verification Required
- **CKC Authority**: Always verify points with official CKC records
- **Title Applications**: Use official CKC documentation for submissions
- **Calculation Tool**: This is a tracking aid, not official record
- **Point Disputes**: Defer to CKC official determinations

#### Data Accuracy
- **Source Dependency**: Accuracy depends on CanuckDogs data quality
- **Complete Extraction**: System captures all available result lines
- **Manual Entry**: Some data may require manual verification
- **Formula Updates**: CKC may modify point calculations
- **Show Results**: Verify with official show superintendents

#### Technical Limitations
- **No Warranty**: Software provided "as-is" without guarantees
- **Data Loss**: No responsibility for lost or corrupted data
- **Compatibility**: May not work with all browser configurations
- **Updates**: No automatic updates or support provided

### Best Practices
- **Regular Backups**: Export reports regularly
- **Cross-Reference**: Verify with multiple sources
- **Stay Updated**: Check CKC for formula changes
- **Professional Use**: Consult with CKC for official matters

## 📞 Support

### Self-Help Resources
- **Demo Mode**: Use built-in examples to learn features
- **Formula Reference**: Built-in CKC calculation documentation
- **Visual Guides**: Color coding and labels throughout interface
- **Export Examples**: Sample reports demonstrate features

### Additional Information
- **CKC Website**: [Official Canadian Kennel Club](https://www.ckc.ca/en)
- **CanuckDogs**: [Competition Results Database](https://www.canuckdogs.com)
- **Show Superintendents**: Contact for official result verification

---

## 📄 License

This project is provided as-is for educational and tracking purposes. Always verify championship points with official CKC records before making title applications.

**Version**: 1.1  
**Last Updated**: December 2025  
**Compatibility**: Modern web browsers

---

*🐕 Happy tracking and congratulations on your championship journey! 🏆*

## 🚀 Installation

### Quick Start
1. **Download the HTML file** (`ckc_master_tracker.html`)
2. **Open in any modern web browser** (Chrome, Firefox, Safari, Edge)
3. **No additional software required** - runs entirely in browser

### Requirements
- Modern web browser with JavaScript enabled
- Internet connection (for fonts and styling)
- No server setup needed - works as standalone HTML file

### File Structure
```
ckc_master_tracker.html    # Main application file
README.md                  # This documentation
```

## 📖 Usage

### Getting Started
1. **Open the application** in your web browser
2. **Enter the dog's registered name** in the search field
3. **Click "Extract & Calculate Points"** to process data
4. **Navigate through tabs** to explore different views

### Demo Mode
- Try entering **"Miller"** to see the system with sample data
- Demonstrates all features with realistic competition results
- Shows calculation formulas and title progression

### Step-by-Step Workflow
```
Enter Dog Name → Extract Data → Calculate Points → Review Results → Export Reports
```

## 🧮 CKC Points Formula

### Base Points
| Achievement | Formula | Maximum |
|-------------|---------|---------|
| **Best of Breed** | min(dogs_defeated, 5) | 5 points |
| **Winners Dog/Bitch** | min(dogs_defeated, 5) | 5 points |

### Group Placement Bonuses
| Placement | Formula | Maximum |
|-----------|---------|---------|
| **Group 1st** | +min(dogs_defeated × 2, 40) | 40 points |
| **Group 2nd** | +min(dogs_defeated × 1.5, 30) | 30 points |
| **Group 3rd** | +min(dogs_defeated × 1, 20) | 20 points |
| **Group 4th** | +min(dogs_defeated × 0.5, 10) | 10 points |

### Special Bonuses
- **Best in Show**: +min(dogs_defeated × 5, 200) points
- **Specialty Shows**: ×1.5 multiplier on all points
- **All-Breed Shows**: Standard calculation

### Title Thresholds
| Title | Points Required |
|-------|-----------------|
| **Champion (CH)** | Prerequisite |
| **Grand Champion (GCH)** | 20+ points |
| **Grand Champion Excellent (GCHX)** | 100+ points |
| **Grand Master (GM)** | 200+ points |
| **Grand Master Supreme (GMS)** | 400+ points |

## 🖥️ Interface Overview

### Tab Navigation
The application features four main sections:

#### 📊 Points Dashboard
- **Total Points Display**: Large, prominent points counter
- **Title Progress**: Visual indicators for each title level
- **Recent Results**: Latest 8 competition results with calculations
- **Summary Statistics**: Key metrics and averages

#### 📅 Year-by-Year Progress
- **Year Cards**: Clickable cards showing annual point totals
- **Detailed Breakdown**: Complete results for selected year
- **Trend Analysis**: Progress tracking across multiple years
- **Performance Metrics**: Year-over-year comparisons

#### 📋 CanuckDogs Raw Data
- **Complete Data Table**: All extracted competition information
- **Sortable Columns**: Year, show, position, judge, points
- **Color Coding**: Highlights point-earning results
- **Data Verification**: Source data for transparency

#### 📄 Export Reports
- **PDF Generation**: Three report types available
- **Complete Documentation**: Calculations and supporting data
- **Professional Format**: Suitable for official submissions
- **Batch Export**: Multiple formats and detail levels

### Visual Elements
- **Color-Coded Results**: Green for points earned, gray for no points
- **Progress Bars**: Visual title progression indicators
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Professional Styling**: Clean, modern interface

## 📊 Data Sources

### Primary Input
- **CanuckDogs Format**: Extracts from standard CanuckDogs result displays
- **Competition Categories**: Conformation, Obedience, Rally Obedience
- **Multi-Year Support**: Handles results across multiple competition years

### Data Fields Extracted
- Show name and date range
- Judge information
- Placement/position achieved
- Competition day (Friday/Saturday/Sunday)
- Raw points from CanuckDogs display
- Dogs defeated (calculated from point formulas)

### Data Processing
- **Automatic Parsing**: Converts CanuckDogs format to structured data
- **Point Calculation**: Applies CKC formula to each result
- **Data Validation**: Checks for consistency and completeness
- **Error Handling**: Graceful handling of missing or invalid data

## 📋 Export Features

### Report Types

#### 1. Complete Championship Report
- **Full Competition History**: All results with calculations
- **Title Progress Timeline**: Achievement dates and progression
- **Formula Documentation**: CKC points calculation reference
- **Summary Statistics**: Totals, averages, and metrics

#### 2. Year-by-Year Progress Report
- **Annual Breakdowns**: Detailed yearly analysis
- **Trend Visualization**: Progress tracking over time
- **Performance Comparison**: Year-over-year metrics
- **Goal Tracking**: Points needed for next title level

#### 3. Points Verification Report
- **Calculation Transparency**: Show-by-show formula breakdown
- **Source Data**: Raw CanuckDogs information included
- **Audit Trail**: Complete calculation methodology
- **Official Reference**: CKC formula documentation

### Export Formats
- **PDF-Ready HTML**: Opens in new window for easy printing
- **Downloadable Files**: Automatically named with dog name and date
- **Professional Layout**: Suitable for official submissions
- **Print Optimization**: Formatted for standard paper sizes

## 🔧 Technical Details

### Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: CSS Grid, Flexbox, CSS Animations
- **Data Processing**: Pure JavaScript (no external dependencies)
- **Export**: HTML-to-PDF conversion ready

### Browser Compatibility
- **Chrome/Edge**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Full support
- **Mobile Browsers**: Responsive design support

### Performance
- **Lightweight**: Single HTML file under 50KB
- **Fast Loading**: No external dependencies
- **Offline Capable**: Works without internet after initial load
- **Memory Efficient**: Optimized for large datasets

### Data Security
- **Local Processing**: All calculations performed in browser
- **No Data Transmission**: Information stays on your device
- **Privacy Focused**: No tracking or analytics
- **Secure**: No server-side vulnerabilities

## 🛠️ Troubleshooting

### Common Issues

#### Data Not Loading
- **Check Dog Name**: Ensure exact registered name spelling
- **Try Demo Mode**: Use "Miller" to test functionality
- **Browser Compatibility**: Use modern browser version
- **JavaScript Enabled**: Verify JavaScript is not blocked

#### Incorrect Point Calculations
- **Verify Formula**: Check against official CKC documentation
- **Dogs Defeated**: Ensure accurate count from show results
- **Specialty Shows**: Confirm if 1.5x multiplier applies
- **Manual Verification**: Cross-check with CKC official records

#### Export Problems
- **Popup Blockers**: Disable for report generation
- **PDF Printing**: Use browser's print-to-PDF function
- **File Download**: Check download folder for exported files
- **Browser Settings**: Ensure downloads are enabled

### Data Quality
- **Source Accuracy**: Verify CanuckDogs data completeness
- **Date Formatting**: Ensure consistent date formats
- **Judge Names**: Check for spelling consistency
- **Show Names**: Verify complete show information

### Performance Issues
- **Large Datasets**: May slow with 100+ shows
- **Browser Memory**: Close other tabs for better performance
- **Mobile Devices**: May require horizontal orientation
- **Refresh Browser**: Clear cache if issues persist

## ⚠️ Disclaimer

### Important Notices

#### Official Verification Required
- **CKC Authority**: Always verify points with official CKC records
- **Title Applications**: Use official CKC documentation for submissions
- **Calculation Tool**: This is a tracking aid, not official record
- **Point Disputes**: Defer to CKC official determinations

#### Data Accuracy
- **Source Dependency**: Accuracy depends on CanuckDogs data quality
- **Manual Entry**: Some data may require manual verification
- **Formula Updates**: CKC may modify point calculations
- **Show Results**: Verify with official show superintendents

#### Technical Limitations
- **No Warranty**: Software provided "as-is" without guarantees
- **Data Loss**: No responsibility for lost or corrupted data
- **Compatibility**: May not work with all browser configurations
- **Updates**: No automatic updates or support provided

### Best Practices
- **Regular Backups**: Export reports regularly
- **Cross-Reference**: Verify with multiple sources
- **Stay Updated**: Check CKC for formula changes
- **Professional Use**: Consult with CKC for official matters

## 📞 Support

### Self-Help Resources
- **Demo Mode**: Use built-in examples to learn features
- **Formula Reference**: Built-in CKC calculation documentation
- **Visual Guides**: Color coding and labels throughout interface
- **Export Examples**: Sample reports demonstrate features

### Additional Information
- **CKC Website**: [Official Canadian Kennel Club](https://www.ckc.ca)
- **CanuckDogs**: [Competition Results Database](https://www.canuckdogs.com)
- **Show Superintendents**: Contact for official result verification

---

## 📄 License

This project is provided as-is for educational and tracking purposes. Always verify championship points with official CKC records before making title applications.

**Version**: 1.0  
**Last Updated**: December 2025  
**Compatibility**: Modern web browsers

---

*🐕 Happy tracking and congratulations on your championship journey! 🏆*
