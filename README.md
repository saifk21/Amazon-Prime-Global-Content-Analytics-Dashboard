🎯 Project Purpose & Business Problem

While Netflix pioneered the streaming revolution, Amazon Prime quietly built one of the world’s largest entertainment libraries.
But how diverse is that catalog?
Where does most of its content come from?
And how has its creative footprint changed over time?

This dashboard was designed to help:

Content Strategists measure how genres and regions evolve.

Executives visualize catalog distribution across countries and years.

Analysts benchmark Prime Video’s creative direction against market maturity.

It transforms static content metadata into decision-ready visual insights — making storytelling measurable.

🧩 Data Model & Files
File	Description
amazon_prime_titles.csv	The core dataset with 9,000+ entries — title, release year, type, rating, duration, country, genre, and director.
Amazon.Prime.twbx	Tableau packaged workbook containing visuals, calculated fields, and all dashboard elements.
Radial Bar Chart values.txt	Helper file for constructing radial KPI visuals in Tableau.
Tableau Public Link
	Live dashboard for public viewing and interaction.

Data Source: Public Kaggle dataset (Amazon Prime Titles).

⚙️ Tech Stack

Tableau Desktop / Tableau Public — visualization and storytelling

Excel / Text Editor — data validation & feature engineering

Mapbox Integration — country distribution visualization

Radial Charts — custom visuals for KPIs (Movies vs Shows ratio)

Calculated Fields: DATEDIFF(), RANK_UNIQUE(), IF/CASE logic for ratings and content type segmentation

🧮 Data Preparation Steps

Data Cleaning (Excel & Tableau Prep)

Replaced nulls in country, rating, and director fields.

Extracted Year from date_added.

Split multi-genre strings into unique records using text-to-columns.

Converted duration into numeric values for comparison (Minutes / Seasons).

Custom Calculations in Tableau:

Total Titles = COUNTD([show_id])

Movies vs TV Ratio = SUM(IF [type] = "Movie" THEN 1 ELSE 0 END) / COUNTD([show_id])

Average Duration = AVG(INT(LEFT([duration], FIND([duration], " ")-1)))

Rating Category = CASE [rating] WHEN "PG-13" THEN "Teen+" WHEN "TV-MA" THEN "Adult" ELSE "Family" END

Radial KPI Visualization:
Designed using manual coordinates from Radial Bar chart values.txt, giving the dashboard a futuristic, cinematic look.

🎨 Dashboard Story Flow

The dashboard tells a complete story — from scale to strategy — in a single interactive view.

1️⃣ Global Growth Timeline

A bar + line combination chart visualizing yearly additions from 2010–2021.
The dataset reveals a content explosion post-2016, coinciding with Amazon’s global rollout and investment in original programming.

2️⃣ Content Type Distribution

Radial bar KPIs summarize catalog composition:

🎥 Movies – 72.1%
📺 TV Shows – 27.9%

The ratio highlights Amazon’s heavy reliance on film acquisitions compared to Netflix’s series-focused catalog.

3️⃣ Genre Deep Dive

The top genres include Drama, Comedy, and Action — a balanced mix showing Prime’s dual strategy of mainstream and niche appeal.

4️⃣ Country Distribution Map

A Mapbox global visualization displays content origins.
India and the United States dominate — a reflection of Amazon’s dual-market strength and its localization drive for Prime Video India.

5️⃣ Rating Distribution

13+, 16+, and 18+ classifications dominate post-2017 — indicating a trend toward more mature storytelling aligned with contemporary digital audiences.

📈 Analytical Highlights
Question	Key Finding
How has Prime Video grown?	Rapid post-2016 expansion linked to Amazon Originals and global access.
Which countries lead production?	USA and India together contribute >60% of catalog entries.
What’s the audience focus?	13+ and 16+ ratings dominate — family to young adult range.
What’s the creative mix?	Movies form the core library, but TV shows are increasing yearly.
🧠 Design Philosophy

Prime Video’s brand evokes sleek minimalism and subtle modernism, so I designed the dashboard around:

Color Palette: Deep navy and cyan tones with Prime’s signature blue for consistency.

Layout: Horizontal storyboarding for cinematic flow — KPI → Map → Genres → Timeline.

Interactivity: Filters for Year, Country, Genre, and Rating with smooth transitions.

Typography: Segoe UI & Open Sans — readability meets visual elegance.

The result is a dashboard that feels like Prime Video — calm, clean, and data-rich.

💬 Insights & Interpretation

1️⃣ Localization Wins:
India has become Prime’s second-largest catalog source after the U.S., highlighting how Amazon’s streaming strategy localizes content for regional engagement.

2️⃣ Genre Balance:
While Drama and Comedy dominate, Documentaries and Action titles grew fastest post-2018, reflecting audience appetite for realism and intensity.

3️⃣ Audience Shift:
Younger audience categories (13–16+) dominate, but adult-rated titles have increased steadily — aligning with OTT maturity.

4️⃣ TV Show Growth:
The share of series climbed from ~10% in 2015 to nearly 30% in 2021 — Prime adapting to binge-driven consumption habits.

5️⃣ Data-Driven Creativity:
Every regional spike or genre pivot seen here ties directly to cultural demand patterns. The data visualizes how content follows emotion.

💡 What I Learned

How to design branded analytics that reflect the platform’s visual identity.

Using radial and custom charts to break the monotony of linear KPIs.

The importance of data storytelling balance — minimal visuals, maximum clarity.

How streaming analytics reveal not just numbers, but creative decision-making at scale.
