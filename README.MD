The attached app.py file contains a code who's main goal is demonstrate the use of POST and GET request handlers in fastAPI in python.

***POST /person :

    Description: Creates a new person entry.

    Expected Behavior:

        -Accepts JSON data containing name, occupation, and address.

       -Validates that none of the fields are empty.

        -If validation passes, the person data is stored in the data list.

        -Returns a success response with the person data.

        -If validation fails, returns an error message indicating an invalid request.

    Expected Results:

        Example Request:

        POST /person
        {
        "name": "Beef Wellington",
        "occupation": "Fry Cook",
        "address": "124 Conch Street"
        }

        Expected Response:

        {
            "success": true,
            "result": {
                "name": "Beef Wellington",
                "occupation": "Fry Cook",
                "address": "124 Conch Street"
            }
        }

    Example Request:

        POST /person

            {
            "name": "Beef Wellington",
            "occupation": "",
            "address": "124 Conch Street"
            }   

        Expected Response

        {
        "success": false,
        "result": {
         "error_message": "invalid request"
        }
        }

*** GET /person

    Description: Retrieves all person entries stored in the system.

        Expected Behavior:

        -Returns a list of all stored person data in JSON format.

        -If no data is present, returns an empty list.

    Expected Results:

        Example Request: 

             GET /person

        Expected Response:

        [
    {
        "name": "Beef Wellington",
        "occupation": "Fry Cook",
        "address": "124 Conch Street"
    },
    {
        "name": "Beef Wellington",
        "occupation": "Fry Cook",
        "address": "124 Conch Street"
    }
]  

***Favourite Pokemon

MewTwo - Existential Crisis ---->  Eventual Redemption.
Also reminds me of Painwheel from Skullgirls
