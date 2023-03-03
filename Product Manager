class Product {
    constructor(id, title, description, price, thumbnail, code, stock){
        this.id = id;
        this.title = title;
        this.description = description;
        this.price = price;
        this.thumbnail = thumbnail;
        this.code = code;
        this.stock = stock;
    }   
    
}  

class ProductManager {
    constructor()
    {
        this.products = new Array();
        this.currentId = 1;
    
    }

    getProducts() {
        return this.products
    }
    addProduct(title, description, price, thumbnail, code, stock)  
    {
        if   ( !title || !description || !price || !thumbnail || !code || !stock ) 
        {
            console.error('You must fill all the box ');
            return;

            }
          const checkingProduct = this.products.find(product => product.code === code);

          if (checkingProduct)
           {

            console.error('This CODE is already in the system.' ) ;
            return;

          }
        const product = new Product(this.currentId, title, description, price, thumbnail, code, stock);
        this.products.push(product)
        this.currentId ++ ;
        
    }
    getProductById(id)
    {
        const product = this.products.find((product)=>product.id == id)
        if (!product)
        //  throw new Error("Not found");]
        console.log("Not found")
        return product
        
    }

}




const productManager = new ProductManager();
productManager.addProduct('Pelota','Es redonda',50 ,'www.google.com','123123',3);
productManager.addProduct('botines','son rojos',100 ,'www.youtube.com','99872',10);
productManager.addProduct('tito','tontito',1 ,'www.facebook.com','327262',99);
console.log(productManager.getProductById(10))

// console.log(productManager.getProducts())
