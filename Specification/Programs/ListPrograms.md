## Program list [/brapi/v1/programs?programName={programName}&abbreviation={abbreviation}&pageSize=&page=]
Call to retrieve a list of programs.

Status: ACCEPTED
Implemented By:

### List programs [GET]

+ Parameters
    + programName (optional, string, `Internation Yield Trial`) ... Filter by program name. Exact match.
    + abbreviation (optional, string, `IYT`) ... Filter by program abbreviation. Exact match.
    + pageSize (optional, integer, `23`) ... the number of programs to be reported per request
    + page (optional, integer, `292`) ... the response page requested

+ Response 200 (application/json)
        
        {
            "metadata" : {
                "pagination": {
                    "pageSize": 10,
                    "currentPage": 1,
                    "totalCount": 10,
                    "totalPages": 1
                },
                "status": null,
                "datafiles": []
            },
            "result" : {
                "data" : [
                    {
                        "programDbId": "123",
                        "name": "Wheat Resistance Program",
                        "abbreviation" : "DRP1",
                        "objective" : "Disease resistance",
                        "leadPerson" : "Dr. Henry Beachell"
                    },
                    {
                        "programDbId": "456",
                        "name": "Wheat Improvement Program",
                        "abbreviation" : "DRP2",
                        "objective" : "Yield improvement",
                        "leadPerson" : "Dr. Norman Borlaug"
                    }
                ]
            }
        }
