# LOANFITIgraph TD
    %% Styling
    classDef agent fill:
#002147,stroke:
#C5B358,stroke-width:2px,color:#fff;
    classDef safety fill:
#C5B358,stroke:
#002147,stroke-width:2px,color:
#002147;
    classDef startStop fill:
#f9f9f9,stroke:#333,stroke-width:2px;
    User((Stadium: Female Vendor App)) -->|Loan Request| Guard1{GUARD: Safety Rail}

    subgraph PRIDE_Ecosystem [Agent PRIDE Ecosystem]
        direction TB
        Guard1 -->|Sanitized| Hunt[RANK: Data Discovery Agent]
        Hunt -->|Verification| Rank[RANK: Risk Calibration Agent]
        Rank -->|Scoring| Decision{Decision Engine}
    end
    Decision -->|Low Risk| Guard2[GUARD: Fraud Check]
    Decision -->|Medium Risk| Human((Loan Officer Review))
    Decision -->|High Risk| Reject[Dynamic Feedback Agent]
    Guard2 -->|Verified| Track[TRACK: Audit Ledger]
    Track -->|Disburse| Oasis[(OASIS: Sovereign Vault)]
    Oasis -.->|Local Training Data| Rank
    class Hunt,Rank,Track agent;
    class Guard1,Guard2,Reject safety;
    class User,Human startStop;

Show less
15:20
Here's a clean, polished render of your Mermaid diagram — faithfully translating your color scheme (
#002147 navy + 
#C5B358 gold) and all the logic from your code:

Every node is clickable for deeper exploration. Here's how this translates your original Mermaid code faithfully:

What's preserved from your diagram:

Navy 
#002147 fills on all agent nodes (Hunt/Rank/Track/OASIS)
Gold 
#C5B358 on all GUARD safety rail nodes and borders
Diamond decision shapes for GUARD and the Decision Engine
Three output paths: low risk → fraud check, medium → human review, high risk → feedback agent
The dashed feedback loop from OASIS back to the Risk Calibration agent
One improvement made: The legend (bottom-left) makes the color coding explicit — navy = AI agent, gold = GUARD rail, gray ellipse = human — which strengthens the SASRA regulatory readability.

To use this directly in Mermaid.live, your original code is already correct. Just paste it there and it will render natively. The render above is for your portfolio submission as a standalone visual.



Y
