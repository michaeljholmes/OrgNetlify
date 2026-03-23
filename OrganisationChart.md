# Organisation Chart

> **Info:** There are 28 roles and 1 external role. Totalling a team of 29.

```mermaid
%%{init: {'themeVariables': {'fontSize': '10px'}, 'flowchart': {'nodeSpacing': 10, 'rankSpacing': 5}}}%%
flowchart TB
    HOD[Head of Development]

    HOD --> TA[Technical Architect]
    HOD --> HOP[Head of Product]
    HOD --> HTO[Head of Technical Operations]

    HOD --> ET1

    subgraph ET1[Engineering Team]
        direction TB
        TL[Team Lead]
        SFE[Senior Frontend Engineer]
        FE1[Frontend Engineers x4]
        SBE[Senior Backend Engineer]
        BE1[Backend Engineers x6]
        BI[BI Engineer]

        TL --> SFE
        SFE --- FE1
        FE1 --- SBE
        SBE --- BE1
        BE1 --- BI
    end

    subgraph PRODUCT[Product Team]
        direction LR

        subgraph PRODUCT_REQ[Product]
            direction TB
            PO[Product Owner]
            BA[BA]
            EBA[External BA]

            PO --- BA
            PO --- EBA
        end

        subgraph PRODUCT_UX[Design]
            direction TB
            HOUIUX[Senior UI/UX]
            UX[UI/UX]

            HOUIUX --- UX
        end

        PRODUCT_REQ --- PRODUCT_UX
    end
    HOP --> PRODUCT

    classDef externalBa fill:#FFE6CC,stroke:#C97C00,color:#000;
    class EBA externalBa;

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
        DBA[DBA]

        POL --- PRODE
        PRODE --- DBA
        DBA --- O1D[Maintenance Developer]
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
- **BI Engineer**: `Roles/Development/BIEngineer.md`
- **BA (Business Analyst)**: `Roles/Product/BA.md`
- **Product Owner**: `Roles/Product/ProductOwner.md`
- **UI/UX**: `Roles/Product/UIUX.md`
- **Senior UI/UX**: `Roles/Product/SeniorUIUX.md`
- **Senior Frontend Engineer**: `Roles/Development/SeniorFrontendEngineer.md`
- **Frontend Engineer**: `Roles/Development/FrontendEngineer.md`
- **Senior Backend Engineer**: `Roles/Development/SeniorBackendEngineer.md`
- **Backend Engineer**: `Roles/Development/BackendEngineer.md`
- **Maintenance Developer**: `Roles/TechnicalOperations/MaintenanceDeveloper.md`
- **Head of Technical Operations**: `Roles/TechnicalOperations/HeadOfTechnicalOperations.md`
- **SysAdmin**: `Roles/TechnicalOperations/SysAdmin.md`
- **Production Operations Lead**: `Roles/TechnicalOperations/ProductionOperationsLead.md`
 - **DBA**: `Roles/TechnicalOperations/DBA.md`
- **Production Engineer**: `Roles/TechnicalOperations/ProductionEngineer.md`
- **Platform Engineer**: `Roles/TechnicalOperations/PlatformEngineer.md`
