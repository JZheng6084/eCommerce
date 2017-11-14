# eCommerce

<html>
        <head>
            <title>The Painting Shop</title>
            <style>
    
                div.container {
                    width: 100%;
                     border: 1px solid gray;
                }
    
                header, footer {
                    padding: 1em;
                    color: white;
                    background-color: rgb(168, 31, 31);
                    clear: left;
                    text-align: center;
                }
                
                body {
                    background-image: url("background3.jpg");
                }
               
    
            </style>
            <script>
                var price1 = 30;
                var price2 = 20;
                var price3 = 25;
                
    
                
                var shipping;
    
                var Oprice1 = 15;
                var Oprice2 = 10;
                var Oprice3 = 10;
              
                
                
                
             
                function calc(){
                    
                    document.getElementById("span1").innerHtml = "Price: $" + price1;
                    document.getElementById("span2").innerHtml = "Price: $" + price2;
                    document.getElementById("span3").innerHtml = "Price: $" + price3;
                   
    
                    
                }
                function ProcessOrder(){
                   
                
                    var qty1 = parseFloat(document.getElementById("qty1").value); 
                    var qty2 = parseFloat(document.getElementById("qty2").value); 
                    var qty3 = parseFloat(document.getElementById("qty3").value);
                 
    
    
    
                    var op = document.getElementById("output");
    
                    var flowersubtotal = (price1 * qty1) + (price2 * qty2) + (price3 * qty3);
                    
                    var customersubtotal = flowersubtotal ;
                    var customertax = customersubtotal * 0.0875;
    
                    if(customersubtotal < 100){
                        shipping = 25;
                    }else if(customersubtotal >= 100 && customersubtotal <= 200){
                        shipping = 10;
                    }else{
                        shipping = 0;
                    }
    
                    var customertotal = customersubtotal + customertax + shipping;
    
                    var cflowersubtotal = (Oprice1 * qty1) + (Oprice2 * qty2) + (Oprice3 * qty3);
                    
                    var companysubtotal = cflowersubtotal;
                    var flowerprofit = flowersubtotal - cflowersubtotal;
                    
                    var companyprofit = customersubtotal - companysubtotal;
                     
                    var floweritem = qty1 + qty2 + qty3;
                    
    
                    var totalitemsold = floweritem;
    
                    var build="";
                    build += "<hr>";
                    build += "<h2> Customer Order Details </h2>";
                    build += "<hr>";
                    build += "Subtotal: $" + customersubtotal;
                    build += "<br>";
                    build += "Tax: $" + customertax;
                    build += "<br>";
                    build += "Shipping: $" + shipping;
                    build += "<br>";
                    build += "Total $" + customertotal;
                    build +="<hr>";
    
                    
                    build +="<h2> Company Details </h2>";
                    build += "<hr>";
                    build += "<h3> Customer Subtotal </h3>";
                    build += " - Flower Painting Customer Subtotal: $" + flowersubtotal;
                    build += "<br>";
                    build += "Customer Total Subtotal: $" + customersubtotal;
                   
                    build += "<hr>";
                    build += "<h3> Company Subtotal </h3>";
                    build += " - Flower Painting Company Subtotal: $" + cflowersubtotal;
                    build += "<br>";
                    build += "Company Total Subtotal: $" + companysubtotal;
                    build += "<hr>";
                    build += "<h3> Company Profit </h3>";
                    build += " - Flower Painting Profit: $" + flowerprofit;
                     build += "<br>";
                 
                    build += "Total Profit: $" + companyprofit;
                    build += "<hr>";
                    build += "<h3> Items Sold </h3>";
                    build += " - Flower Paintings: " + floweritem ;
                    build += "<br>";
             
                    build += "Total Items Sold: " + totalitemsold;
                    build += "<hr>";
    
                    op.innerHTML= build;
                    
            
                }
                
            </script> 
        </head>
        <body onload="calc()">
             
                <header>
                    <ul>
                      <h1> The Flower Painting Shop</h1><hr>
                      <h3>The World's Best Flower Paintings
    
                          
                      </h3>
                          
                    </ul>
                </header>
                      
                
                    <ul>
                        
                        <table>
                            <tr>
                                <td>
                                       
                                    
                                    <hr>
                                    <div>
                                        <img src="flower1.jpg" style="border: 5px solid rgb(192, 70, 70);" width="210" height="210"/><br>
                                        <h3>Rosey Red</h3>
                                        <h3>Price: $30</h3>
                                        <h4>Painted by Lisa Serland</h4>
                                        <span id="span1"></span>
                                        <input type = "text" id="qty1" value="0" placeholder = "Quantity">
                                        <hr>
                                    </div>

                                </td>
                                <td>
                                    <hr>
                                    <div>
                                        <img src="flower2.jpg" style= "border: 5px solid rgb(173, 91, 53);" width="210" height="210"/><br>
                                        <h3>Crystal Orange</h3>
                                        <h3>Price: $20</h3>
                                        <h4>Painted by Jessy Bloom</h4>
                                        <span id="span2"></span>
                                        <input type = "text" id="qty2" value="0" placeholder = "Quantity">
                                        <hr>
                                    </div>
                                </td>
                                <td>
                                    <hr>
                                    <div>
                                        <img src="flower3.jpg" style="border: 5px solid rgb(180, 174, 114);" width="210" height="210"/><br>
                                        <h3>Milky White</h3>
                                        <h3>Price: $25</h3>
                                        <h4>Painted by Ashley Gilberg</h4>
                                        <span id="span3"></span>
                                        <input type = "text" id="qty3" value="0" placeholder = "Quantity">
                                    </div>
                                    <hr>
                                </td>
                               
                            </tr>
                        </table>
                          
                          
                    </ul>
    
            
                      
                
    
    
            <button onclick="ProcessOrder()"> Process Order </button>
            <br>
            <div id = "output"></div>
            <hr>
            <h3>Attention Customers</h3>
            <p>
                This website is under the owership of the JSU Company. 
            </p>
            <p>
                All ecommerce on this website are under the protection of the BDP (Bureau of Digital Protections)
            </p>
    
    
            <footer>
                <h2> Thanks for Shopping </h2>
            </footer>
            
    
        </body>
        
    </html>
