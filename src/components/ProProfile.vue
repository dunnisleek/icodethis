<template>
       <div class="profile-wrapper">
         <div class="card">
              <div>
              <h2 class="img-circle"></h2>
              <h3>Ricky Pack</h3>
              <p>NEW YORK</p>
              <p>User interface designer and front end developement</p>
              <div class="btnwrap">
                <button class="green">Message</button>
                <button class="greenBorder">Following</button>
              </div>
              </div>
              <div class="career">
                     <h2 class="skill">Skills</h2>
                  <div  v-for="item in skills" :key="item.id">
                     {{item }}
                  </div>
               </div>
        </div>
       </div>
</template>

<script>
       export default {
              data(){
                     return{
                            skills:['ui/ux','frontend development','HTML','Java','Jquery']
                     }
              }
       }
</script>

<style scoped>
.profile-wrapper{
       background: #292240;
       padding-top:8rem;
       padding-bottom: 15rem;
}
/*CARD SECTION */
.card{
       background:#231F39;
       width:300px;
       padding:5rem;
       margin: 0 auto;
       box-shadow: rgba(0, 0, 0, 0.16) 0px 10px 36px 0px, rgba(0, 0, 0, 0.06) 0px 0px 0px 1px;
}
.img-circle{
  background: pink;
  width:100px;
  height:16vh;
  border-radius:100%;
  margin-bottom:10px;
}
.card > div{
       display: flex;
       flex-direction: column;
       justify-content: center;
       align-items: center;
}
.card p{
       color:#fff;
       text-align: center;
       font-size:15px;
}
.card h3{
       font-size:20px;
       line-height:28px;
       color:#fff;
       font-weight: 700;
}
.green{
       background:#01BFCB;
       background: #01BFCB;
       border-radius: 2px;
       border: none;
      padding: 10px 40px;
    color: #fff;
}
.greenBorder{
       background:transparent;
       border:1px solid #01BFCB;
       border-radius: 2px;
       padding: 10px 40px;
    color: #01BFCB;
}
.btnwrap{
       display: flex;
       gap:10px;
       margin-top:20px;
}
.career{
    background: #1D1A36;
    width: 460px;
    padding:3rem 0rem;
    margin: 0 auto;
    display: flex;
    position: absolute;
    left: 0;
    right: 0;
    margin-top:30px;

}
.skill{
       color:#fff;
       flex: 1; /* This makes the left column take up the available space */
    text-align: left; /* Align text to the left */
}
.career > div{
       display:flex;
}
</style>