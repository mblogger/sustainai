graph TD
    subgraph External_Data_Sources [India Open Data Stack]
        A1[data.gov.in: AQI API] --> B[Data Ingestion Agent]
        A2[CGWB: Groundwater Levels] --> B
    end

    subgraph Kiro_Core_Logic [SustainAI Core]
        B --> C{Compliance Engine}
        D[Building Design Specs] --> C
        C -- Validates against --> E[GRIHA Standards]
        C -- Validates against --> F[NBC 2016 Guidelines]
    end

    subgraph Visualization [ULB Dashboard]
        C --> G[Carbon Footprint Analytics]
        C --> H[Water Saving Metrics]
        G & H --> I[Sustainability Scorecard]
    end
