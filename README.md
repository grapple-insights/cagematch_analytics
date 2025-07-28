Cagematch Analytics 📊  
[](https://github.com/bryansauka/pro_wrestling_analytics#pro-wrestling-events-analytics-dbt-project)  

This dbt project models professional wrestling event data from WWE and AEW spanning 2021-2025. It follows a classic star schema design for clean, scalable analytics-ready data with clear separation of staging, dimension, fact, and reporting layers.

📦 Project Overview  
[](https://github.com/bryansauka/pro_wrestling_analytics#-project-overview)  

Supports reporting, dashboards, and analysis for pro wrestling events including attendance, matches, locations, and dates. Designed for flexibility and ease of integration with BI tools.

🔧 Data Sources  
[](https://github.com/bryansauka/pro_wrestling_analytics#-data-sources)  

Built primarily from raw events and match data ingested into staging models.

🧱 Model Layers  
[](https://github.com/bryansauka/pro_wrestling_analytics#-model-layers)  

Organized following dbt best practices into:

- **Staging (models/stage/):** Prepares raw source data for downstream models.  
  - `stage_pro_wrestling_events.sql`: Raw wrestling events data.  
  - `stage_pro_wrestling_matches.sql`: Raw match data.

- **Dimension (models/dimensions/):** Business entities and attributes.  
  - `dim_event.sql`: Event details such as brand, event name, show number.  
  - `dim_arena.sql`: Unique arenas.  
  - `dim_location.sql`: Locations (city, state, country).  
  - `dim_date.sql`: Calendar date dimension.  
  - `dim_match.sql`: Match details including winner, stipulations, title changes.

- **Fact (models/facts/):** Event and match level business measures linked to dimensions.  
  - `fact_pro_wrestling_events.sql`: Attendance and event metrics.  
  - `fact_pro_wrestling_matches.sql`: Match-level metrics like duration.

- **Reporting (models/reporting/):** Denormalized tables for BI and dashboards.  
  - `report_pro_wrestling_events.sql`: Joins facts and dimensions for analysis-ready views.

🧪 Data Testing  
[](https://github.com/bryansauka/pro_wrestling_analytics#-data-testing)  

Uses dbt tests to enforce:  
- Uniqueness and non-null constraints on keys  
- Referential integrity between fact and dimension tables  

📄 Documentation  
[](https://github.com/bryansauka/pro_wrestling_analytics#-documentation)  

Models and columns are documented in `schema.yml`. Documentation is generated and viewable with dbt docs.

🚀 Usage  
[](https://github.com/bryansauka/pro_wrestling_analytics#-usage)  


🛠️ Customization  
[](https://github.com/bryansauka/pro_wrestling_analytics#-customization)  

- Add new dimensions or facts by placing models in the appropriate folders.  
- Update documentation and tests in `schema.yml`.  
- Extend reporting models with additional joins or calculated fields as needed.

📋 Best Practices  
[](https://github.com/bryansauka/pro_wrestling_analytics#-best-practices)  

- Keep dimension tables unique on business keys.  
- Validate fact table grain to avoid duplicates.  
- Document models thoroughly with tests for data quality.

🤝 Support & Contributions  
[](https://github.com/bryansauka/pro_wrestling_analytics#-support--contributions)  

For questions or contributions, contact Grapple Insights or open an issue in this repository.

Made with ❤️ and dbt, for comprehensive, scalable professional wrestling analytics.
