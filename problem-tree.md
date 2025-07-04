flowchart TB
    %% Define styles
    classDef rootCause fill:#f9f9f9,stroke:#666,stroke-width:2px,color:#333
    classDef coreProblem fill:#ffcccc,stroke:#cc0000,stroke-width:3px,color:#000,font-weight:bold
    classDef consequence fill:#ccf,stroke:#00c,stroke-width:2px,color:#000
    classDef subCause fill:#e6f3ff,stroke:#4682b4,stroke-width:2px,color:#000
    classDef impact fill:#ffe6cc,stroke:#ff8c00,stroke-width:2px,color:#000
    classDef label fill:#fff,stroke:none,color:#666,font-style:italic

    %% Core Problem (Center)
    CoreProblem[PWDs continue to<br/>remain<br/>marginalized]:::coreProblem

    %% Root Causes Section
    RootLabel{Root Causes}:::label
    
    %% Primary Root Causes
    FragmentedServices([Fragmented<br/>Services]):::rootCause
    WeakNGO([Weak NGO<br/>capacities]):::rootCause
    LackCoordination([Lack of Coordinated<br/>Advocacy]):::rootCause

    %% Secondary Root Causes under Fragmented Services
    SiloedOps([Siloed Operations]):::subCause
    AbsenceKM([Absence of<br/>Centralized Knowledge<br/>Management]):::subCause
    InconsistentInfo([Inconsistent<br/>Information Flows]):::subCause
    InconsistentStandards([Inconsistent<br/>Standards &<br/>Approaches]):::subCause
    LimitedCollaboration([Limited Cross-Sector<br/>Collaboration]):::subCause

    %% Secondary Root Causes under Weak NGO capacities
    ResourceScarcity([Resource Scarcity<br/>and Funding Volatility]):::subCause
    OrgDevGaps([Organizational<br/>Development Gaps]):::subCause
    LimitedKnowledge([Limited Access to<br/>Knowledge Resources]):::subCause
    PeerLearning([Barriers to Peer<br/>Learning]):::subCause

    %% Secondary Root Causes under Lack of Coordinated Advocacy
    FragmentedEfforts([Fragmented<br/>Advocacy Efforts]):::subCause
    LimitedPolicy([Limited Access to<br/>Policy Spaces]):::subCause
    WeakNarrative([Weak Narrative and<br/>Public Awareness]):::subCause
    NoUnifiedVoice([No Unified<br/>Representative Voice<br/>in the Disability Space]):::subCause

    %% Consequences Section
    ConseqLabel{Consequences}:::label

    %% Primary Consequence Categories
    ForPWDs([For PWDs]):::consequence
    ForNGOs([For NGOs and<br/>Disability sector]):::consequence
    ForSociety([For Society]):::consequence

    %% Secondary Consequences under For PWDs
    LimitedAgency([Limited Agency and<br/>Voice]):::impact
    IneqAccess([Inequitable Access<br/>to Services]):::impact

    %% Secondary Consequences under For NGOs
    StagnantGrowth([Stagnant<br/>Organizational<br/>Growth]):::impact
    WeakPolicy([Weak Policy Impact]):::impact
    IneffUse([Inefficient Use of<br/>Resources]):::impact

    %% Secondary Consequences under For Society
    PerpDiscrim([Perpetuation of<br/>Stigma &<br/>Discrimination]):::impact
    MissedOpp([Missed Opportunities for Inclusive<br/>Development]):::impact
    ReducedCohesion([Reduced Social<br/>Cohesion]):::impact

    %% Connections - Root Causes to Core Problem
    RootLabel -.-> FragmentedServices
    RootLabel -.-> WeakNGO
    RootLabel -.-> LackCoordination
    
    FragmentedServices -->|due to| CoreProblem
    WeakNGO -->|due to| CoreProblem
    LackCoordination -->|due to| CoreProblem

    %% Connections - Secondary Root Causes
    SiloedOps --> FragmentedServices
    AbsenceKM --> FragmentedServices
    InconsistentInfo --> FragmentedServices
    InconsistentStandards --> FragmentedServices
    LimitedCollaboration --> FragmentedServices

    ResourceScarcity --> WeakNGO
    OrgDevGaps --> WeakNGO
    LimitedKnowledge --> WeakNGO
    PeerLearning --> WeakNGO

    FragmentedEfforts --> LackCoordination
    LimitedPolicy --> LackCoordination
    WeakNarrative --> LackCoordination
    NoUnifiedVoice --> LackCoordination

    %% Connections - Core Problem to Consequences
    CoreProblem -->|leading to| ForPWDs
    CoreProblem -->|leading to| ForNGOs
    CoreProblem -->|leading to| ForSociety

    ConseqLabel -.-> ForPWDs
    ConseqLabel -.-> ForNGOs
    ConseqLabel -.-> ForSociety

    %% Connections - Secondary Consequences
    ForPWDs --> LimitedAgency
    ForPWDs --> IneqAccess

    ForNGOs --> StagnantGrowth
    ForNGOs --> WeakPolicy
    ForNGOs --> IneffUse

    ForSociety --> PerpDiscrim
    ForSociety --> MissedOpp
    ForSociety --> ReducedCohesion
