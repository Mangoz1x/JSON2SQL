
# MangoSQL
Turns traditional MySQL string queries into JSON queries similar to mongoose & mongodb




## Features

- JSON Based SQL Queries
- Uses Local/Non Local Env 
- Synchronous
- Cross platform


## Usage/Examples

```javascript
const MangoSQL = require("mangosql");

<!-- Inserting To Database -->
### EX: INSERT INTO TABLE_NAME SET `productName=test product`, `productId=1` ### 
const InsertProduct = await MangoSQL.insert("TABLE_NAME", { productId: 1, productName: "test product" });

<!-- Deleting From Database -->
### EX: DELETE FROM TABLE_NAME WHERE `productName=test product` AND `productId=1` ###;
const DeleteProduct = await MangoSQL.delete("TABLE_NAME", { productId: 1, productName: "test product" });

<!-- Retreiving From Database -->
### EX: SELECT FROM TABLE_NAME WHERE `productId=1` ###
const GetProduct = await MangoSQL.select("TABLE_NAME", { productId: 1 });

<!-- Updating Item In Database -->
### EX: UPDATE TABLE_NAME SET `productName=another product` WHERE `productId=1` ###
const UpdateProduct = await MangoSQL.update("TABLE_NAME", { productName: "another product" }, { productId: 1 });

<!-- Selecting From Database Using Conditionals -->
### EX: SELECT FROM TABLE_NAME WHERE `productId=1` OR `productName=test product` ###
const GetProduct = await MangoSQL.selectany("TABLE_NAME", { productName: "test product" }, { productId: 1 });

<!-- Delete From Database Using Conditionals -->
### EX: DELETE FROM TABLE_NAME WHERE `productName=test product` AND `productId=1` OR `productName=another test product` ###;
const DeleteProduct = await MangoSQL.deleteany("TABLE_NAME", { productName: "testProduct", productId: 1 }, { productName: "another test product" });
```


## Authors

- [@mangoz1x](https://mangoz1x.com)

