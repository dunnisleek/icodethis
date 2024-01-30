<template>
  <div class="wrapper wrap-rows">
       <div class="first row">
         <img src="../assets/organic-flat-business-people-meditating-illustration_23-2148926706.avif"/>
         <h2>Connect multiple account</h2>
         <p>There's a new coding challenge awaiting for you every day, and you have 24 hours to complete it.</p>
          <div class="btn-row">
            <button>Skip</button>
           <button>arrow</button>
          </div>
         
       </div>

       <div class="second row">
        <img src="../assets/flat-illustration-secretary-s-day-celebration_23-2150229828.avif"/>
         <h2>Smart messaging system</h2>
         <p>There's a new coding challenge awaiting for you every day, and you have 24 hours to complete it.</p>
          
         <div class="btn-row">
         <button>Skip</button>
        <button class="arrow"><img src="../assets/arrow-right-solid.svg"/></button> 
        </div>
       </div>

       <div class="third row">
        <img src="../assets/organic-flat-business-people-meditating-illustration_23-2148926706.avif"/>
         <h2>Instant data analysis</h2>
         <p>There's a new coding challenge awaiting for you every day, and you have 24 hours to complete it.</p>
          
         <button>Get Started</button>
         
       </div>

  </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
.wrapper{

  width:500px;
  max-width: 500px;

  padding:10rem;
 
}
.wrap-rows{
  display:flex;
  justify-content: space-between;
  flex-direction: row;
  gap:50px;
  /* width:1300px; */
}
.row img{
  width:300px;

}
.row{
  background: #ffffff;
  padding:30px;
  border-radius: 20px;
  width:300px;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}
.row h2{
  font-size:23px;
  line-height:27px;
   word-wrap: break-word;
   width:260px;
  text-align: center;
  padding:13px 0px;
  margin: 0 auto;
}

.row p{
  font-size:16px;
   width:240px;
   margin: 0 auto;
  text-align: center;
}
.third button{
  background:#FF9765;
  border:none;
  border-bottom-right-radius: 10px;
  color:#fff;
  padding:10px;
  /* text-align: center; */
  margin: 0 auto;
}

.arrow img{
  width:20px;
 
}
.arrow {
  background: #FF9765;
  border-bottom-right-radius: 10px;
  border:none;
}
button{
  background: transparent;
  border:none;
}
.btn-row{
  display: flex;
  gap:70px;
}
</style>