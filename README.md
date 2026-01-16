# Airbnb Data Analytics Project - Snowflake & Power BI

## 📋 Project Overview

This project is a comprehensive data analytics solution that leverages **Snowflake** as the cloud data warehouse and **Power BI** for interactive data visualization and business intelligence. The project focuses on analyzing Airbnb listing data to provide insights into property pricing, revenue patterns, host performance, and rating distributions across different neighborhoods in New York City.

The solution demonstrates end-to-end data engineering and analytics capabilities, from data ingestion and transformation in Snowflake to creating interactive dashboards in Power BI for business stakeholders.

## 🎯 Objectives

- **Data Warehousing**: Store and manage large-scale Airbnb listing data in Snowflake
- **Data Analysis**: Perform comprehensive analysis on property listings, pricing, and host performance
- **Business Intelligence**: Create interactive dashboards for executive decision-making
- **Data Visualization**: Provide multiple analytical views including executive summaries, price & revenue analysis, and rating & host insights

## 🏗️ Project Structure

```
Snowflake and Powerbi Project/
│
├── Airbnb Data.csv                    # Source dataset (38,235 records)
├── Airbnb-Project.pbix                 # Power BI report file
├── README.md                          # Project documentation
│
├── Images/                            # Dashboard screenshots
│   ├── Executive-view.PNG            # Executive summary dashboard
│   ├── LogicalModel diagram.png      # Database logical model
│   ├── price&revenue Analysis.PNG    # Price and revenue analysis view
│   └── rating&host view.PNG          # Rating and host performance view
│
└── Documentation/
    ├── Create+Table+Queries.docx      # SQL scripts for table creation
    ├── Populate+Table+Queries+Script.docx  # Data population scripts
    └── Model+view+and+code+for+DB+Diagram.docx  # Database schema documentation
```

## 🛠️ Technologies Used

### Data Warehouse
- **Snowflake**: Cloud-based data warehousing platform for scalable data storage and processing

### Business Intelligence
- **Power BI**: Microsoft's business analytics tool for data visualization and interactive reporting

### Data Format
- **CSV**: Comma-separated values file format for data exchange

## 📊 Dataset Description

The project uses an Airbnb listing dataset containing **38,235 records** with the following key attributes:

### Data Fields

| Field | Description | Data Type |
|-------|-------------|-----------|
| `HOST_ID` | Unique identifier for the host | Integer |
| `HOST_SINCE` | Date when host joined Airbnb | Date |
| `NAME` | Property listing name | String |
| `NEIGHBOURHOOD` | Neighborhood location (Manhattan, Brooklyn, Queens, etc.) | String |
| `PROPERTY_TYPE` | Type of property (Apartment, House, etc.) | String |
| `ROOM_TYPE` | Room category (Entire home/apt, Private room, Shared room) | String |
| `ZIPCODE` | Postal code of the property | String |
| `BEDS` | Number of beds in the property | Integer |
| `NUMBER_OF_RECORDS` | Record count indicator | Integer |
| `NUMBER_OF_REVIEWS` | Total number of reviews received | Integer |
| `PRICE` | Listing price per night | Decimal |
| `REVIEW_SCORES_RATING` | Average review rating score | Decimal |
| `CANCELLATION_POLICY` | Cancellation policy type (Strict, Moderate, Flexible) | String |
| `ALLOWS_PETS` | Whether pets are allowed (Yes/No) | Boolean |
| `OUTDOOR_SPACE` | Type of outdoor space (Rooftop, Balcony, Patio, Garden, None) | String |
| `PROPERTY_VIEW_TYPE` | View from property (City, Ocean, Mountain, Garden, None) | String |
| `HOST_LANGUAGE` | Primary language of the host | String |

### Data Coverage
- **Geographic Coverage**: Primarily New York City (Manhattan, Brooklyn, Queens)
- **Time Period**: Listings from 2008 onwards
- **Property Types**: Apartments, Houses, and other property types
- **Room Types**: Entire homes/apartments, Private rooms, Shared rooms

## 🚀 Setup Instructions

### Prerequisites

1. **Snowflake Account**
   - Access to a Snowflake account with appropriate privileges
   - Warehouse, database, and schema created

2. **Power BI Desktop**
   - Power BI Desktop installed (free download from Microsoft)
   - Power BI Pro license (for publishing to Power BI Service, optional)

3. **Data Access**
   - Access to the `Airbnb Data.csv` file

### Step 1: Snowflake Setup

1. **Create Database and Schema**
   ```sql
   -- Execute scripts from Create+Table+Queries.docx
   -- This will create the necessary tables in Snowflake
   ```

2. **Load Data into Snowflake**
   ```sql
   -- Execute scripts from Populate+Table+Queries+Script.docx
   -- This will populate the tables with data from Airbnb Data.csv
   ```

3. **Verify Data Load**
   ```sql
   SELECT COUNT(*) FROM <your_table_name>;
   -- Should return 38,235 records
   ```

### Step 2: Power BI Connection

1. **Open Power BI Desktop**
   - Launch Power BI Desktop application

2. **Connect to Snowflake**
   - Click "Get Data" → Search for "Snowflake"
   - Enter your Snowflake connection details:
     - Server: `your_account.snowflakecomputing.com`
     - Database: Your database name
     - Warehouse: Your warehouse name
   - Authenticate using your Snowflake credentials

