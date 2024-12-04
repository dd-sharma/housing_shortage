# Data Dictionaries

## Housing Supply Data

#### Identification and Geographic Information

| Column     | Description                                       | Data Type | Example                        |
|------------|---------------------------------------------------|-----------|--------------------------------|
| `GEOID`    | A unique geographic identifier for counties.      | Integer   | `53021` (Franklin County, WA) |
| `NAME`     | Name of the county.                              | String    | `Franklin`                    |
| `STATE_NAME`| Name of the state where the county is located.   | String    | `Washington`                  |

#### Permit Data (2000–2022)

For each year from 2000 to 2022, the following columns are included:

| Column                         | Description                                                                 | Data Type | Example                        |
|--------------------------------|-----------------------------------------------------------------------------|-----------|--------------------------------|
| `ALL_PERMITS_[YEAR]`           | Total number of residential construction permits issued in the given year. | Float     | `281.0` (Franklin County, 2000) |
| `SINGLE_FAMILY_PERMITS_[YEAR]` | Number of permits issued for single-family residential constructions.      | Float     | `281.0` (Franklin County, 2000) |
| `ALL_MULTIFAMILY_PERMITS_[YEAR]` | Number of permits issued for multi-family residential constructions.       | Float     | `NaN` (Franklin County, 2000)  |

## Demand Data

### Population Growth & Demograhpics

#### Historical population

Units: Population values are in thousands.

| Column Name | Description                                                                 | Data Type | Example                                   |
|-------------|-----------------------------------------------------------------------------|-----------|-------------------------------------------|
| DATE        | The date associated with the population measurement.                     | String    | 2000-01-01                                |
| POPULATION  | Population value for a specific metropolitan statistical area (MSA).     | Float     | 4281.905 (represents thousands of people) |
| MSA         | The name of the Metropolitan Statistical Area (MSA).                     | String    | atlanta-sandy_springs-roswell             |

#### Projected population

Units: Population values are presented as raw counts of individuals.

| Column Name              | Description                                                                 | Data Type | Example             |
|--------------------------|-----------------------------------------------------------------------------|-----------|---------------------|
| Geographic Area      | The name of the Metropolitan Statistical Area (MSA).                       | String    | "Abilene, TX"       |
| Base Population (2020) | The baseline population for the year 2020.                                 | Float     | 176562.0            |
| Population 2020      | The actual population for the year 2020.                                   | Float     | 176883.0            |
| Population 2021      | The projected or actual population for the year 2021.                      | Float     | 177831.0            |
| Population 2022      | The projected or actual population for the year 2022.                      | Float     | 179665.0            |
| Population 2023      | The projected or actual population for the year 2023.                      | Float     | 181591.0            |

### Economic Indicators

#### Wages

Units: The wage data values are presented in dollars.

| Column Name          | Description                                                                                                   | Data Type | Example        |
|-----------------------|---------------------------------------------------------------------------------------------------------------|-----------|----------------|
| DATE             | The date of the wage measurement.                                                                             | String    | "2000-01-01"   |
| ENUC120640010SA  | Seasonally adjusted wage data for the Atlanta-Sandy Springs-Roswell MSA.                                       | Float     | 758.092970     |
| ENUC144640010SA  | Seasonally adjusted wage data for the Boston-Cambridge-Newton MSA.                                             | Float     | NaN            |
| ENUC169840010SA  | Seasonally adjusted wage data for the Chicago-Naperville-Elgin MSA.                                            | Float     | NaN            |
| ENUC191040010SA  | Seasonally adjusted wage data for the Dallas-Fort Worth-Arlington MSA.                                         | Float     | NaN            |
| ENUC264240010SA  | Seasonally adjusted wage data for the Houston-The Woodlands-Sugar Land MSA.                                    | Float     | NaN            |
| ENUC310840010SA  | Seasonally adjusted wage data for the Los Angeles-Long Beach-Anaheim MSA.                                      | Float     | NaN            |
| ENUC331040010SA  | Seasonally adjusted wage data for the Miami-Fort Lauderdale-West Palm Beach MSA.                               | Float     | NaN            |
| ENUC356240010SA  | Seasonally adjusted wage data for the New York-Newark-Jersey City MSA.                                         | Float     | NaN            |
| ENUC379840010SA  | Seasonally adjusted wage data for the Philadelphia-Camden-Wilmington MSA.                                      | Float     | NaN            |
| ENUC479040010SA  | Seasonally adjusted wage data for the Washington-Arlington-Alexandria MSA.                                     | Float     | NaN            |

#### Unemployment Rates

Units: The unemployment rate values are presented as percentages (%).

| Column Name  | Description                                                                                | Data Type | Example    |
|--------------|--------------------------------------------------------------------------------------------|-----------|------------|
| DATE     | The date of the unemployment rate measurement.                                             | String    | "2000-01-01" |
| ATLA013URN | Unemployment rate (%) for the Atlanta-Sandy Springs-Roswell MSA.                          | Float     | 3.23       |
| BOST625URN | Unemployment rate (%) for the Boston-Cambridge-Newton MSA.                                | Float     | NaN        |
| CHIC917URN | Unemployment rate (%) for the Chicago-Naperville-Elgin MSA.                               | Float     | NaN        |
| DALL148URN | Unemployment rate (%) for the Dallas-Fort Worth-Arlington MSA.                            | Float     | NaN        |
| HOUS448URN | Unemployment rate (%) for the Houston-The Woodlands-Sugar Land MSA.                       | Float     | NaN        |
| LOSA106URN | Unemployment rate (%) for the Los Angeles-Long Beach-Anaheim MSA.                         | Float     | NaN        |
| MIAM112URN | Unemployment rate (%) for the Miami-Fort Lauderdale-West Palm Beach MSA.                  | Float     | NaN        |
| NEWY636URN | Unemployment rate (%) for the New York-Newark-Jersey City MSA.                            | Float     | NaN        |
| PHIL942URN | Unemployment rate (%) for the Philadelphia-Camden-Wilmington MSA.                         | Float     | NaN        |
| WASH911URN | Unemployment rate (%) for the Washington-Arlington-Alexandria MSA.                        | Float     | NaN        |

