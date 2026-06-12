# Streaming Platform Content Identity Research

## Project Overview

This project analyzes how major streaming platforms differentiate themselves through content identity strategies. Using data collected from the TMDB API, we explored how platforms such as Netflix, Hulu, HBO Max, Peacock, and Prime Video differ in:

* exclusivity strategy
* genre emphasis
* popularity
* perceived quality

The goal of the project was not simply to compare catalog sizes, but to understand how platforms position themselves strategically within the streaming market.

---

# Research Question

How do streaming platforms build distinct content identities through genre focus, exclusivity, popularity, and perceived quality?

---

# Data Acquisition

At the beginning of the project, our team wanted to work on a topic that could generate meaningful business insights rather than simply visualizing generic datasets. We decided to focus on streaming platforms because of the increasing competition among services such as Netflix, Hulu, HBO Max, Peacock, and Prime Video, as well as the strategic importance of content differentiation in the streaming industry.

The data acquisition process took significantly longer than we initially expected. One major challenge was that streaming platforms keep most of their internal business and user data private, which is understandable given the highly competitive nature of the industry. As a result, finding a reliable and sufficiently detailed public dataset became one of the first major obstacles of the project.

We initially explored datasets available on Kaggle after receiving suggestions from ChatGPT. However, many of the datasets we found were either outdated, incomplete, manually curated, or contained questionable/generated values that were not appropriate for a more analytical business-focused project. Because of this, we decided not to rely on pre-made Kaggle datasets.

Instead, we searched for a more reliable source and eventually discovered TMDB (The Movie Database), which provides a public API containing movie and TV metadata across multiple streaming platforms. We signed up for a TMDB developer account, obtained an API key, and used ChatGPT to help generate a Python script that could automatically collect and organize the data we needed into CSV format.

Using the TMDB API allowed us to build a more customized and up-to-date dataset tailored to our research question. The dataset included information such as:

* streaming platform availability
* genres
* popularity scores
* vote averages
* vote counts
* media type (movie vs TV show)

This approach also gave us more control over data cleaning, filtering, and feature engineering later in the project.

---

## Data Cleaning and Preparation

The data cleaning process was relatively simple because the data pulled from the TMDB API was already structured in a way that was easy to work with. After exporting the API results into a CSV file, we reviewed the dataset to check for missing values, inconsistent platform coverage, and fields that might affect the reliability of our visualizations.

During this review, we noticed that Disney+ had a large number of missing or zero values compared with the other platforms. While the other platforms each had around 400 rows of usable title information, Disney+ had only around 100 rows. Because this created an imbalance in sample size and could distort comparisons across platforms, we decided to remove Disney+ from the final dataset.

After removing Disney+, the final dataset included five platforms:

* Netflix
* Hulu
* HBO Max
* Peacock
* Prime Video

Once the dataset was cleaned, we imported the final CSV file into Tableau for visualization and dashboard development.

---

## Dashboard Planning and Analytical Design

One of the biggest challenges of the project was figuring out how to generate meaningful business insights from a relatively limited public dataset. While the TMDB API provided useful metadata, it did not include internal streaming metrics such as subscriber counts, watch time, retention, or revenue. Because of this, we needed to carefully think about what kinds of questions could realistically be answered using the data we had available.

To address this, we began by outlining potential business questions related to streaming platform strategy and content differentiation. We explored many different ideas while experimenting with the dataset in Tableau and discussing possible analytical directions. During this process, we focused on identifying patterns that could reveal how platforms position themselves differently within the streaming market.

Eventually, we developed a more detailed analytical framework centered around several key questions, including:

* How much do platforms rely on exclusive content?
* Which genres are overrepresented or underrepresented on each platform?
* Do platforms differ in popularity and perceived quality?
* How are platforms positioned relative to one another?

After finalizing the analytical direction, we mapped each question to an appropriate visualization type and planned the overall dashboard structure before building the final charts in Tableau. This process helped us move from simply displaying data to creating a dashboard that tells a more cohesive strategic story.

---

## Dashboard Design Process

The dashboard design process ended up taking much longer than we originally expected. While Tableau was useful for building the visualizations themselves, we found that its built-in design customization options were somewhat limited for creating the kind of polished and minimalistic dashboard aesthetic we wanted.

Because of this, we focused less on heavily styling the charts directly inside Tableau and instead spent more time thinking about overall layout, visual hierarchy, readability, and storytelling. One useful technique we discovered was that Tableau allows custom logos and icons to be imported as shapefiles, which allowed us to integrate streaming platform logos directly into the dashboard visuals.

We also used Canva extensively during the dashboard planning process to prototype layouts and presentation ideas outside of Tableau. In addition, we used ChatGPT to generate many example dashboard concepts and mockups to help us explore different design directions. This process involved multiple iterations as we experimented with:

* dashboard layouts
* chart placement
* spacing and visual hierarchy
* color palettes
* typography and readability
* balancing analytical depth with visual simplicity

One major challenge was avoiding overcrowding. Since the project involved many different charts and metrics, we needed to carefully decide which visuals deserved the most emphasis and how to guide the viewer through the dashboard naturally. We eventually settled on a more minimalistic layout inspired by modern business analytics dashboards and consulting-style presentations.

We also spent a significant amount of time selecting colors. Because the dashboard already contained many platform-specific colors, it was important to avoid making the overall design visually overwhelming. We experimented with several different palettes before ultimately selecting a softer, cleaner palette that maintained readability while still preserving platform identity distinctions.

---

## Project Limitations and Assumptions

One of the main limitations of this project was the lack of access to internal streaming platform data. Metrics such as subscriber counts, watch time, retention rates, recommendation system performance, and revenue are generally private and unavailable to the public. Because of this, our analysis relied primarily on publicly available metadata from the TMDB API.

Another limitation was that TMDB popularity scores are not direct measures of actual viewership. Instead, they function more as relative attention or engagement indicators based on user activity and platform interactions within TMDB. Similarly, weighted ratings represent perceived audience quality rather than objective measures of success.

We also assumed that titles available on multiple platforms represented “shared” content, while titles appearing on only one platform in our dataset represented “exclusive” content. However, actual licensing agreements and regional availability may differ in reality.

Additionally, streaming catalogs change constantly over time. Since the dataset was collected at a single point in time, the analysis should be interpreted as a snapshot of platform positioning rather than a permanent representation of each platform’s catalog strategy.

Finally, because Disney+ had significantly fewer usable observations and many missing values, we removed it from the analysis to maintain more balanced platform comparisons.

---

## Key Findings

* Streaming platforms differentiate themselves through combinations of exclusivity, genre emphasis, popularity, and perceived quality rather than competing identically.
* Netflix occupies the strongest premium mainstream position by combining high popularity with strong perceived quality.
* HBO Max demonstrates a more prestige-oriented positioning strategy focused on higher-quality content.
* Peacock appears to pursue the most differentiated positioning strategy among the platforms analyzed by avoiding direct competition in several dominant genres.
* No major platform strongly occupies the high-attention / lower-quality quadrant, suggesting a possible opportunity for future streaming entrants or alternative positioning strategies.

---

## Tools Used

* Python
* TMDB API
* Pandas
* Tableau
* Canva
* ChatGPT
* GitHub

---

## Authors

* Kenyee Liu
* Jingyi (Skye) Huang
