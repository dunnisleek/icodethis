<template>
       <div class="loginWrap">
        <section>
              <div class="imgSection">
                     <img src="../assets/car.webp" width="400"/>
              </div>
              <div class="loginForm">
                     <h2>Login</h2>
                     <form>
                            <label>Email</label>
                            <input type="text" placeholder="Enter Your Email Address"/>

                            <label>Password</label>
                            <input type="password" placeholder="Enter Your Password"/>
                            <button class="loginBtn">Log in</button>
                            <span>or</span>
                            <div>
                            <button class="socialBtn"><svg xmlns="http://www.w3.org/2000/svg" class="w-6" viewBox="0 0 15 15">
                        <path fill="none" stroke="currentColor" d="M4.5 6v5m6 0V8.5a2 2 0 1 0-4 0V11V6M4 4.5h1M1.5.5h12a1 1 0 0 1 1 1v12a1 1 0 0 1-1 1h-12a1 1 0 0 1-1-1v-12a1 1 0 0 1 1-1Z"></path>
                    </svg>
                    Continue with LinkedIn
                    </button>
                   </div>
                     </form>
                     <footer>
                            <ul>
                                   <li><a href="#">Can't log In?</a></li>
                                   <li><a href="#">Sign up for an account</a></li>
                            </ul>
                     </footer>
              </div>
        </section>
       </div>
</template>

<script>
       export default {
              
       }
</script>

<style scoped>
 
.loginWrap{
    background:#581a1a;
    height: 100vh;
    margin: 0 auto;
    display:flex;
    align-items: center;
    justify-content: center;
    align-content: center;
}
section{
       background:#ffffff;
       display:flex;
       width:800px;
       max-width:800px;
       padding:20px;
       border-radius: 10px;
       gap:40px;
       position: relative;
}
div .loginForm  {
       display:flex;
       flex-direction:column;
       padding-top:40px;
}
.imgSection img{
       border-radius: 10px;
       height:70vh;
       object-fit: cover;
}
form{
       display:flex;
       flex-direction: column;
       gap:5px;
}
.socialBtn svg{
       width:30px;
}
.socialBtn{
       background: #0369A1;
       font-size:20px;
       width:280px;
       color:#ffffff;
       padding:13px;
       border-radius: 5px;
       border:none;
       display: flex;
    justify-content: center;
    align-items: center;
    gap:5px;


}
.socialBtn:hover{
       
}
.loginForm h2{
       font-size:25px;
       line-height: 30px;
       padding-bottom: 40px;
}
input{
       padding:13px;
       width:250px;
      margin-bottom: 10px;
      background: rgb(245, 217, 222);
      border:1px solid grey;
      border-radius: 5px;
}
label{
       font-size:18px;
       padding-bottom: 10px;
}
.loginBtn{
       font-size:20px;
       background: #B45309;
       color:#ffffff;
       padding:13px;
       border-radius: 5px;
       border:none;
}
footer{
       position: absolute;
       /* top:0; */
       
      
       bottom:0;
      
}
footer ul{
       list-style-type: none;
       display: flex;
       justify-content: flex-start;
       gap:50px;
       padding-bottom: 20px;
       text-align: left;
}
footer ul li{
       padding:0;
       margin-left:-30px;
}

@media only screen and (max-width: 1200px){
    /*Tablets [601px -> 1200px]*/
    section{
       width: 661px;
    max-width: 661px;
    }
    input{
       width:189px;
    }
    .loginBtn, .socialBtn{
       width:193px;
    }
    .socialBtn{
       font-size:16px;
       font-size: 16px;
    padding: 3px 6px;
    display: flex;
    justify-content: center;
    align-items: center;
    }

}
@media only screen and (max-width: 600px){
	/*Big smartphones [426px -> 600px]*/
          section{
              display:flex;
              flex-direction: column;
              width:300px;
          } 
          .imgSection img{
              width:300px;
              height:50vh;
       }
       footer{
              position:relative;
              top:20px;
       }
       .socialBtn{
              padding:6px;
       }
}
@media only screen and (max-width: 425px){
	/*Small smartphones [325px -> 425px]*/
       section{
              display:flex;
              flex-direction: column;
              width:300px;

       }
       .imgSection img{
              width:300px;
              height:50vh;
       }
       .div .loginForm{
              padding-top: 0px;
       }
       footer{
              position:relative;
              top:20px;
       }
       .socialBtn{
              padding:6px;
       }
}
</style>