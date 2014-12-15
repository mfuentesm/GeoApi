FORMAT: 1A
HOST: http://www.lan.com

# Geo.
LATAM's geographic API


## Places [/ws/api/geo/1.0/places/{id}/type/{type}/code/{code}/ancestor_type/{ancestor_type}/ancestor_code/{ancestor_code}]


## GET

+ Parameters

    + id (optional, string) ... Id of the place.
    + type (optional, string) ... Type of the place (continent, country, region, city or airport).
    + code (optional, string) ... Alphabetical code assigned to the place.
    + ancestor_type (optional, string) ... Type of the ancestor of the place (continent, country, region, city or airport).
    + ancestor_code (optional, string) ... Alphabetical code assigned to the ancestor of the place.



+ Request (application/json)

    + Headers

                trackId     : 9c1c3785-bdb0-45fe-bcf9-d5605a97e1cb
                flowId      : 5830492
    
    + Body

            {
              "language": "ES",
              "country": "CL",
              "application": "compra",
              "portal": "personas",
              "type": "airport",
              "ancestor_type": "city",
              "ancestor_code": "SCL"
            }

       
+ Response 200 (application/json)

    + Headers

                trackId     : 9c1c3785-bdb0-45fe-bcf9-d5605a97e1cb
                flowId      : 5830492

    + Body

                {
                  "data": {
                    "places": [
                      {
                        "id": "2c05f2ee0a17497d",
                        "name": "A. MERINO BENITEZ INTL",
                        "code": "SCL",
                        "type": "airport",
                        "location": {
                          "latitude": -33.3892492,
                          "longitud": -70.79442159999996
                        }
                      }
                    ]
                  },
                  "status": {
                    "code": 200
                  }
                }

+ Response (application/json)

        {"status":{"code":500,"message":"Fatal error"}}

+ Response (application/json)

        {"status":{"code":501,"message":"No paso la validacion del apellido o record locator, intente de nuevo"}}

+ Response (application/json)  

        {"status":{"code":502,"message":"Error llamando al servicio, trate en un rato" }}

+ Response (application/json)

        {"status":{"code":503,"message":"No disponible el checkin" }}

+ Response (application/json)

        {"status":{"code":510,"message":"Reserva inhibida para checkin"}}

+ Response (application/json)

        {"status":{"code":520,"message":"Request invalido"}}

+ Response (application/json)

        {"status":{"code":521,"message":"Redirigiendo a sitio tam", "url" : "tam.com.br/supercheckindetam"}}

+ Response (application/json)

        {"status":{"code":530,"message":"Reserva de grupo, pedir ingreso foid o eticket"}}


