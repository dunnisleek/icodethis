<template>
       <div class="wrapper">
       <header>
              <nav>
                     <ul>
                      <li>Home</li>
                      <li><b>Project</b></li>
                      <li>Inbox</li>
                      <li>Teams</li>   
                     </ul>
              </nav>
              <div>
                            <button class="btn">Upgrade</button>
                            <button class="jb">JB</button>
                     </div>
       
       </header>
       
        <section>
        <div class="sidebar">
              <div>
               <h3>Projects</h3>
               <ul>
              <li>boardme development</li>
              <li>Feature lists</li>
              <li>Marketing</li>
              <li>UIDD development</li>
              <li>Topics</li>
              <li>Bugs and fixes</li>
              </ul>
              <button class="viewBtn">View All ></button>
              </div>
              <div class="teamSection">
                     <h3>Teams</h3>
                     <div>
                     <h4>Need to form a team?</h4>
                     <p>Try out 30 days trail and see what you can achieve together.</p>
                     <button>Try it free</button>
                      </div>
              </div>
        </div>

        <div class="container">
          <h3>Projects</h3>
          <ul>
              <li>
                     <div>bd
                     </div>
                     <span>boardme development</span>
                     </li>
              <li><div>FL</div><span>Feature lists</span></li>
              <li><div>M</div><span>Marketing</span></li>
              <li><div>Ud</div><span>UIDD development</span></li>
              <li><div>T</div><span>Topics</span></li>
              <li><div>Ba</div><span>Bugs and fixes</span></li>
              <li class="plus" @click="displayMe"><div>+</div>
              <span >Add a project</span></li>
          </ul>
        </div>

        <div class="modal" v-show="display">
              Thank You for clicking me, Have a great time
              <button @click="close">Close</button>
        </div>
       </section>
       </div>
</template>

<script>
       export default {
              data(){
                     return{
                            display:false
                     }
              },
              methods:{
                     displayMe(){
                           this.display = !this.display
                     },
                     close(){
                            this.display=false
                     }
              }
       }
</script>

<style scoped>
.wrapper{
    background:  #FFF6E7; 
    padding:20px;
    /* height:80vh; */
  
}
/* HEADER */
header{
       display:flex;
       justify-content: space-between;
       padding-bottom:20px;
}
nav ul{
       display:flex;
       gap:20px;
}
nav ul{
       list-style-type: none;
       font-size:20px;
       line-height:24px;
       padding:0px;
}
ul li{
       cursor:pointer;
       transition:.2s ease-in;
}
ul li:hover{
       transform: scale(1.075);
}
header div{
       display:flex;
       gap:20px;
}
.btn{
       font-size:20px;
       line-height:24px;
       border:2px solid #282828;
       border-radius:50%;
       border-radius: 50px;
       width: 133px;
       max-width: 133px;
       padding: 10px;
       cursor:pointer;
       transition:.2s ease-in;
}
.btn:hover{
       transform: scale(1.075);
}
.jb{
       background:#FF589C;
       width:50px;
       font-size:20px;
       line-height:24px;
       border:none;
       border-radius:50%;
       cursor:pointer;
       transition:.2s ease-in;
}
.jb:hover{
       transform: scale(1.075);
}
.wrapper section{
       display: flex;
       width:100%;
}
/* start of sidebar */
.sidebar{
       width:250px;
       max-width:250px;
       height:75vh;
       border-radius:30px;
       padding:20px;
       background:#232323;
       color:#fff;
}
.sidebar h3{
       color:#b0adad;
       font-size:18px;
       line-height:23px;
       text-transform: uppercase;
       padding-bottom:20px;
}
.sidebar li{
       font-size:16px;
       line-height: 20px;
       padding-bottom:20px;
}
.sidebar ul{
       padding:0px 0px 0px 20px;
}
.sidebar li:nth-of-type(1)::marker{   
 color:#FFB658;
}
.sidebar li:nth-of-type(2)::marker{   
 color:#FF8158;
}
.sidebar li:nth-of-type(3)::marker{   
 color:#58AEFF;
}
.sidebar li:nth-of-type(4)::marker{   
 color:#B058FF;
}
.sidebar li:nth-of-type(5)::marker{
       color:lime;
 
}
.sidebar li:nth-of-type(6)::marker{
       color:  #FF589C;
     
}
/* view button style */
.viewBtn{
       background:transparent;
       color:#FF589C;
       font-size:18px;
       transition:.3s linear;
       border:none;
       cursor: pointer;
}
.viewBtn:hover{
       text-decoration:underline;
       transform:scale(1.075);
     
}

/* TEAMS SECTION SIDEBAR */
.teamSection{
       padding-top:50px;
}
.teamSection div{
       background:#4A4745;
       padding:20px 15px;
       border-radius:10px;
}
.teamSection h4{
       font-size:20px;
}
.teamSection button{
       background:#FFF6E7;
       width:200px;
       height:5vh;
       font-size:16px;
       line-height:22px;
       border:none;
       border-radius:5px;
       transition: 0.3s ease-in-out;
       cursor:pointer;
       margin-top:15px;
}
.teamSection button:hover{
       transform: scale(1.075);
       background:rgb(196, 233, 246) ;
}
/* START OF CONTAINERS PROJECTS */

.container ul {
      display: flex;
      gap:1rem;
      flex-wrap: wrap;
list-style-type: none;
position: relative;
      
       
}


.container li{
       flex: 0 0  14%; /* Each item takes 20% of the container width */
       box-sizing: border-box;
       padding: 10px;
       /* width:240px;
       border-radius:15px;
       height:20vh; */
       display:flex;
       flex-direction: column;
       align-items: center;
       position:relative;
}
.container div{
       width:135px;
       border-radius:15px;
       height:20vh;
       display:flex;
       flex-direction: column;
       align-items: center;
       justify-content: center;
       font-size:30px;
       color:#ffffff;
       box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
}
.container h3{
       font-size:30px;
       padding-left: 3rem;
       padding-bottom:3rem;
}
.container li:nth-child(1) div{   
 background:#FFB658;
}
.container li:nth-child(2) div{   
       background:#FF8158;
}
.container li:nth-child(3) div{   
       background:#58AEFF;
}
.container li:nth-child(4) div{   
       background:#B058FF;
}
.container li:nth-child(5) div{
       background:lime;
 
}
.container li:nth-child(6) div{
       background:#FF589C;
 
}

.sidebar li:nth-of-type(8)::marker{
       background:none;
      
}
.container li span:first-child {
       color:#fff;
       font-size:70px;
}
.container li:last-child div{
       border:2px solid #232323;
       border-radius:10px;
       color:#232323;
   
}

/* .container li span:nth-child(2){
       position: absolute;
       top:10rem;
       
} */
.plus li{
       color:#232323;
      
}
.container span{
       font-size:16px;
       line-height: 22px;
       text-align: center;
       padding-top:10px;
}

/* popup details */
.modal{
    background: rgb(255, 255, 255);
    width: 600px;
    height: 50vh;
    border-radius: 30px;
    position: absolute;
    top:90%;
    left: 30%;
    right: 50%;
    font-size:20px;
    padding: 40px;
}

</style>