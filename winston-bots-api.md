
## Bots [/bots]

### List All Bots [GET]

+ Response 200 (application/json)

    + Headers
            Location: /bots

    + Body
    
            [
                {
                    name: String,
                    cid: String,
                    plan: String,
                    token: { type: String, required: true },
                    active: { type: Boolean, default: false },
                    subscribed: { type: Boolean, default: false },
                    limitToGID: { type: Boolean, default: false },
                    permissions: [String],
                    gid: String,
                }            
            ]


### Get A Bot By Id [GET]

+ Response 200 (application/json)

    + Headers
            Location: /bots?id=

    + Body
    
            {
                name: String,
                cid: String,
                plan: String,
                token: { type: String, required: true },
                active: { type: Boolean, default: false },
                subscribed: { type: Boolean, default: false },
                limitToGID: { type: Boolean, default: false },
                permissions: [String],
                gid: String,
            } 

### Create a Bot [POST]

Create a bot. It takes a JSON object.

+ Request (application/json)

    + Headers
            Location: /bots

    + Body
    
            {
            }

+ Response 201 (application/json)

    + Headers
            Location: /bots

    + Body

            {
            
            }


### Update Bots [PUT]

+ Request (application/json)

    + Headers
            Location: /bots

    + Body
    
            {
            }

+ Response 200 (application/json)

    + Headers
            Location: /bots

    + Body

            {
            
            }

### Update a Bot [PATCH]

+ Request (application/json)

    + Headers
            Location: /bots

    + Body
    
            {
            }

+ Response 201 (application/json)

    + Headers
            Location: /bots

    + Body

            {
            
            }

### Delete a Bot [DELETE]

+ Request (application/json)

    + Headers
            Location: /bots

    + Body
    
            {
            }

+ Response 200 (application/json)

    + Headers
            Location: /bots

    + Body

            {
            
            }
