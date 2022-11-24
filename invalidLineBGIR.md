# Invalid Line removal BGIR for Flowchart

## Important note GSS can not Modify lines on `BGIR`. For This lines, GSS will `review` the Activity and `Advice The Business Group`

## ! important Note After Login into MCH. Type BHDR and check The client ID if You find `EMXX`, `SVXX` or `24ZZ` Please `STOP` Immediately
```mermaid
flowchart TD
   A([Start MCH application \nlogin id: \npin+pass]) --> B([Select The Region as per User\nExample CI500])
   B --> C{Type BGIR hit Enter\n Enter the Detail\n FUND:\nASSET:\n 1DUE DATE\n INCOME INT/DIV : #}
   C --> |At Income = A|D([You Selected A i.e ALL\n 2It Will Display All the Status like O P F\n You can See all the Record])
   D --> E{Select The Record where Due Date Matches the Pay Date}
   E -->|YES| F[[3Select the record that satisfied the Above Condition\n Press 'd' to detail it]] 
   E -->|NO| G((4))

   F --> H{After Detailing Note down INC STATUS: and REPORT DT fields \n Check the Condition}
   H --> |if INC STATUS == O|I{IF \nINC STATUS == O\nAND\n6REPORT DATE is before the as-of Date of the report}
   I -->|YES| J{{We Close the Request by Saying comment i.e at page 23}}
   I -->|NO| K((5))
   H --> |if INC STATUS == P or F|L{IF \nINC STATUS == P or F\nAND\n6REPORT DATE is before the as-of Date of the report}
   L -->|YES| M[[If it Satisfied above condition \nTab Down to the INCOME RCVD:  field \n Input Y and hit Enter]]
   L -->|NO| N((5))

   M-->O{7Check REPORT DATE of Income Receipt\n IF \nThe Report date of income receipt is After the As-OF of the Interest Receivable report}
   O -->|YES| P{{Close the Request by Response in comment in page24}}
   O -->|NO| Q((5))
```
