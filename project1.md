HTML codes

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="style.css" />
    <link rel="stylesheet" href="../styles.css" />
    <title>JavaScript Background Color Switcher</title>
  </head>
  <body>
    <nav>
      <a href="/" aria-current="page">Home</a>
      <a target="_blank" href="#"
        >Youtube channel</a
      >
    </nav>
    <div class="canvas">
      <!-- <a
        style="
          background-color: #fff;
          padding: 10px 30px;
          border-radius: 8px;
          color: #212121;
          text-decoration: none;
          border: 2px solid #212121;
        "
        href="../index.html"
        >Back to Home Page</a
      > -->
      <h1>Color Scheme Switcher by Rupayan Dey</h1>
      <span class="btn" id="grey"></span>
      <span class="btn" id="white"></span>
      <span class="btn" id="blue"></span>
      <span class="btn" id="yellow"></span>
      <span class="btn" id="lime"></span>
      <span class="btn" id="brown"></span>
      <h2>
        Try clicking on one of the colors above
        <span>to change the background color of this page!</span>
      </h2>
    </div>
    <script src="chaiaurcode.js"></script>
  </body>
</html>


CSS codes

html {
  margin: 0;
}

span {
  display: block;
}
.canvas {
  margin: 100px auto 100px;
  width: 80%;
  text-align: center;
}

.btn {
  width: 100px;
  height: 100px;
  border: solid black 2px;
  display: inline-block;
}

#grey {
  background: grey;
}

#white {
  background: white;
}
#blue {
  background: blue;
}
#yellow {
  background: yellow;
}

#lime {
  background: rgb(179, 236, 152);
}

#brown {
  background: brown;
}

```
JS codes

const buttons = document.querySelectorAll(".btn")

const bodys = document.querySelector("body")

buttons.forEach( function (butt) {

   console.log(butt)

  butt.addEventListener("click", function(e) {
      console.log(e)
        console.log(e.target)
        if (e.target.id === "grey") {
         bodys.style.backgroundColor = e.target.id
        }
        if (e.target.id === "white") {
            bodys.style.backgroundColor = e.target.id
        }
        if (e.target.id === "blue") {
            bodys.style.backgroundColor = e.target.id
        }
        if (e.target.id === "yellow") {
            bodys.style.backgroundColor = e.target.id         
        }
        if (e.target.id === "lime") {
            bodys.style.backgroundColor = e.target.id        
        }
      if (e.target.id === "brown") {
            bodys.style.backgroundColor = e.target.id       
        }
    } )
    
} )

```
