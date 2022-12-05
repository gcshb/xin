
 <head>
  <meta charset="utf-8" name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
  <title>满屏心动</title>
  <style>
       *{
         
         margin:0;
         padding:0;
         }
    body{
      width:100vw;
      height:100vh;
      overflow:hidden;
      background-color:black;
    /* text-shadow:1px 1px 8px #ffb3d9;*/
    
    }
  
  span{
    display:block;
    position:absolute;
    
    font-size:100px;
    animation: xin 1s alternate infinite;
  
   }
 @keyframes xin{
   0%{
     transform:scale(1)
   }
   100%{
     
     transform:scale(1.2)
   }
  }
    
    
    h1{
      
      color:white;
      text-align:center;
      margin-top:50%;
      text-shadow:2px 2px 20px rgba(0,255,255);
      }
  </style>
  </head>
  
  <body>
     <h1>流心雨</h1>
  </body>
  
  <script>
     
     //创建50个心
     for(let i = 0; i< 50; i++){
        let xin = document.createElement("span")
        xin.innerHTML = "❤️"
        
        xin.style.left = Math.round(Math.random() *110) + "%"
        xin.style.fontSize = Math.round(Math.random() *50)+"px"
        document.body.insertAdjacentElement("afterbegin",xin)
        
        //定时
        let top = Math.round(Math.random() *100) - 100
        let i = top
        setInterval(function(){
            i+=0.5
            xin.style.top = i+"%"
            if(i >= 100){
               i = top
             }
        },20)
        
     }
     
  
  
  </script>
  

