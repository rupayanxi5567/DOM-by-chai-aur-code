HTML codes

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="style.css" />
    <link rel="stylesheet" href="../styles.css" />
    <title>BMI Calculator</title>
  </head>
  <body>
    <nav>
      <a href="/" aria-current="page">Home</a>
      <a target="_blank" href="https://www.youtube.com/@chaiaurcode"
        >Youtube channel</a
      >
    </nav>
    <div class="container">
      <h1>BMI Calculator</h1>
      <form>
        <p><label>Height in CM: </label><input type="text" id="height" /></p>
        <p><label>Weight in KG: </label><input type="text" id="weight" /></p>
        <button>Calculate</button>
        <div id="results"></div>
        <div id="weight-guide">
          <h3>BMI Weight Guide</h3>
          <p>Under Weight = Less than 18.6</p>
          <p>Normal Range = 18.6 and 24.9</p>
          <p>Overweight = Greater than 24.9</p>
          
        </div>
      </form>
    </div>
  </body>
  <script src="chaiaurcode.js"></script>
</html>


CSS codes

body{
    background-color: grey;
    color: white;
}

.BMI{
    color: black;
    font-size: 20px;
    font-weight: bold;
    
}

JS codes

const forms = document.querySelector("form")

//this following comment is wrong

//const heights = parseInt(document.querySelector("#height"))

forms.addEventListener("submit", function (e){
    e.preventDefault()

    const heights = parseInt(document.querySelector("#height").value)

    const weights = parseInt(document.querySelector("#weight").value)

    const result = document.querySelector("#results")

    if( heights === "" ){
        result.innerHTML = "Height can't be empty"
    }


    if(  heights <= 0  ){
        result.innerHTML = "Height can't be negative"
    }


    if(  isNaN (heights) ){
        result.innerHTML = "Height must be a number"
    }


    if(  isNaN (weights) ){
        result.innerHTML = "weights must be a number"
    }


    if(  isNaN (weights) ){
        result.innerHTML = "weights must be a number"
    }


    if(  isNaN (weights) ){
        result.innerHTML = "weights must be a number"
    }

    else{
      const BMI =  (weights/((heights*heights)/10000)).toFixed(2)
      const resBMI = document.querySelector("#BMI")

    //   result.innerHTML = ` <span id = "BMI" > Your BMI is ${BMI} </span>`
if (BMI < 18.6){
    result.innerHTML = ` <span class = "BMI" > Your BMI is ${BMI} which is underweight </span> `
}    

else if (BMI > 18.6 && BMI< 24.9 ){
    result.innerHTML = ` <span class = "BMI" > Your BMI is ${BMI} which is in normal range </span> `
} 

else if ( BMI> 24.9 ){
    result.innerHTML = ` <span class = "BMI" > Your BMI is ${BMI} which is overweight </span> `
} 

}

  

} )
