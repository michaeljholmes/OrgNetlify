
# Organisation Chart

```mermaid
flowchart TB
    HOD[Head of Development]

    HOD --> TA[Technical Architect]
    HOD --> HOP[Head of Product]
    HOD --> HPE[Head of Platform Engineering]

    HOD --> FT1

    subgraph FT1[Feature Team]
        direction TB
        TL[Team Lead]
        SFE[Senior Frontend Engineer]
        FE1[Frontend Engineers]
        SBE[Senior Backend Engineer]
        BE1[Backend Engineers]

        TL --> SFE
        SFE --- FE1
        FE1 --- SBE
        SBE --- BE1
    end

    subgraph PRODUCT[Product]
        direction TB
        PO[Product Owner]
        BA[BA's]
        HOUIUX[Senior UI/UX]
        UX[UI/UX]
        HOQA[Senior QA]
        QA2[QA's]

        PO --- BA
        HOUIUX --- UX
        HOQA --- QA2
    end
    HOP --> PRODUCT

    subgraph ITOPS[IT Operations]
        direction TB
        SA[SysAdmin]
    end
    subgraph PLATFORMTEAM[Platform Team]
        direction TB
        PFE[Platform Engineer]
    end
    subgraph OPSTEAM[Operations Team]
        direction TB
        HOO[Operation Lead]
        PE[Production Engineer]
        DBA[DBA]

        HOO --- PE
        PE --- DBA
    end

    HPE --> ITOPS
    HPE --> PLATFORMTEAM
    HPE --> OPSTEAM
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
- **Head of Platform Engineering**: `Roles/Platform/HeadOfPlatformEngineering.md`
- **SysAdmin**: `Roles/Platform/SysAdmin.md`
- **Operation Lead**: `Roles/Platform/OperationsLead.md`
- **DBA**: `Roles/Platform/DBA.md`
- **Production Engineer**: `Roles/Platform/ProductionEngineer.md`
- **Platform Engineer**: `Roles/Platform/PlatformEngineer.md`
