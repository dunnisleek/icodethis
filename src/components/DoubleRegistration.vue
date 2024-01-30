<template>
       <section class="reg">
           <div class="centered orangebg">
              <h2>Registration Open!</h2>
              <p>2018 - 2019</p>
              <p class="para">Register and upload your design today to know how good your design is: get a complimentory preliminary score.</p>
              <button>Submit Now</button>
           </div>

           <div class="left orangebg">
              <div class="wrap">
              <div>
              <h2>Registration Open!</h2>
              <p>2018 - 2019</p>
              <p class="para-left">Register and upload your design today to know how good your design is: get a complimentory preliminary score.</p>
              </div>
              <div>
                     <button>Submit Now</button>
              </div>
            
              </div>
           </div>
       </section>
</template>

<script>
       export default {
              
       }
</script>

<style scoped>
  section{
       padding-top:100px;
  }
  .reg{
      display: flex;
      flex-direction: column;
      justify-content: center;
      gap:50px;
      align-content: center;
      align-items: center;
     color:#ffffff;
   
  }
  .centered{
       text-align: center
  }
  .orangebg{
       background: #E2375E;
       width:700px;
       max-width: 700px;
       margin:20px;
       padding:30px 20px;
       border-radius:10px;
  }
  .para{
       width:400px;
       max-width: 400px;
       margin: 0 auto;
       padding:13px 0px;
  }
  
  .wrap {
       display: flex;
       padding:30px 30px 30px 80px
  }
  .centered button{
       width:180px;
       padding:10px;
       text-transform: uppercase;
       border:none;
       border-radius: 5px;
       transition: .2s ease-in-out;
  }
  .centered button:hover{
       background:transparent;
       border:2px solid #fff;
       color:#fff;
      
  }
  .left button{
       background:transparent;
       border:1px solid #ffffffcf;
       width:140px;
       padding:10px;
       color:#fff;
       text-transform: uppercase;
  }
</style>