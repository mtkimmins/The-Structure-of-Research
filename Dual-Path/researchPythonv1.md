**Longitudinal Project:** "The Atlas of Worlds" — A comprehensive Python-based research tool for ingesting, cleaning, analyzing, and visualizing exoplanetary data.

### Phase I: Data Structures & Control Flow

**Tier 1**
* **Tier Name:** The Star Count
* **New Concepts:** Lists, Basic `for` Loops
* **PART A: Side Quest:**
    * **The Puzzle:** Calculate the total energy output of a cluster of batteries.
    * **Synthetic Data:** `batteries = [15, 20, 10, 5, 25]`
    * **Deliverable:** A script that sums the list and prints "System Charged."
* **PART B: Main Build:**
    * **The Feature Goal:** Initialize the Atlas registry.
    * **Field Data Task:** Create a manual list of 5 real stars visible from your location (or from Wikipedia) with their apparent magnitudes.
    * **Deliverable:** A script that iterates through your star list and prints each name.

**Tier 2**
* **Tier Name:** The Metadata Tag
* **New Concepts:** Dictionaries, Key-Value Pairs
* **PART A: Side Quest:**
    * **The Puzzle:** Store the inventory of a space suit.
    * **Synthetic Data:** `suit = {"oxygen": 80, "water": 100, "patches": 2}`
    * **Deliverable:** A script that prints "Oxygen level is [value]."
* **PART B: Main Build:**
    * **The Feature Goal:** Convert the star registry to store detailed data.
    * **Field Data Task:** For your 5 stars, look up their spectral type (e.g., G2V) and distance in light years.
    * **Deliverable:** A list of dictionaries, where each dictionary represents one star containing `name`, `magnitude`, `type`, and `distance`.

**Tier 3**
* **Tier Name:** The Converter
* **New Concepts:** Functions, Arguments, Return Values
* **PART A: Side Quest:**
    * **The Puzzle:** Convert alien currency "Zorks" to USD.
    * **Synthetic Data:** `exchange_rate = 1.5`
    * **Deliverable:** A function `zork_to_usd(amount)` that returns the converted value.
* **PART B: Main Build:**
    * **The Feature Goal:** Standardize distance metrics in the Atlas.
    * **Field Data Task:** N/A (Use existing data).
    * **Deliverable:** A function `lightyears_to_parsecs(ly)` applied to every star in your dictionary list.

**Tier 4**
* **Tier Name:** The Habitable Filter
* **New Concepts:** `if/else` Conditionals, Comparison Operators
* **PART A: Side Quest:**
    * **The Puzzle:** Determine if a spaceship hatch is locked.
    * **Synthetic Data:** `hatch_status = "open"`
    * **Deliverable:** A script that prints "Danger!" if open, "Safe" if closed.
* **PART B: Main Build:**
    * **The Feature Goal:** Identify potential observation targets.
    * **Field Data Task:** Add a `visible_to_naked_eye` boolean to your data based on magnitude (< 6.0 is True).
    * **Deliverable:** A loop that only prints stars where `visible_to_naked_eye` is `True`.

**Tier 5**
* **Tier Name:** The Efficient Scan
* **New Concepts:** List Comprehensions
* **PART A: Side Quest:**
    * **The Puzzle:** Double the speed of all thrusters.
    * **Synthetic Data:** `speeds = [100, 200, 300]`
    * **Deliverable:** A one-line list comprehension resulting in `[200, 400, 600]`.
* **PART B: Main Build:**
    * **The Feature Goal:** Create a quick-access list of star names.
    * **Field Data Task:** N/A.
    * **Deliverable:** Use a list comprehension to extract just the `name` from your list of star dictionaries.

**Tier 6**
* **Tier Name:** The Glitch Patch
* **New Concepts:** Error Handling (`try/except`), Input Validation
* **PART A: Side Quest:**
    * **The Puzzle:** Divide rations among crew, avoiding division by zero if crew is 0.
    * **Synthetic Data:** `rations = 100`, `crew = 0`
    * **Deliverable:** A script that catches `ZeroDivisionError` and prints "No crew to feed."
* **PART B: Main Build:**
    * **The Feature Goal:** Safely calculate absolute magnitude.
    * **Field Data Task:** Add a "Ghost Star" to your list with missing distance data (None or 0).
    * **Deliverable:** A loop calculating absolute magnitude using the distance modulus formula, skipping stars with missing data gracefully.

### Phase II: File I/O & Persistence

