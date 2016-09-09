## Trait Details [/brapi/v1/traits/{traitDbId}]
Scope: CORE.
Status: ACCEPTED.

Implemented by: Germinate

Retrieve the variables associated to a trait 

+ Parameters
    + traitDbId (required, string, `464`) ... Id of the trait to retrieve details of.

### Retrieve trait details by id [GET]

+ Response 200 (application/json)

        {
            "metadata": {
                "pagination": {},
                "status": null,
                "datafiles": []
            },
            "result": {
                "traitDbId": "123",
                "traitId": "CO:123000007",
                "name": "Plant Height",
                "description": "Description of Plant Height",
                "observationVariables": [
                    "CO_334:0100121", 
                    "CO_334:0100122", 
                    "CO_334:0100123" 
                ],
                "defaultValue": null
            }
        }