### Migration

Units: Counts of individuals.

| Column Name  | Description                                                                 | Data Type | Example                        |
|--------------|-----------------------------------------------------------------------------|-----------|--------------------------------|
| NAME     | The name of the geographic area (usually Metropolitan Statistical Areas).   | String    | "San Luis Obispo-Paso Robles, CA" |
| B07201_014E | Number of people who moved into the MSA from abroad.                     | Float     | 899.0                         |
| B07201_013E | Number of people who moved within the same county of the MSA.            | Float     | 200.0                         |
| B07201_012E | Number of people who moved from one county to another within the MSA.    | Float     | 778.0                         |
| B07201_011E | Number of people who moved from a different MSA within the same state.   | Float     | 553.0                         |
| B07201_010E | Number of people who moved from a different MSA in a different state.    | Float     | 1331.0                        |
| B07201_009E | Number of people who moved from a rural area within the same state.      | Float     | 10085.0                       |
| B07201_008E | Number of people who moved from a rural area in a different state.       | Float     | 6401.0                        |
| B07201_007E | Number of people who moved from rural areas outside the U.S.             | Float     | 16486.0                       |
| B07201_006E | Number of people who stayed in the same house within the last year.      | Float     | 21954.0                       |
| B07201_005E | Number of people who moved within the same city or town.                 | Float     | 12722.0                       |
| B07201_004E | Number of people who moved to another city or town within the same state.| Float     | 34676.0                       |
| B07201_003E | Number of people who moved to another city or town in a different state. | Float     | 52693.0                       |
| B07201_002E | Total population who moved within the past year.                         | Float     | 183207.0                      |
| B07201_001E | Total population.                                                        | Float     | 236799.0                      |

### Affordability Metrics

#### Cost Burden

General Information
City: Name of the city, including state.
Year: Year range for the data (e.g., 2006–2010).

Each column corresponds to one of the metrics defined earlier, organized by housing category (owner/renter), income levels, and housing cost burden. Below is a breakdown of the column format:

Full Data Dictionary can be found on data source link under [Response Structure 'Click here for data dictionary'](https://www.huduser.gov/portal/dataset/chas-api.html). 

#### Rental and Housing Costs

**Rental Prices**

- The dataset contains one row per metro area.
- Each column (from `2015-01-31` to `2024-10-31`) represents the average rental price for a specific month in that metro area.
- Rental prices are represented as numerical values in dollars.

| **Column**   | **Description**                                                                 |
|--------------|---------------------------------------------------------------------------------|
| `RegionName` | Name of the metro area (e.g., "New York, NY").                                  |
| `YYYY-MM-DD` | Monthly rental price data for the specified date. Columns are formatted as dates (e.g., `2015-01-31`) and contain numerical values representing the average rental price in dollars. |

**Housing Prices**

- All monetary values are numerical and expressed in dollars.
- Percentage changes are represented in decimal format (e.g., 0.013 corresponds to 1.3%).

| **Column**                | **Description**                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| city                    | Name of the city and state where the data is collected (e.g., "Anaheim, CA").                       |
| Month of Period End     | The end date of the reporting period in "YYYY-MM-DD" format (e.g., "2012-01-01").                   |
| Median Sale Price       | Median sale price of homes during the reporting period (numerical, in dollars).                    |
| Median Sale Price MoM   | Month-over-month percentage change in the median sale price (numerical, expressed as a decimal).    |
| Median Sale Price YoY   | Year-over-year percentage change in the median sale price (numerical, expressed as a decimal).      |
| Homes Sold              | Total number of homes sold during the reporting period (integer).                                   |
| Homes Sold MoM          | Month-over-month percentage change in the number of homes sold (numerical, expressed as a decimal).|
| Homes Sold YoY          | Year-over-year percentage change in the number of homes sold (numerical, expressed as a decimal).  |
| New Listings            | Number of newly listed homes during the reporting period (integer).                                |
| New Listings MoM        | Month-over-month percentage change in the number of new listings (numerical, decimal format).      |
| New Listings YoY        | Year-over-year percentage change in the number of new listings (numerical, decimal format).        |
| Inventory               | Total inventory of homes available for sale during the reporting period (integer).                 |
| Inventory MoM           | Month-over-month percentage change in the inventory (numerical, decimal format).                  |
| Inventory YoY           | Year-over-year percentage change in the inventory (numerical, decimal format).                    |
| Days on Market          | Average number of days homes stayed on the market during the reporting period (numerical).         |
| Days on Market MoM      | Month-over-month change in the average days on market (numerical).                                 |
| Days on Market YoY      | Year-over-year change in the average days on market (numerical).                                   |
| Average Sale To List    | Ratio of the sale price to the list price (numerical, expressed as a decimal).                     |
| Average Sale To List MoM| Month-over-month change in the average sale-to-list ratio (numerical, decimal format).             |
| Average Sale To List YoY| Year-over-year change in the average sale-to-list ratio (numerical, decimal format).               |