**Tier 7**
* **Tier Name:** The Log Reader
* **New Concepts:** Reading Text Files (`open`, `.read()`, `.split()`)
* **PART A: Side Quest:**
    * **The Puzzle:** Decode a distress signal stored in a text file.
    * **Synthetic Data:** Create `signal.txt` containing: `SOS-HELP-NOW`
    * **Deliverable:** A script that reads the file and prints the content replacing hyphens with spaces.
* **PART B: Main Build:**
    * **The Feature Goal:** Move hardcoded data to external storage.
    * **Field Data Task:** Move your star dictionary data into a raw text file named `stars.txt` (comma-separated manually).
    * **Deliverable:** A script that parses `stars.txt` back into the list-of-dictionaries format.

**Tier 8**
* **Tier Name:** The Report Generator
* **New Concepts:** Writing Text Files (`.write()`, append mode `a`)
* **PART A: Side Quest:**
    * **The Puzzle:** Log a captain's entry.
    * **Synthetic Data:** `entry = "Stardate 4523.1: We found a cat."`
    * **Deliverable:** A script that appends this string to a file `logbook.txt`.
* **PART B: Main Build:**
    * **The Feature Goal:** Export analysis results.
    * **Field Data Task:** N/A.
    * **Deliverable:** A function that takes your filtered list of visible stars and writes their names to `observation_targets.txt`.

**Tier 9**
* **Tier Name:** The CSV Interface
* **New Concepts:** The `csv` library (reader/writer)
* **PART A: Side Quest:**
    * **The Puzzle:** Parse a roster of robot workers.
    * **Synthetic Data:** `robots.csv`: `ID,Model,Status\n1,T-800,Active`
    * **Deliverable:** A script using `csv.DictReader` to print the Model of the robot.
* **PART B: Main Build:**
    * **The Feature Goal:** Professional data ingestion.
    * **Field Data Task:** Download a real CSV subset (approx 50 rows) from the NASA Exoplanet Archive (focus on columns: `pl_name`, `hostname`, `disc_year`).
    * **Deliverable:** A script that reads the NASA CSV and stores it as a list of dictionaries.

**Tier 10**
* **Tier Name:** The JSON Uplink
* **New Concepts:** The `json` library (serialization/deserialization)
* **PART A: Side Quest:**
    * **The Puzzle:** Save the ship's configuration settings.
    * **Synthetic Data:** `config = {"shield_level": 100, "weapons": ["laser", "torpedo"]}`
    * **Deliverable:** A script that saves this dict to `ship_config.json`.
* **PART B: Main Build:**
    * **The Feature Goal:** Create a persistent state for the Atlas.
    * **Field Data Task:** N/A.
    * **Deliverable:** A script that converts the NASA CSV data into a JSON file for faster loading in future runs.

**Tier 11**
* **Tier Name:** The File System
* **New Concepts:** `os` and `pathlib` modules
* **PART A: Side Quest:**
    * **The Puzzle:** Check if a fuel tank file exists before filling it.
    * **Synthetic Data:** N/A (File manipulation).
    * **Deliverable:** A script that checks for `fuel.txt`; if missing, creates it.
* **PART B: Main Build:**
    * **The Feature Goal:** Organize the data library.
    * **Field Data Task:** Create subdirectories `data/raw` and `data/processed` on your computer.
    * **Deliverable:** A script that automatically moves your downloaded CSVs into `data/raw`.

### Phase III: The Pandas Revolution (Analysis)

**Tier 12**
* **Tier Name:** The DataFrame
* **New Concepts:** `pandas`, `DataFrame`, `read_csv`
* **PART A: Side Quest:**
    * **The Puzzle:** Load a scoreboard of alien sports.
    * **Synthetic Data:** `scores.csv`: `Team,Points\nMartians,50\nVenusians,40`
    * **Deliverable:** A script using `pd.read_csv()` to display the table.
* **PART B: Main Build:**
    * **The Feature Goal:** Refactor the Atlas core.
    * **Field Data Task:** Use the full NASA Exoplanet Archive CSV (thousands of rows).
    * **Deliverable:** Replace all previous list-of-dict logic with a single `df = pd.read_csv(...)` command.

**Tier 13**
* **Tier Name:** The Inspector
* **New Concepts:** `.head()`, `.info()`, `.describe()`, `.columns`
* **PART A: Side Quest:**
    * **The Puzzle:** Summarize the stats of a clone army.
    * **Synthetic Data:** `clones = pd.DataFrame({'height': [180, 182, 178], 'weight': [80, 82, 79]})`
    * **Deliverable:** Print the statistical summary of the clones using `.describe()`.