3. **Load Data Model**
   - Select the tables you want to import
   - Click "Load" to import data into Power BI

4. **Open Existing Report** (Alternative)
   - Open `Airbnb-Project.pbix` directly
   - Update data source credentials if needed
   - Refresh the data connection

### Step 3: Refresh Data

- In Power BI Desktop, click "Refresh" to update data from Snowflake
- For scheduled refreshes, publish to Power BI Service and configure refresh schedules

## 📈 Dashboard Views

The project includes four comprehensive analytical views:

### 1. Executive View
**Location**: `Images/Executive-view.PNG`

A high-level executive dashboard providing:
- Key performance indicators (KPIs)
- Overall business metrics
- Summary statistics
- Quick insights for decision-makers

### 2. Price & Revenue Analysis
**Location**: `Images/price&revenue Analysis.PNG`

Detailed analysis focusing on:
- Price distribution across neighborhoods
- Revenue trends and patterns
- Price comparisons by property type
- Revenue optimization opportunities

### 3. Rating & Host View
**Location**: `Images/rating&host view.PNG`

Host and rating performance insights:
- Review score distributions
- Host performance metrics
- Rating trends over time
- Host language analysis
- Property quality indicators

### 4. Logical Model Diagram
**Location**: `Images/LogicalModel diagram.png`

Database schema visualization showing:
- Table relationships
- Data model structure
- Entity relationships
- Data flow architecture

## 🔍 Key Features

### Data Analysis Capabilities

1. **Geographic Analysis**
   - Neighborhood-level insights
   - Zip code distribution
   - Location-based pricing trends

2. **Property Analysis**
   - Property type comparisons
   - Room type analysis
   - Bed capacity insights
   - Outdoor space and view type impact

3. **Host Performance**
   - Host tenure analysis (HOST_SINCE)
   - Host language diversity
   - Host listing counts

4. **Pricing Intelligence**
   - Price range analysis
   - Price by property characteristics
   - Revenue potential assessment

5. **Quality Metrics**
   - Review score analysis
   - Review count trends
   - Rating distribution patterns

6. **Policy Analysis**
   - Cancellation policy impact
   - Pet-friendly property analysis
   - Policy preferences by market segment

## 📸 Screenshots

### Executive Dashboard
![Executive View](Images/Executive-view.PNG)

### Price & Revenue Analysis
![Price and Revenue Analysis](Images/price&revenue%20Analysis.PNG)

### Rating & Host Performance
![Rating and Host View](Images/rating&host%20view.PNG)

### Database Logical Model
![Logical Model](Images/LogicalModel%20diagram.png)

## 🔄 Data Refresh

### Manual Refresh
1. Open Power BI Desktop
2. Click "Refresh" button in the Home ribbon
3. Wait for data to update from Snowflake

### Scheduled Refresh (Power BI Service)
1. Publish the report to Power BI Service
2. Go to Dataset settings
3. Configure scheduled refresh (requires Power BI Pro/PPU license)
4. Set refresh frequency (daily, weekly, etc.)

## 📝 SQL Scripts Reference

The project includes documentation files with SQL scripts:

- **Create+Table+Queries.docx**: Contains DDL statements for creating tables in Snowflake
- **Populate+Table+Queries+Script.docx**: Contains DML statements for loading data
- **Model+view+and+code+for+DB+Diagram.docx**: Contains database schema documentation and views

Refer to these documents for:
- Table creation scripts
- Data loading procedures
- View definitions
- Database schema details

## 🎓 Learning Outcomes

This project demonstrates:

1. **Cloud Data Warehousing**: Setting up and managing data in Snowflake
2. **ETL/ELT Processes**: Data extraction, transformation, and loading
3. **Data Modeling**: Designing logical data models for analytics
4. **Business Intelligence**: Creating interactive dashboards in Power BI
5. **Data Visualization**: Best practices for presenting data insights
6. **End-to-End Analytics**: Complete analytics pipeline from raw data to insights

## 🔐 Security & Best Practices

- **Credentials Management**: Store Snowflake credentials securely
- **Data Privacy**: Ensure compliance with data privacy regulations
- **Access Control**: Implement appropriate role-based access in Snowflake
- **Version Control**: Use version control for SQL scripts and Power BI files
- **Documentation**: Maintain up-to-date documentation for all components

## 🚧 Future Enhancements

Potential improvements for the project:

- [ ] Real-time data streaming integration
- [ ] Advanced machine learning predictions
- [ ] Automated report scheduling and distribution
- [ ] Additional data sources integration
- [ ] Mobile-optimized dashboard views
- [ ] Custom DAX measures for advanced analytics
- [ ] Data quality monitoring and alerts
- [ ] Integration with other BI tools

## 📞 Support & Contact

For questions or issues related to this project:

1. Review the documentation files in the project directory
2. Check SQL scripts in the documentation files
3. Verify Snowflake connection settings
4. Ensure Power BI Desktop is up to date

## 📄 License

This project is for educational and demonstration purposes.

## 🙏 Acknowledgments

- Dataset: Airbnb listing data
- Tools: Snowflake, Power BI
- Documentation: Project-specific SQL scripts and diagrams

---

**Last Updated**: 2024  
**Project Status**: ✅ Completed  
**Version**: 1.0
