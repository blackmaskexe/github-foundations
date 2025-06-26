
## Types of GitHub API:

|                                  |                                                  |                                                  |
| -------------------------------- | ------------------------------------------------ | ------------------------------------------------ |
|                                  | **REST API**                                     | **GraphQL API**                                  |
| **Design Philosophy**            | Resource-based. Different endpoints per resource | Single endpoint, query for precise data requests |
| **HTTP Methods**                 | Uses GET, POST, PUT, DELETE for operations       | Mainly uses POST for all operations              |
| **Data Fetching**                | Multiple requests for related data               | Single request for complex, related data         |
| **Over-fetching/Under-fetching** | Can have over-fetching or under-fetching         | Precise data fetching, no over/under-fetching    |
| **Performance**                  | Less efficient for complex systems               | More efficient for complex queries               |
| **Caching**                      | Easier due to HTTP methods                       | More challenging due to POST method              |
| **Learning Curve**               | Generally easier to learn                        | Steeper but offers powerful features             |
| **Flexibility**                  | Server-driven structure                          | Client-driven, highly flexible                   |
| **Versioning**                   | Often requires API versioning                    | Less need for versioning                         |
| **Ecosystem**                    | Mature, with extensive tools                     | Growing, with unique tools for queries           |
- allow you to access much of the data you could using GitHub CLI, but through an API (makes integration into your own apps much easier)