* **PART B: Main Build:**
    * **The Feature Goal:** Audit the downloaded data.
    * **Field Data Task:** N/A.
    * **Deliverable:** A report script that prints the column names, memory usage, and basic statistics of the planet radii and orbital periods.

**Tier 14**
* **Tier Name:** The Filter Array
* **New Concepts:** Boolean Indexing, Column Selection
* **PART A: Side Quest:**
    * **The Puzzle:** Find all red apples in a fruit crate.
    * **Synthetic Data:** `fruit = pd.DataFrame({'name': ['apple', 'banana', 'apple'], 'color': ['red', 'yellow', 'green']})`
    * **Deliverable:** Select rows where `name` is 'apple' AND `color` is 'red'.
* **PART B: Main Build:**
    * **The Feature Goal:** Search for Earth-like candidates.
    * **Field Data Task:** Identify the column headers for "Planet Radius" (usually `pl_rade`) and "Orbital Period" (`pl_orbper`).
    * **Deliverable:** Create a new DataFrame `candidates` containing only planets with a radius < 2.0 Earth radii.

**Tier 15**
* **Tier Name:** The Void Cleaner
* **New Concepts:** Handling Missing Data (`.dropna()`, `.fillna()`, `.isna()`)
* **PART A: Side Quest:**
    * **The Puzzle:** Fix a corrupted sensor log.
    * **Synthetic Data:** `log = pd.DataFrame({'temp': [20, None, 22]})`
    * **Deliverable:** Replace `None` with the mean temperature (21).
* **PART B: Main Build:**
    * **The Feature Goal:** Sanitize the dataset for research.
    * **Field Data Task:** N/A.
    * **Deliverable:** Drop all rows where the "Planet Mass" or "Distance" is missing from the main DataFrame.

**Tier 16**
* **Tier Name:** The Sorter
* **New Concepts:** Sorting Values (`.sort_values()`), Resetting Index
* **PART A: Side Quest:**
    * **The Puzzle:** Rank space racers by speed.
    * **Synthetic Data:** `racers = pd.DataFrame({'name': ['A', 'B'], 'speed': [500, 1000]})`
    * **Deliverable:** Sort the DataFrame by speed descending.
* **PART B: Main Build:**
    * **The Feature Goal:** Find the closest worlds.
    * **Field Data Task:** N/A.
    * **Deliverable:** Sort the cleaned DataFrame by "System Distance" (`sy_dist`) and display the top 10 closest exoplanets.

**Tier 17**
* **Tier Name:** The Feature Engineer
* **New Concepts:** Vectorized Operations, Creating New Columns
* **PART A: Side Quest:**
    * **The Puzzle:** Calculate area for a list of square panels.
    * **Synthetic Data:** `panels = pd.DataFrame({'side': [2, 4, 6]})`
    * **Deliverable:** Create column `area` by squaring the `side` column.
* **PART B: Main Build:**
    * **The Feature Goal:** Calculate planetary gravity.
    * **Field Data Task:** Use columns `pl_bmasse` (mass in Earths) and `pl_rade` (radius in Earths).
    * **Deliverable:** Create a new column `gravity_g` using the formula $M / R^2$ (approximation in Earth units).

**Tier 18**
* **Tier Name:** The Aggregator
* **New Concepts:** GroupBy, Aggregation Functions (`mean`, `count`, `sum`)
* **PART A: Side Quest:**
    * **The Puzzle:** Average scores by team color.
    * **Synthetic Data:** `games = pd.DataFrame({'color': ['red', 'blue', 'red'], 'score': [10, 20, 30]})`
    * **Deliverable:** Group by `color` and calculate mean score.
* **PART B: Main Build:**
    * **The Feature Goal:** Analyze discovery methods.
    * **Field Data Task:** Use the `discoverymethod` column.
    * **Deliverable:** Group the data by discovery method and count how many planets were found by each method (Transit, Radial Velocity, etc.).

**Tier 19**
* **Tier Name:** The Query
* **New Concepts:** String operations (`.str`), Complex Filtering
* **PART A: Side Quest:**
    * **The Puzzle:** Find all personnel with "Smith" in their name.
    * **Synthetic Data:** `staff = pd.DataFrame({'name': ['John Smith', 'Jane Doe', 'Agent Smith']})`
    * **Deliverable:** Filter rows where `name` contains "Smith".
* **PART B: Main Build:**
    * **The Feature Goal:** Focus on the Kepler mission.
    * **Field Data Task:** N/A.
    * **Deliverable:** Filter the dataset to find all planets where the `pl_name` starts with "Kepler".

