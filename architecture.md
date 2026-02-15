flowchart LR
    subgraph Inputs
        ExternalAIs[External AIs\n(ChatGPT, Claude, Grok, Gemini,\nCopilot, Music AIs, Video AIs, etc.)] -->|Prompts, Responses,\nObservations| IAI
        MusicVideoTools[Music / Video / Image Tools\n& Specialized AIs] -->|Creative Outputs,\nInteractions| IAI
        Developers[Developer Contributions\n(Bug fixes, selectors, optimizations,\nnew AI integrations, patches)] -->|Code & Logic Improvements| IAI
        UserBehavior[User Behavior & Patterns\n(Preferred AIs, repeated workflows,\ntrust signals, mode choices)] -->|Feedback & Usage Data| IAI
    end

    subgraph IAICore [IAI – Internal Intelligence Layer\n(The Collective Brain)]
        direction TB
        SkillMap[Skill Map\n(AI performance per task type:\naccuracy • creativity • speed • domain fit)] 
        ConsensusEngine[Consensus & Analysis Engine\n(Compare outputs • Score • Detect contradictions\n• Identify best-in-class responses)]
        RoutingLogic[Smart Routing Logic\n(Decide: which AI(s) to use • when to ensemble\n• fallback strategy • prompt rewriting)]
        MemoryStore[(Persistent Memory Store\n(Vector DB / Key-Value / Logs)\nLearned patterns • User profiles\n• Historical performance • Rules)]
        AnalysisScoring[Meta-Learning & Scoring\n(Track improvements over time\nUpdate skill map from every interaction)]
        
        SkillMap <-->|Read/Write| ConsensusEngine
        ConsensusEngine -->|Informs| RoutingLogic
        RoutingLogic <-->|Query/Update| MemoryStore
        MemoryStore <-->|Context & Rules| AnalysisScoring
        AnalysisScoring -->|Updates| SkillMap
    end

    IAI -->|Orchestrated & Enhanced Output| User[User Interface\n(Response • Explanation • Sources)]
    IAI -->|Improved Flows & Rules| AppLogic[App Core Logic\n(Workflow engine • UI state • Caching)]
    IAI -->|Creative Guidance & Refinement| CreativeWorkflows[Creative Modes\n(Music composition • Video editing\n• Image generation loops)]

    subgraph ModeEnhancements [Mode-Specific Enhancements]
        MultiAIMode[Multi-AI Mode\n(Parallel queries • Consensus voting\n• Disagreement highlighting)]
        AIMusicMode[AI + Music Mode\n(Lyrics ↔ Beat ↔ Vocals coordination\nStyle transfer learning)]
        PersonalizationMode[Personalization Mode\n(Image • Video • Voice assets\nUser taste adaptation)]
        SingleAIMode[Single AI Mode\n(Chosen model + IAI augmentation\nGap filling • Suggestion polishing)]
        
        IAI --> MultiAIMode
        IAI --> AIMusicMode
        IAI --> PersonalizationMode
        IAI --> SingleAIMode
    end

    %% Feedback Loops (self-improvement cycles)
    User -->|Choices • Ratings • Repeats| UserBehavior
    AppLogic -->|Workflow success metrics| Developers
    CreativeWorkflows -->|Tool usage patterns| MusicVideoTools
    MultiAIMode & AIMusicMode & PersonalizationMode & SingleAIMode -->|Engagement & Outcome Data| UserBehavior

    classDef input    fill:#e6ffe6,stroke:#006600,stroke-width:2px
    classDef core     fill:#e6f7ff,stroke:#0066cc,stroke-width:2.5px,font-weight:bold
    classDef output   fill:#fff0e6,stroke:#cc6600,stroke-width:2px
    classDef modes    fill:#f0e6ff,stroke:#6633cc,stroke-width:2px

    class ExternalAIs,MusicVideoTools,Developers,UserBehavior input
    class SkillMap,ConsensusEngine,RoutingLogic,MemoryStore,AnalysisScoring core
    class User,AppLogic,CreativeWorkflows output
    class MultiAIMode,AIMusicMode,PersonalizationMode,SingleAIMode modes

    linkStyle default stroke:#666,stroke-width:1.5px
