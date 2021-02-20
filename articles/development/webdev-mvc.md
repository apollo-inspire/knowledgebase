# Webdev MVC Model

## General
Model   
View    
Controller  

Router  
Browser 
Database    


## Example Pseudocode

### browser 
```http
https://awesomewebapp.com/catalog/products/1234
```

### router
```js
catalog/products/:sku =  Products.getProduct(sku)
```

### controller
```js
class Products {
  function getProduct(sku){
    product = this.ProductsModel.getProduct(sku)

    renderView('views/products', product)
  }
}
```

### model
```js
class ProductsModel {
  function getProduct(sku) {
    data = this.db.get('SELECT * FROM products WHERE sku = sku')
    return data
  }
}
```

### view/products
```php
<h1>$product.name;</h1>
<img src=$product.name;>
<p>$product.description;</p>
<p>$product.price;</p>
``` 