### Phase IV: Visualization

**Tier 20**
* **Tier Name:** The Plotter
* **New Concepts:** `matplotlib.pyplot`, Basic Line/Scatter Plots
* **PART A: Side Quest:**
    * **The Puzzle:** Graph the trajectory of a rocket.
    * **Synthetic Data:** `time = [1, 2, 3]`, `altitude = [10, 40, 90]`
    * **Deliverable:** A simple line plot of Time vs. Altitude.
* **PART B: Main Build:**
    * **The Feature Goal:** Visualizing the planet population.
    * **Field Data Task:** N/A.
    * **Deliverable:** A scatter plot of Orbital Period (x-axis, log scale) vs. Planet Mass (y-axis, log scale).

**Tier 21**
* **Tier Name:** The Histogram
* **New Concepts:** Histograms, Binning, `plt.hist()`
* **PART A: Side Quest:**
    * **The Puzzle:** Visualize the distribution of astronaut ages.
    * **Synthetic Data:** `ages = [25, 30, 30, 35, 40, 40, 40, 50]`
    * **Deliverable:** A histogram showing the frequency of age ranges.
* **PART B: Main Build:**
    * **The Feature Goal:** Analyze planet size distribution.
    * **Field Data Task:** N/A.
    * **Deliverable:** A histogram of Planet Radii (restricted to radii < 10 Earths) to see if "Super-Earths" or "Mini-Neptunes" are more common.

**Tier 22**
* **Tier Name:** The Stylist
* **New Concepts:** Plot customization (Titles, Labels, Legends, Colors)
* **PART A: Side Quest:**
    * **The Puzzle:** Make the rocket graph look "Science-y".
    * **Synthetic Data:** Reuse Tier 20 data.
    * **Deliverable:** Add a black background, green lines, grid, and axis labels "Time (s)" and "Altitude (m)".
* **PART B: Main Build:**
    * **The Feature Goal:** Publication-ready charts.
    * **Field Data Task:** N/A.
    * **Deliverable:** Refine the Scatter Plot from Tier 20 to differentiate Discovery Method by color.

**Tier 23**
* **Tier Name:** The Seaborn Upgrade
* **New Concepts:** `seaborn` library, Boxplots/Violin Plots
* **PART A: Side Quest:**
    * **The Puzzle:** Compare fuel efficiency across different ship classes.
    * **Synthetic Data:** `data = pd.DataFrame({'class': ['A', 'A', 'B', 'B'], 'mpg': [10, 12, 5, 6]})`
    * **Deliverable:** A seaborn boxplot of MPG by Class.
* **PART B: Main Build:**
    * **The Feature Goal:** Compare planetary characteristics by discovery method.
    * **Field Data Task:** N/A.
    * **Deliverable:** A boxplot showing the distribution of "Planet Mass" for each "Discovery Method".

**Tier 24**
* **Tier Name:** The Dashboard
* **New Concepts:** Subplots (`plt.subplots`), Layouts
* **PART A: Side Quest:**
    * **The Puzzle:** Show engine temp and speed side-by-side.
    * **Synthetic Data:** `temp=[100, 110]`, `speed=[50, 60]`
    * **Deliverable:** A figure with 1 row and 2 columns of plots.
* **PART B: Main Build:**
    * **The Feature Goal:** The Atlas Summary View.
    * **Field Data Task:** N/A.
    * **Deliverable:** A single image containing 4 subplots: Mass vs Period, Radius Histogram, Distance Histogram, and Discovery Method Bar Chart.

### Phase V: Advanced Logic & Automation

**Tier 25**
* **Tier Name:** The Timekeeper
* **New Concepts:** `datetime` module, Timestamp parsing
* **PART A: Side Quest:**
    * **The Puzzle:** Calculate days since launch.
    * **Synthetic Data:** `launch = "2020-01-01"`
    * **Deliverable:** A script calculating the delta between today and launch date.
* **PART B: Main Build:**
    * **The Feature Goal:** Analyze discovery rates over time.
    * **Field Data Task:** Use the `disc_year` column.
    * **Deliverable:** Convert years to datetime objects (if needed) and plot a cumulative count of planets discovered per year.

**Tier 26**
* **Tier Name:** The Scientist
* **New Concepts:** `scipy` or `numpy` polynomial fitting (`polyfit`)
* **PART A: Side Quest:**
    * **The Puzzle:** Find the trend line of a growing bacteria culture.
    * **Synthetic Data:** `x=[1,2,3]`, `y=[2,4,6]`
    * **Deliverable:** Calculate the slope and intercept.
