
Endpoints :
1. Post /register
2. Post /login
3. Get /products
4. Get /mycart
5. Patch /checkout
6. Get /delivery/cities
7. Post /delivery/fee
8. Post /generate-midtrans-token
9. Delete /mycart/:id
10. Post /products/:productId

&nbsp;
# 1. Post /register
        Request:
            body:
                {
                    "username": "string",
                    "email": "string",
                    "password": "string",
                }
        Response(201-Created)
            {
                "id": "integer",
                "username": "string",
                "email": "string",
                "password": "string",
            }
        Response(400 - Bad Request)
            {
                 "message": "Username is required"
            }
            OR
            {
                 "message": "Email is required"
            }
            OR
            {
                "message": "Password is required"
            }
&nbsp;
# 2. POST /login

## Request:

### body:
```json 
{
    "email": "string",
    "password":"string"
}

```
## Response (201-Created)

```json 

    {
        "email": "string",
        "password":"string"
    }
```

## Response (400 - Bad Request)

```json
    {
            "message": "Email is required"
    }
    OR
    {
            "message": "Password is required"
    }

```

&nbsp;
# 3. Get /products
Description: get all products from 3rd party API 

## Request
### headers:
```json
{
    "access_token": "string"
}

```
### Response (200 - OK)
```json
[
    {
        "id": 1048,
            "brand": "colourpop",
            "name": "Lippie Pencil",
            "price": "5.0",
            "price_sign": "$",
            "currency": "CAD",
            "image_link": "https://cdn.shopify.com/s/files/1/1338/0845/collections/lippie-pencil_grande.jpg?v=1512588769",
            "product_link": "https://colourpop.com/collections/lippie-pencil",
            "website_link": "https://colourpop.com",
            "description": "Lippie Pencil A long-wearing and high-intensity lip pencil that glides on easily and prevents feathering. Many of our Lippie Stix have a coordinating Lippie Pencil designed to compliment it perfectly, but feel free to mix and match!",
            "rating": null,
            "category": "pencil",
            "product_type": "lip_liner",
            "tag_list": [
                "cruelty free",
                "Vegan"
            ],
            "created_at": "2018-07-08T23:45:08.056Z",
            "updated_at": "2018-07-09T00:53:23.301Z",
            "product_api_url": "https://makeup-api.herokuapp.com/api/v1/products/1048.json",
            "api_featured_image": "//s3.amazonaws.com/donovanbailey/products/api_featured_images/000/001/048/original/open-uri20180708-4-13okqci?1531093614",
            "product_colors": [
                {
                    "hex_value": "#B28378",
                    "colour_name": "BFF Pencil"
                },
                {
                    "hex_value": "#A36B5E",
                    "colour_name": "951 Pencil"
                },
                {
                    "hex_value": "#966A60",
                    "colour_name": "Beeper Pencil"
                },
                {
                    "hex_value": "#8F5954",
                    "colour_name": "Oh Snap Pencil"
                },
                {
                    "hex_value": "#975348",
                    "colour_name": "Curvii Pencil"
                },
                {
                    "hex_value": "#865B69",
                    "colour_name": "Lumiere Pencil"
                },
                {
                    "hex_value": "#8E474D",
                    "colour_name": "Bumble Pencil"
                },
                {
                    "hex_value": "#5F2820",
                    "colour_name": "BFF Pencil 3"
                },
                {
                    "hex_value": "#C095BC",
                    "colour_name": "Brills Pencil"
                },
                {
                    "hex_value": "#743A6A",
                    "colour_name": "Are N Be Pencil"
                },
                {
                    "hex_value": "#965564",
                    "colour_name": "Contempo Pencil"
                },
                {
                    "hex_value": "#BF2C7E",
                    "colour_name": "Heart On Pencil"
                },
                {
                    "hex_value": "#CE435D",
                    "colour_name": "Trixie Pencil"
                },
                {
                    "hex_value": "#DA6952",
                    "colour_name": "Chi Chi Pencil"
                },
                {
                    "hex_value": "#A33C37",
                    "colour_name": "Clique Pencil"
                },
                {
                    "hex_value": "#C23D3C",
                    "colour_name": "Frenchie Pencil"
                },
                {
                    "hex_value": "#AF4051",
                    "colour_name": "Bossy Pencil"
                },
                {
                    "hex_value": "#914B4C",
                    "colour_name": "Wild Nothing Pencil"
                },
                {
                    "hex_value": "#6D414B",
                    "colour_name": "Dopey Pencil"
                },
                {
                    "hex_value": "#4D2D28",
                    "colour_name": "Toolips Pencil"
                },
                {
                    "hex_value": "#361927",
                    "colour_name": "Mamacita Pencil"
                },
                {
                    "hex_value": "#714B41",
                    "colour_name": "Pitch Pencil"
                },
                {
                    "hex_value": "#762F50",
                    "colour_name": "LBB Pencil"
                },
                {
                    "hex_value": "#8C4A47",
                    "colour_name": "Love Bug Pencil"
                },
                {
                    "hex_value": "#702E2D",
                    "colour_name": "Poison Pencil"
                },
                {
                    "hex_value": "#93283C",
                    "colour_name": "Bichette Pencil"
                },
                {
                    "hex_value": "#653E44",
                    "colour_name": "Dukes Pencil"
                },
                {
                    "hex_value": "#5C3357",
                    "colour_name": "Leather Pencil"
                },
                {
                    "hex_value": "#242225",
                    "colour_name": "Bull Chic Pencil"
                },
                {
                    "hex_value": "#B5716A",
                    "colour_name": "Brink Pencil"
                },
                {
                    "hex_value": "#B0516F",
                    "colour_name": "I Heart This Pencil"
                },
                {
                    "hex_value": "#542328",
                    "colour_name": "Ellarie Pencil"
                },
                {
                    "hex_value": "#DFAC9B",
                    "colour_name": "Toy Pencil"
                },
                {
                    "hex_value": "#AB7164",
                    "colour_name": "BFF Pencil 2"
                }
            ]
    },
    {
        "id": 1047,
        "brand": "colourpop",
        "name": "Blotted Lip",
        "price": "5.5",
        "price_sign": "$",
        "currency": "CAD",
        "image_link": "https://cdn.shopify.com/s/files/1/1338/0845/products/brain-freeze_a_800x1200.jpg?v=1502255076",
        "product_link": "https://colourpop.com/collections/lippie-stix?filter=blotted-lip",
        "website_link": "https://colourpop.com",
        "description": "Blotted Lip Sheer matte lipstick that creates the perfect popsicle pout! Formula is lightweight, matte and buildable for light to medium coverage.",
        "rating": null,
        "category": "lipstick",
        "product_type": "lipstick",
        "tag_list": [
                        "cruelty free",
                        "Vegan"
                    ],
        "created_at": "2018-07-08T22:01:20.178Z",
        "updated_at": "2018-07-09T00:53:23.287Z",
        "product_api_url": "https://makeup-api.herokuapp.com/api/v1/products/1047.json",
        "api_featured_image": "//s3.amazonaws.com/donovanbailey/products/api_featured_images/000/001/047/original/open-uri20180708-4-e7idod?1531087336",
        "product_colors": [
            {
                "hex_value": "#b72227",
                "colour_name": "Bee's Knees"
            },
            {
                "hex_value": "#BB656B",
                "colour_name": "Brain Freeze"
            },
            {
                "hex_value": "#8E4140",
                "colour_name": "Drip"
            },
            {
                "hex_value": "#A12A33",
                "colour_name": "On a Stick"
            },
            {
                "hex_value": "#904550",
                "colour_name": "Ice Cube"
            },
            {
                "hex_value": "#452222",
                "colour_name": "Lolly"
            },
            {
                "hex_value": "#7C3F35",
                "colour_name": "Candyfloss"
            }
        ]
    },...
]
```

