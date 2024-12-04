# End Point 1: Get all available shoes


*Request:*
**GET /api/shoes**

Headers:

    Accept: application/json
    Accept: application/xml

**Response:**
*Status Code: 200 OK*

```json
[
    {
        "id": "0011",
        "name": "Adidas Samba",
        "brand": "Adidas",
        "category": "Casual",
        "price": "PHP 6,500",
        "availability": "In Stock"
    },
    {
        "id": "0012",
        "name": "Nike Zoom Air",
        "brand": "Nike",
        "category": "Running Shoes",
        "price": "PHP 7,500",
        "availability": "In Stock"
    },
    {
        "id": "0013",
        "name": "Jordan 1 Low",
        "brand": "Jordan",
        "category": "Casual",
        "price": "PHP 9,200",
        "availability": "Out of Stock"
    },
    {
        "id": "0014",
        "name": "New Balance 530",
        "brand": "New Balance",
        "category": "Basketball",
        "price": "PHP 8,000",
        "availability": "In Stock"
    },
    {
        "id": "0015",
        "name": "Asics Gel-Nimbus",
        "brand": "Asics",
        "category": "Running Shoes",
        "price": "PHP 9,000",
        "availability": "In Stock"
    }
]
```

# End Point 2: Get shoe by ID

***Request:
GET /api/shoes/{id}
Headers:***

    Accept: application/json
    Accept: application/xml

**Response:**
Status Code: 200 OK

**JSON**
```JSON
{
    "id": "0011",
    "name": "Adidas Samba",
    "brand": "Adidas",
    "category": "Casual",
    "price": "PHP 6,500",
    "availability": "In Stock"
}
```

```XML
<product>
    <id>0011</id>
    <name>Adidas Samba</name>
    <brand>Adidas</brand>
    <category>Casual</category>
    <price>PHP 6,500</price>
    <availability>In Stock</availability>
</product>
```



# End Point 3: Add a new shoe

*Request:*
**POST /api/shoes/brand/Adidas** 

Headers:

    Accept: application/json
    Accept: application/xml

*Response:*
**Status Code: 200 OK**

**JSON**
~~~JSON
{
    "name": "Puma RS-X",
    "brand": "Puma",
    "category": "Lifestyle",
    "price": "PHP 7,000",
    "availability": "In Stock"
}
~~~
**XML**
~~~XML
<product>
    <name>Puma RS-X</name>
    <brand>Puma</brand>
    <category>Lifestyle</category>
    <price>PHP 7,000</price>
    <availability>In Stock</availability>
</product>
~~~


# End Point 4: Update shoe details
*Response:*
**Status Code: 201 Created**

Request:
**PUT /api/shoes/{id}**

Headers:

    Accept: application/json
    Accept: application/xml

**JSON**
~~~JSON
{
    "price": "PHP 5,800",
    "availability": "Out of Stock"
}
~~~
**XML**
~~~XML
<product>
    <price>PHP 5,800</price>
    <availability>Out of Stock</availability>
</product>
~~~


# End Point 5: Delete a shoe by ID

*Request:*
**DELETE /api/shoes/{id}**

Headers:

    Accept: application/json
    Accept: application/xml

*Response:*
**Status Code: 200 OK**

**JSON**
~~~JSON
{
    "message": "Product deleted successfully"
}
~~~
**XML**
~~~XML
<message>Product deleted successfully</message>
~~~

# End Point 6: Get all in-stock shoes

*Request:*
**GET /api/shoes/instock**

Headers:

    Accept: application/json
    Accept: application/xml

*Response:*
**Status Code: 200 OK**

**JSON**
~~~JSON
[
    {
        "id": "0011",
        "name": "Adidas Samba",
        "brand": "Adidas",
        "category": "Casual",
        "price": "PHP 6,500",
        "availability": "In Stock"
    },
    {
        "id": "0015",
        "name": "Asics Gel-Nimbus",
        "brand": "Asics",
        "category": "Running Shoes",
        "price": "PHP 9,000",
        "availability": "In Stock"
    }
]
~~~
**XML**
~~~XML
<products>
    <product>
        <id>0011</id>
        <name>Adidas Samba</name>
        <brand>Adidas</brand>
        <category>Casual</category>
        <price>PHP 6,500</price>
        <availability>In Stock</availability>
    </product>
    <product>
        <id>0012</id>
        <name>Nike Zoom Air</name>
        <brand>Nike</brand>
        <category>Running Shoes</category>
        <price>PHP 7,500</price>
        <availability>In Stock</availability>
    </product>
    <product>
        <id>0014</id>
        <name>New Balance 530</name>
        <brand>New Balance</brand>
        <category>Basketball</category>
        <price>PHP 8,000</price>
        <availability>In Stock</availability>
    </product>
</products>
~~~


# End Point 7: Get all shoes within a price range

*Request:*
**GET /api/shoes/price**

Headers:

    Accept: application/json
    Accept: application/xml

*Response:*
**Status Code: 200 OK**

