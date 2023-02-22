<nav>
    <div class="navbar">
    <h1>Your Daily Fruit</h1>
     <ul> 
        <li> <a href="/" class="active">Home</a> </li> 
        <li> <a href="/product">Product</a></li> 
        <li> <a href="/chart">Chart</a> </li> 
        <li> <a href="/order">Order</a> </li> 
        <li> <a href="#keranjang">          
        </li>  
    </ul>
    </div>
</nav> 
<div class="container">
<slot />
</div>

<style>
nav{
  padding: 0.5em;
} 
    ul {
        display: flex;
        margin: 0;
        margin-left: auto;
        list-style-type: none;
        font-size:1em;
        }
    .navbar{
          display: flex;
    }
    li {
        margin-right: 20px; 
    }

    li a {
        display: block;
        color: gray;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;  
        }

li a:hover:not(.active) {
    color: black;
    }

.active {
  color: #703c00;
}
h1 {
    
    font-size: 1.3em;
    font-weight: normal;
}

</style>

