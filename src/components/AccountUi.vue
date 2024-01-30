<template>
       <body>
  <div class="accountWrapper">
<!-- ICONS SECTIONS -->
    <div class="icons">
      <label @click="display(0)">
        <img src="../assets/person_icon.svg" />
      </label>
      <label  @click="display(1)">
        <img src="../assets/emoji_people.svg" />
      </label>
      <label  @click="display(2)">
        <img src="../assets/notifications.svg" />
      </label>
      <label  @click="display(3)">
        <img src="../assets/settings.svg" />
      </label>
    </div>

    <!-- START OF MAIN CONTENT -->
    <section id="panel1" v-show="currentStep == 0">
       <div>
              <img src="../assets/120.jpeg"/>
              <h3>Janet World</h3>
              <p>Ui Consultant</p>
       </div>
    </section>

    <section id="panel2" v-show="currentStep == 1">
       <div>
              <img src="../assets/balloons.png" width="50"/>
        <h3>200th streak submission</h3>
       </div>
    </section>

    <section id="panel3" v-show="currentStep == 2" class="notify">
       <h3><img src="../assets/lock.svg"/>App permissions</h3>
       <p class="greybg"><strong>31 apps</strong> have access to your data
                </p>
      <p class="textsmall">Manage which apps have access to your data. You can revoke permission whenever you want</p>
      <button class="purpleBtn">Change app permissions</button>
    </section>

    <!-- START OF THEME SWITCHER -->
    <section class="switcher" v-show="currentStep == 3">
       <div class="switch" @click="toggleTheme">
              <p>Dark Mood</p>
              <span><i class="far fa-moon"></i>{{darkMode ? 'light mode' : 'dark mode'}}</span>
       </div>
      
    </section>
  </div>
  </body>
</template>

<script>
export default {
       data(){
              return{
                     hideMe:false,
                     currentStep:0,
                     toggle:true,
                     darkMode:false
              }
                    
              
       },
       methods:{
             display(val){
              this.currentStep = val
             } ,
             toggleButton(){
              this.toggle = !this.toggle
             },
             toggleTheme(){
              this.darkMode = !this.darkMode
              localStorage.setItem('darkMode', this.darkMode.toString())
              this.applyTheme()
             },
             applyTheme(){
              const switcherSection = document.querySelector('.accountWrapper');
              if(this.darkMode){
              switcherSection.classList.add('dark-theme');
             }else{
              switcherSection.classList.remove('dark-theme');
             }
       },
       created() {
    // Retrieve user's theme preference from local storage
    const storedTheme = localStorage.getItem('darkMode');
     // Convert the string value to a boolean
    this.darkMode = storedTheme === 'true';
    //apply theme
    this.applyTheme();
  }
}
}
</script>

<style scoped>
.accountWrapper {
  background: #2356ce;
  height: 50vh;
  padding:50px;
}
.icons{
       background:#4E75D1;
       display:flex;
       flex-direction:column;
       justify-content: center;
       align-items: center;
       width:70px;
       margin:0 auto;
       border-radius:80px;
       padding:40px 10px;
       
}

.icons label img{
       background:#fff;
       padding:10px;
       border-radius:20px;
       margin:4px;
       animation: .2s ease-in-out;
}
.icons label img:hover{
       background: blue;
       color:#fff;
       transition-property: all;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 150ms;

}
#panel1{
       background:#224FBF;
       border-radius:10px;
       width:400px;
       color:#fff;
       display:flex;
       flex-direction: column;
       align-items: center;
       padding-bottom:40px;
       position: absolute;
       top: 127px;
      left: 200px;

}
#panel1 img{
       border-radius:80px;
       position: relative;
       top:-40px;
}
#panel1 p{
       text-transform: uppercase;
}

#panel2, #panel3{
       background: #062981;
       border-radius:10px;
       width:400px;
       color:#fff;
       display:flex;
       flex-direction: column;
       align-items: center;
       padding-bottom:10px;
       position: absolute;
       top: 127px;
      left: 200px;
}
#panel3{
       height:34vh;
}
.purpleBtn{
       padding: 14px 25px;
       border:none;
       background:rgb(2, 2, 112);
       color:#fff;
       text-transform: uppercase;
}
/* START OF switcher */
.notify{
       padding:40px 20px;
       height:20vh;
}
.switcher{
       /* background: red; */
       height:40vh;
       width:300px;
       text-align: center;
       border-radius: 20px;
       position: absolute;
       top: 167px;
      left: 230px;
  
       /* position: relative; */
}
.switch i{
       background: #fff;
       width:70px;
       border-radius:30px;
       padding:10px;
       text-align: center;
}
.switch{
       background:#1E3A8A;
       padding:30px;
       border-radius: 20px;
}
.switch p{
       font-size:25px;
       line-height: 30px;
       padding-bottom:10px;
       color:white;
}
.dark-theme{
       background-color:rgb(0, 0, 0);
}
.dark-theme .switch{
       background: #ffff;
      
}
.dark-theme .switch p{
       color:#232323;
}
.dark-theme .switch i{
       background:#1E3A8A;
}
.notify h3{
       font-size:30px;
       padding-bottom:10px;
}
.greybg{
       background:rgb(181, 180, 180);
       padding:10px;
       color:#232323;
}
.textsmall{
       width:300px;
       padding:20px;
}
</style>
