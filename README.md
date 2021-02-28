# shopping cart app



### Installing

download the [fontawesome](fontawesome/css/all.css)


* app.js
```
get the products from [products.json]
initlize the code :
async getProducts(){
    try{

      let result = await fetch('products.json');
      let data = await result.json();
      let products = data.items;



      products = products.map(item => {
        const {title, price} = item.fields;
        const {id} = item.sys;
        const image = item.fields.image.fields.file.url;
        return {title, price, id, image};
      })
      return products;
    }
    catch(error){
      
    }
  }
   
        
```
