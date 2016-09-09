## Study Observation Units as a Table [/brapi/v1/studies/{studyDbId}/table] 
Scope: CORE.
Status: ACCEPTED. Implemented in Cassavabase, HIDAP and Germinate.
Notes: 
Implementation target date: after PAG2016
Retrieve the details of the study required for field data collection. Includes actual trait data.

###### Response data types
|Variable|Datatype|Description|Required|  
|------|------|------|:-----:|
|studyDbId|Long|internal DB id ||
|observationVariableDbId|Long | internal DB id for the traits measured ||
|observationVariableName|String| name of variable||
|data| object| List of lists, specifying the plotId, block, rep, germplasmId, and the phenotypic values||

### Retrieve study Observation Units as table [GET]

+ Parameters
    + studyDbId (required, string, `1`) ... Identifier of the study. Usually a number, could be alphanumeric.
    
+ Response 200 (application/json)

        {
            "metadata": {
                "pagination": {
                    "pageSize": 1,
                    "currentPage": 1,
                    "totalCount": 1,
                    "totalPages": 1
                },
                "status": null,
                "datafiles": []
            },
            "result" : {
                "headerRow": [ "year","studyDbId","studyName","locationDbId","locationName","germplasmDbId","germplasmName","observationUnitDbId","plotNumber","replicate","blockNumber", "observationTimestamp", "entryType", "X", "Y"],
                "observationVariableDbIds": [ "variable1Id", "variable2Id", "variable2Id"],  // for linking
                "observationVariableNames": [ "plant height", "fruit weight", "root weight" ],  // for display
                // the observationNames will follow the columns defined in the headerRow

                "data" :
                [
                    [1, 1, 1, "CIP1", ...],
                    [2, 1, 1, "CIP2", ...]
                ]
            }
        }