* **PART B: Main Build:**
    * **The Feature Goal:** Transit Depth analysis.
    * **Field Data Task:** Locate `pl_trandep` (Transit Depth) and `pl_rade` (Radius).
    * **Deliverable:** Perform a regression analysis to correlate transit depth with planet radius.

**Tier 27**
* **Tier Name:** The Architect
* **New Concepts:** Custom Modules, `import` from local files
* **PART A: Side Quest:**
    * **The Puzzle:** Move the currency converter to a utility file.
    * **Synthetic Data:** N/A.
    * **Deliverable:** `utils.py` contains the function; `main.py` imports and uses it.
* **PART B: Main Build:**
    * **The Feature Goal:** Modularize the Atlas.
    * **Field Data Task:** N/A.
    * **Deliverable:** Split your project into `loader.py` (data ingestion), `cleaner.py` (processing), and `visualizer.py` (plots).

**Tier 28**
* **Tier Name:** The Object
* **New Concepts:** Classes, Object-Oriented Programming (OOP)
* **PART A: Side Quest:**
    * **The Puzzle:** Create a blueprint for a Droid.
    * **Synthetic Data:** Class `Droid` with attribute `battery_level`.
    * **Deliverable:** Instantiate `r2` and `c3`, print their battery levels.
* **PART B: Main Build:**
    * **The Feature Goal:** Object-based Planet representation.
    * **Field Data Task:** N/A.
    * **Deliverable:** Define a class `Exoplanet` that takes a data row and calculates its own gravity and classification (e.g., "Jovian" or "Terrestrial") upon initialization.

**Tier 29**
* **Tier Name:** The Network
* **New Concepts:** `requests` library, APIs
* **PART A: Side Quest:**
    * **The Puzzle:** Get the current location of the ISS.
    * **Synthetic Data:** URL: `http://api.open-notify.org/iss-now.json`
    * **Deliverable:** A script that fetches and prints the latitude/longitude.
* **PART B: Main Build:**
    * **The Feature Goal:** Real-time data fetching.
    * **Field Data Task:** Use the NASA Exoplanet Archive TAP Service (API).
    * **Deliverable:** A script that fetches the latest 5 confirmed planets directly from NASA via HTTP request rather than reading a local CSV.

**Tier 30**
* **Tier Name:** The Scraper
* **New Concepts:** `BeautifulSoup`, HTML Parsing
* **PART A: Side Quest:**
    * **The Puzzle:** Extract headlines from a news mock-up.
    * **Synthetic Data:** `html = "<h1>Alien Found</h1>"`
    * **Deliverable:** A script extracting the text inside `<h1>`.
* **PART B: Main Build:**
    * **The Feature Goal:** Enrich data with context.
    * **Field Data Task:** Identify a Wikipedia page for a specific famous exoplanet (e.g., TRAPPIST-1).
    * **Deliverable:** A script that scrapes the introductory paragraph of the Wikipedia page to add a textual description to your planet data.

**Tier 31**
* **Tier Name:** The Vault
* **New Concepts:** `sqlite3`, SQL Queries
* **PART A: Side Quest:**
    * **The Puzzle:** Create a high-score table.
    * **Synthetic Data:** Table `scores` with columns `player`, `points`.
    * **Deliverable:** A script that creates the DB and inserts one row.
* **PART B: Main Build:**
    * **The Feature Goal:** The Final Database.
    * **Field Data Task:** N/A.
    * **Deliverable:** A script that reads your Cleaned Pandas DataFrame and exports it directly into a SQLite database file `atlas.db`, allowing for SQL querying of planets.

### Phase VI: The Capstone

**Tier 32**
* **Tier Name:** BOSS FIGHT: The Drake Equation Solver
* **New Concepts:** Synthesis of all previous tiers.
* **Objective:**
    1.  Fetch the absolute latest data from the NASA API.
    2.  Clean the data (handle nulls, convert units).
    3.  Store it in a local SQLite database.
    4.  Filter for "Potentially Habitable" planets (defined as: 0.5 < Radius < 1.5 Earths, inside the "Habitable Zone" calculated via stellar luminosity approximation).
    5.  Generate a PDF or Image Report showing:
        * A histogram of the radii of these habitable worlds.
        * A scatter plot of their distance vs. star brightness.
        * A ranked list of the top 5 candidates for transmission, exported to a text file.
    6.  **Constraint:** Use OOP (Classes) and Error Handling throughout.
* **Instructions:** None. Good luck.
