The Hiring proect is to help keep track of candidates state in the hiring process.


```mermaid
erDiagram
    Candidate ||--o{ Interview : "" 
    Position ||--|{ InterviewSequence : adv
    Candidate {
        int id
        string name
        int stateId
        string resume
        string project
        int positionId
    }
    Interview {
        int id
        string interviewee
        date interviewedOn
        int rating
    }
    State {
        int id
        int sequence
        int description
    }
    Position {
        int id
        string title
        string description
    }
    InterviewSequence {
        int id
        int sequence
        int stateId
    }

```

## State
* Applied
* Initial Email Sent
* Scheduled Initial Call
* Waiting for Project
* Reviewing Project
* Scheduling Interview
* Tecnical Interview Scheduled
* Team Interview Scheduled
* Final Interview
* Extend Offer
* Accepted
* Declined
* Other Offer
* Didn't Reply or Show

## Rating
1 - Strong No
2 - Weak No
3 - Meh
4 - Weak Yes
5 - Strong Yes