# 4. Get /mycart
Description: get all myCart based on UserId from database
## Request:
headers:
```json
    {
            "access_token": "string"
    }
```
## Response (200-OK)
```json
[
    {
            
        "id": 30,
        "UserId": 6,
        "ProductId": 1047,
        "product_api_url": "https://makeup-api.herokuapp.com/api/v1/products/1047.json",
        "status": "unpaid",
        "createdAt": "2023-02-08T16:38:22.664Z",
        "updatedAt": "2023-02-08T16:38:22.664Z"

    },
    {
        "id": 31,
        "UserId": 6,
        "ProductId": 1048,
        "product_api_url": "https://makeup-api.herokuapp.com/api/v1/products/1048.json",
        "status": "unpaid",
        "createdAt": "2023-02-08T16:41:06.105Z",
        "updatedAt": "2023-02-08T16:41:06.105Z"
    },...
]
```
## Response (400 - Bad Request)
```json
{
    "message": "Unauthorized"
}
OR
{
    "message": "Data not found"
}
```

# 5. Patch /checkout
## Request:
headers:
```json
{
    "access_token": "string"
}
```
## Response (200-OK)
```json
{
    "message": "The receipt will be send to your email shorlty!

}
```
## Response (404 - Not Found)
```json
{
    "message": "Data not found"
}
```

