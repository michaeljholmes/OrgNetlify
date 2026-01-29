
# Organisation Chart

```mermaid
flowchart TB
    HOD[Head of Development]

    HOD --> TA[Technical Architect]
    HOD --> HOP[Head of Product]
    HOD --> HTO[Head of Technical Operations]

    HOD --> FT1

    subgraph FT1[Feature Team]
        direction TB
        TL[Team Lead]
        SFE[Senior Frontend Engineer]
        FE1[Frontend Engineers x3]
        SBE[Senior Backend Engineer]
        BE1[Backend Engineers x6]
        BI[BI Engineer]

        TL --> SFE
        SFE --- FE1
        FE1 --- SBE
        SBE --- BE1
        BE1 --- BI
    end

    subgraph PRODUCT[Product]
        direction TB
        PO[Product Owner]
        BA[BA x2]
        HOUIUX[Senior UI/UX]
        UX[UI/UX]


        PO --- BA
        HOUIUX --- UX
    end
    HOP --> PRODUCT

    subgraph PLATFORM_SERVICES[Platform Services]
        direction TB
        PE[Platform Engineer]
    end

    subgraph ITOPS[IT Operations]
        direction TB
        SA[SysAdmin]
    end

    subgraph PRODUCTION[Production Operations]
        direction TB
        POL[Production Operations Lead]
        PRODE[Production Engineers]

        POL --- PRODE
    end

    HTO --> PLATFORM_SERVICES
    HTO --> ITOPS
    HTO --> PRODUCTION
```

## Roles

- **Head of Development**: `Roles/HeadOfDevelopment.md`
- **Head of Product**: `Roles/Product/HeadOfProduct.md`
- **Technical Architect**: `Roles/TechnicalArchitect.md`
- **Team Lead**: `Roles/Development/TeamLead.md`
- **BA (Business Analyst)**: `Roles/Product/BA.md`
- **Product Owner**: `Roles/Product/ProductOwner.md`
- **UI/UX**: `Roles/Product/UIUX.md`
- **Senior UI/UX**: `Roles/Product/SeniorUIUX.md`
- **Senior Frontend Engineer**: `Roles/Development/SeniorFrontendEngineer.md`
- **Frontend Engineer**: `Roles/Development/FrontendEngineer.md`
- **Senior Backend Engineer**: `Roles/Development/SeniorBackendEngineer.md`
- **Backend Engineer**: `Roles/Development/BackendEngineer.md`
- **QA (Quality Assurance)**: `Roles/Product/QA.md`
- **Senior QA**: `Roles/Product/HeadOfQA.md`
- **Head of Technical Operations**: `Roles/TechnicalOperations/HeadOfTechnicalOperations.md`
- **SysAdmin**: `Roles/TechnicalOperations/SysAdmin.md`
- **Production Operations Lead**: `Roles/TechnicalOperations/ProductionOperationsLead.md`
- **DBA**: `Roles/TechnicalOperations/DBA.md`
- **Production Engineer**: `Roles/TechnicalOperations/ProductionEngineer.md`
- **Platform Engineer**: `Roles/TechnicalOperations/PlatformEngineer.md`