**JSON**
~~~JSON

[
    {
        "id": "0012",
        "name": "Nike Zoom Air",
        "brand": "Nike",
        "category": "Running Shoes",
        "price": "PHP 7,500",
        "availability": "In Stock"
    },
    {
        "id": "0014",
        "name": "New Balance 530",
        "brand": "New Balance",
        "category": "Basketball",
        "price": "PHP 8,000",
        "availability": "In Stock"
    }
]
~~~
**XML**
~~~XML
<products>
    <product>
        <id>0012</id>
        <name>Nike Zoom Air</name>
        <brand>Nike</brand>
        <category>Running Shoes</category>
        <price>PHP 7,500</price>
        <availability>In Stock</availability>
    </product>
    <product>
        <id>0014</id>
        <name>New Balance 530</name>
        <brand>New Balance</brand>
        <category>Basketball</category>
        <price>PHP 8,000</price>
        <availability>In Stock</availability>
    </product>
</products>
~~~


# End Point 8: Search shoes by brand

*Request:*
**GET /api/shoes/brand/Nike**
Headers:

    Accept: application/json
    Accept: application/xml

*Response:*
**Status Code: 200 OK**

**JSON**
~~~JSON
[
    {
        "id": "0012",
        "name": "Nike Zoom Air",
        "brand": "Nike",
        "category": "Running Shoes",
        "price": "PHP 7,500",
        "availability": "In Stock"
    }
]
~~~
**XML**
~~~XML
<products>
    <product>
        <id>0012</id>
        <name>Nike Zoom Air</name>
        <brand>Nike</brand>
        <category>Running Shoes</category>
        <price>PHP 7,500</price>
        <availability>In Stock</availability>
    </product>
</products>
~~~

# End Point 9: Delete shoes by brand

*Request:*
**DELETE /api/shoes/brand**
Headers:

    Accept: application/json
    Accept: application/xml

*Response:*
**Status Code: 200 OK**

**JSON**
~~~JSON

{
    "message": "All shoes of brand 'Nike' have been deleted successfully",
    "remainingShoes": [
        {
            "id": "0011",
            "name": "Adidas Samba",
            "brand": "Adidas",
            "category": "Casual",
            "price": "PHP 6,500",
            "availability": "In Stock"
        },
        {
            "id": "0014",
            "name": "New Balance 530",
            "brand": "New Balance",
            "category": "Basketball",
            "price": "PHP 8,000",
            "availability": "In Stock"
        }
    ]
}
~~~
**XML**
~~~XML

<response>
    <message>All shoes of brand 'Nike' have been deleted successfully</message>
    <remainingShoes>
        <product>
            <id>0011</id>
            <name>Adidas Samba</name>
            <brand>Adidas</brand>
            <category>Casual</category>
            <price>PHP 6,500</price>
            <availability>In Stock</availability>
        </product>
        <product>
            <id>0014</id>
            <name>New Balance 530</name>
            <brand>New Balance</brand>
            <category>Basketball</category>
            <price>PHP 8,000</price>
            <availability>In Stock</availability>
        </product>
    </remainingShoes>
</response>
~~~

# End Point 10: Get shoes by brand

*Request:*
**GET /api/shoes/brand/Adidas** 

Headers:

    Accept: application/json
    Accept: application/xml

*Response:*
**Status Code: 200 OK**


**JSON**
~~~JSON
{
    "message": "Shoes of brand 'Adidas' retrieved successfully",
    "shoes": [
        {
            "id": "0011",
            "name": "Adidas Samba",
            "brand": "Adidas",
            "category": "Casual",
            "price": "PHP 6,500",
            "availability": "In Stock"
        }
    ]
}
~~~

***XML***
~~~XML
<response>
    <message>Shoes of brand 'Adidas' retrieved successfully</message>
    <shoes>
        <product>
            <id>0011</id>
            <name>Adidas Samba</name>
            <brand>Adidas</brand>
            <category>Casual</category>
            <price>PHP 6,500</price>
            <availability>In Stock</availability>
        </product>
    </shoes>
</response>
~~~
# End Point 11: Update shoes by brand

*Request:*
**PUT /api/shoes/brand/Nike**

Headers:

    Accept: application/json
    Accept: application/xml

***JSON:***
~~~JSON
{
    "message": "All shoes of brand 'Nike' have been updated successfully",
    "updatedShoes": [
        {
            "id": "0012",
            "name": "Nike Zoom Air",
            "brand": "Nike",
            "category": "Running Shoes",
            "price": "PHP 8,000",
            "availability": "Out of Stock"
        }
    ]
}
~~~

**XML:**
~~~XML
<response>
    <message>All shoes of brand 'Nike' have been updated successfully</message>
    <updatedShoes>
        <product>
            <id>0012</id>
            <name>Nike Zoom Air</name>
            <brand>Nike</brand>
            <category>Running Shoes</category>
            <price>PHP 8,000</price>
            <availability>Out of Stock</availability>
        </product>
    </updatedShoes>
</response>
~~~
