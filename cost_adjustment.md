# Cost Adjustment

## Tools Required

- MCH Access
- Snow Service Request

## User Requrements

- Which `month` -> Current or Previous
- FUND == CLIENT ACCT

## Logic for cost adjustment

```mermaid
flowchart TD
    A([Start]) --> B[[check for 1]]
    B --> C[[check for 2]]
    C --> D([Open MCH 3])
    D --> E([Type BCMC and Fill 4])
    E --> F{Check \n SECURITY COSTING\n Condition\n5}
    F --> |A|G([The Security is Avarage Costing])
    F --> |I|H([The Security is ID Costing])
    G --> I{CHECK\n BGMM/PMM is CLOSED\nAND\nAMONT <= 1000$ `dollers`\n6}
```

## Number represention for above logic steps



> ### 1. Before Starting the application check `BHDR` for client. If the Request if for funds with client ID `EMXX`, `PBHH`, `SVXX` or `24ZZ`- Stop immediately.



>### 2. The request Should not be processed between `2:00 PM and 6:30 PM ET`



> ### 3. Open `MCH` Login with Pass or PIN and Enter the Correct `Location` According to `USER`



> ### 4 Type `BCMC` And fill At Key 1
>
> > - CLIENT ACCT:
> > - FUNCTION : b
>
> ### Press ENTER and Press `D` next to `CLIENT ACCT`



> ### 5 Inside `BCMC` Screen you cannot see `SECURITY COSTING` Field So You need to go to `next` Page by `FWD` Button And Check The Field `SECURITY COSTING`



> ### 6
