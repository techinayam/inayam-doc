# JSON to CSV Converter Tool

A powerful, feature-rich tool for converting JSON data to CSV format with advanced customization options and data analysis capabilities.

## Overview

The JSON to CSV Converter transforms JSON data into CSV format for easier data analysis, spreadsheet import, and data manipulation. It supports complex nested objects, arrays, and provides extensive customization options.

## Features

### Core Functionality
- **Real-time Conversion**: Auto-converts JSON to CSV as you type
- **Nested Object Flattening**: Handles complex nested JSON structures
- **Array Support**: Processes JSON arrays and nested arrays
- **Multiple Delimiters**: Support for comma, semicolon, tab, and pipe delimiters
- **Header Control**: Option to include/exclude headers in CSV output

### Display Options
- **Table View**: Interactive table display with sorting and filtering
- **CSV Text View**: Raw CSV text output for copying/editing
- **Data Preview**: Side-by-side comparison of JSON and CSV formats

### Advanced Features
- **Data Analysis**: Real-time statistics (rows, columns, processing time, file size)
- **Schema Detection**: Automatic detection of data types and structure
- **Search & Filter**: Filter data by column or search terms
- **Batch Processing**: Upload and merge multiple JSON files
- **Export Options**: Download as CSV, TSV, Excel, or JSON

### Data Transformation
- **JSON Formatting**: Auto-format and beautify JSON input
- **Data Sorting**: Sort data by any column
- **Data Slicing**: Preview with top 10 rows option
- **Null Handling**: Proper handling of null and undefined values

## How to Use

### Basic Usage

1. **Input JSON Data**
   - Paste JSON data into the input textarea
   - Upload JSON files using the file upload button
   - Use the sample data button to load example JSON

2. **Configure Settings**
   - **Show As**: Choose between table or CSV text view
   - **Delimiter**: Select CSV delimiter (comma, semicolon, tab, pipe)
   - **Options**: 
     - Top 10 Row: Show only first 10 rows in table view
     - Flatten Nested Objects: Convert nested objects to flat structure
     - Include Headers: Add column headers to CSV output

3. **View Results**
   - Table view: Interactive table with sorting and filtering
   - CSV view: Raw CSV text ready for copying or download

### Advanced Usage

#### Batch Processing
1. Click "Batch Upload" button
2. Select multiple JSON files
3. Files are automatically merged into a single dataset
4. Convert the combined data to CSV

#### Data Filtering
1. Enter search terms in the search box
2. Select specific columns to filter
3. Click "Apply" to filter the data
4. Export filtered results

#### Export Options
- **CSV**: Standard comma-separated values
- **TSV**: Tab-separated values
- **Excel**: Excel-compatible format
- **JSON**: Export processed JSON data

## Configuration Options

### Display Settings
```javascript
showas: 'table' | 'csv'  // Default: 'table'
```

### CSV Formatting
```javascript
delimiter: ',' | ';' | 'tab' | '|'  // Default: ','
```

### Processing Options
```javascript
options: [
  'slice',           // Show top 10 rows only
  'flattenNested',   // Flatten nested objects
  'includeHeaders'   // Include CSV headers
]
```

## Sample JSON Data

```json
{
  "users": [
    {
      "id": 1,
      "name": "John Doe",
      "email": "john@example.com",
      "age": 30,
      "address": {
        "street": "123 Main St",
        "city": "New York",
        "zipCode": "10001"
      },
      "hobbies": ["reading", "swimming"]
    },
    {
      "id": 2,
      "name": "Jane Smith",
      "email": "jane@example.com",
      "age": 25,
      "address": {
        "street": "456 Oak Ave",
        "city": "Los Angeles",
        "zipCode": "90210"
      },
      "hobbies": ["coding", "hiking"]
    }
  ]
}
```

## Output Examples

### With Flattened Objects
```csv
id,name,email,age,address.street,address.city,address.zipCode,hobbies
1,John Doe,john@example.com,30,123 Main St,New York,10001,"[""reading"",""swimming""]"
2,Jane Smith,jane@example.com,25,456 Oak Ave,Los Angeles,90210,"[""coding"",""hiking""]"
```

### Without Flattening
```csv
id,name,email,age,address,hobbies
1,John Doe,john@example.com,30,"{""street"":""123 Main St"",""city"":""New York"",""zipCode"":""10001""}","[""reading"",""swimming""]"
2,Jane Smith,jane@example.com,25,"{""street"":""456 Oak Ave"",""city"":""Los Angeles"",""zipCode"":""90210""}","[""coding"",""hiking""]"
```

## Keyboard Shortcuts

- **Ctrl+S** (Cmd+S): Save CSV file
- **Ctrl+F** (Cmd+F): Format JSON input
- **Ctrl+L** (Cmd+L): Load sample data
- **Ctrl+K** (Cmd+K): Clear all data

## Data Analysis Features

### Statistics Panel
- **Total Records**: Number of data rows processed
- **Total Columns**: Number of columns in output
- **Processing Time**: Conversion time in milliseconds
- **File Size**: Size of generated CSV data
- **Null Values**: Count of null/undefined values
- **Nested Objects**: Count of nested object structures
- **Arrays**: Count of array fields

### Schema Detection
Automatically detects and displays:
- Field names and data types
- Required vs optional fields
- Sample values for each field
- Data type icons (string 📝, number 🔢, boolean ✅, object 📦)

## Error Handling

### Common Errors
- **Invalid JSON**: Displays line and column of syntax errors
- **File Too Large**: 10MB file size limit
- **Conversion Errors**: Detailed error messages for processing issues

### Validation
- Real-time JSON syntax validation
- Error highlighting with line numbers
- Graceful handling of malformed data

## Browser Compatibility

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## File Size Limits

- **Single File**: 10MB maximum
- **Batch Upload**: No limit on number of files
- **Memory Usage**: Optimized for large datasets

## Tips & Best Practices

### Performance Optimization
- Use "Top 10 Row" option for large datasets preview
- Enable "Flatten Nested Objects" for complex JSON structures
- Use batch processing for multiple related files

### Data Quality
- Validate JSON before conversion
- Check for consistent data types across records
- Review schema detection results for data understanding

### Export Recommendations
- Use CSV for general spreadsheet applications
- Use TSV for tab-delimited requirements
- Use Excel format for Microsoft Office compatibility

## Troubleshooting

### Common Issues

**JSON Not Converting**
- Check JSON syntax validity
- Ensure proper quote escaping
- Verify bracket/brace matching

**Missing Data in Output**
- Enable "Flatten Nested Objects" for nested data
- Check if data is in array format
- Verify field names are consistent

**Performance Issues**
- Enable "Top 10 Row" for large datasets
- Use batch processing for multiple files
- Clear browser cache if memory issues occur

### Support

For technical support or feature requests, please contact our support team or visit our documentation portal.

---

*Last updated: 2024*