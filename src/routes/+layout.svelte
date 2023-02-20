<nav>
    <div class="container">
    <h1>Be Skin</h1>
     <ul> 
        <li> <a href="/">Home</a> </li> 
        <li> <a href="/product">Product</a></li> 
        <li> <a href="/chart">Chart</a> </li> 
        <li> <a href="/order">Order</a> </li> 
        <li> <a class="active" href="#keranjang">          
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
  background-color: white;
} 
    ul {
        display: flex;
        margin: 0;
        margin-left: auto;
        list-style-type: none;
        font-size:1em;
        }
    .container{
          display: flex;
    }
    li {
        margin-right: 20px; 
    }

    li a {
        display: block;
        color: #111;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;  
        }

li a:hover:not(.active) {
    color: gray;
    }

.active {
  color: gray;
}
h1 {
    
    font-size: 1.3em;
    font-weight: normal;
}

</style>