# 6. Get /delivery/cities
Description: get cities from data 3rd party Api Raja Ongkir 

## Request:

### headers:
```json
{
    "access_token": "string"
}
```
## Response (200 - OK)
```json
[
    {
        "rajaongkir": {
            "query": [],
            "status": {
                "code": 200,
                "description": "OK"
            },
            "results": [
                {
                    "city_id": "1",
                    "province_id": "21",
                    "province": "Nanggroe Aceh Darussalam (NAD)",
                    "type": "Kabupaten",
                    "city_name": "Aceh Barat",
                    "postal_code": "23681"
                },
                {
                    "city_id": "2",
                    "province_id": "21",
                    "province": "Nanggroe Aceh Darussalam (NAD)",
                    "type": "Kabupaten",
                    "city_name": "Aceh Barat Daya",
                    "postal_code": "23764"
                },
                {
                    "city_id": "3",
                    "province_id": "21",
                    "province": "Nanggroe Aceh Darussalam (NAD)",
                    "type": "Kabupaten",
                    "city_name": "Aceh Besar",
                    "postal_code": "23951"
                }, ...
    },
]
```

#  7. Post /delivery/fee
## Request:
### headers:
```json
{
    "access_token": "string"
}
```
### query:

```json
{
    destination
}
```
## Response (200 - OK)
```json
{
    30000
}
```

 # 8. Post /generate-midtrans-token
## Request:
### headers:
```json
{
    "access_token": "string"
}
```
## Response (200 - OK)
```json
{
    token: 'string'
}
```
## Response (400 - Bad request
```json
{
    error_messages: 
    [ 
        'transaction_details.gross_amount is not a number' 
    ]
}
```
# 9. Delete /mycart/:id
Description: Delete itemProduct by MyCart.id
## Request:
headers:
```json
{
    "access_token": "string"
}
```
### params:
```json
{
    "id": "integer (required)"
}
```
## Response (200-OK)
```json
{
    "message": "Delete success"
}
```
## Response (404)
```json
{
    message: "not found"
}
```

# 10. POST /products/:productId
## Request:
### User:
```json
{
    UserId: "integer"
}
```
### params:
```json
{
    ProductId: "integer"
}
```
### body:
```json
{
    product_api_url: 'string'
}
```
## Response(201-Created)
```json
{
    message: "add to cart"
}
```
# 11. Global Error
## Response (500)
```json
{
        "message": "Internal server error"
}
```

