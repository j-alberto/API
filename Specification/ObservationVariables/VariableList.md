## Variable list [/brapi/v1/variables?category={categoryName}]
Scope: CORE.
Status: ACCEPTED.

Call to retrieve a list of observationVariables available in the system.
`required` means the key has to be provided, but the value may be null.

### Variable list [GET]

+ Parameters
    + categoryName (required, string, `Phenology`) ... string containing the name of the category

+ Response 200 (application/json)

        {
            "metadata": {
                "pagination": {
                    "pageSize": 2,
                    "currentPage": 1,
                    "totalCount": 300,
                    "totalPages": 100
                },
                "status": null,
                "datafiles": []
            },
            "result": {
                "data": [{
                    "observationVariableDbId": "CO_334:0100632",
                    "name": "CT_M_C",
                    "ontologyDbId": "CO_334",
                    "ontologyName": "Cassava",
                    "trait": {
                        "traiDbId": "CO_334:0100630",
                        "name": "Canopy temperature"
                    },
                    "method": null,
                    "scale": null,
                    "defaultValue": null
                }, {
                  "observationVariableDbId": "CO_334:0100622",
                  "name": "caro_spectro",
                  "ontologyDbId": "CO_334",
                  "ontologyName": "Cassava",
                  "synonyms": ["Carotenoid content by spectro"],
                  "contextOfUse": ["Trial evaluation", "Nursery evaluation"],
                  "growthStage": "mature",
                  "status": "recommended",
                  "xref": "TL_455:0003001",
                  "institution": "",
                  "scientist": "",
                  "date": "2016-05-13",
                  "language": "EN",
                  "crop": "Cassava",
                  "trait": {
                      "traitDbId": "CO_334:0100620",
                      "name": "Carotenoid content",
                      "class": "physiological trait",
                      "description": "Cassava storage root pulp carotenoid content",
                      "synonyms": ["carotenoid content measure"],
                      "mainAbbreviation": "CC",
                      "alternativeAbbreviations": ["CCS"],
                      "entity": "root",
                      "attribute": "carotenoid",
                      "status": "recommended",
                      "xref": "TL_455:0003023"
                  },
                  "method": {
                      "methodDbId": "CO_334:0010320",
                      "name": "Visual Rating:total carotenoid by chart_method",
                      "class": "Estimation",
                      "description": "Assessment of the level of yellowness in cassava storage root pulp using the tc chart",
                      "formula": null,
                      "reference": null
                  },
                  "scale": {
                      "scaleDbId": "CO_334:0100526",
                      "name": "ug/g",
                      "datatype": "Numeric",
                      "decimalPlaces": 2,
                      "xref": null,
                      "validValues": {
                          "min": 1,
                          "max": 3,
                          "categories": ["1=low", "2=medium", "3=high"]
                      }
                  },
                  "defaultValue": null
                }]
            }
        }
