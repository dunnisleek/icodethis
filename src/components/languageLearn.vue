<template>
  <div class="content">
    <section>
      <div class="quiz wht-bg slide-in-up">
        <progress value="90" min="0" max="100"></progress>
        <h3>Which of these is “You eat pasta”?</h3>
        <fieldset>
          <label>
            <input type="radio" name="El caballo es pequeño"  />
            <span>El caballo es pequeño</span>
          </label>
          <label>
            <input type="radio" name="Tú comes pasta" />
            <span>Tú comes pasta</span>
          </label>
          <label>
            <input type="radio" name="Él come pan" />
            <span>Él come pan</span>
          </label>
        </fieldset>

        <footer>
          <button>skip this question</button>
          <div>submit</div>
        </footer>
      </div>
 
      <div class="tier wht-bg">
        <h3>Select a tier</h3>
        <ul>
          <li>
            <p><span>$5/month</span> A significant contribution</p>
            <button>Select</button>
          </li>
          <li>
            <p><span>$30/month</span> A huge contribution</p>
            <button>Select</button>
          </li>
        </ul>
      </div>

      <div class="progress wht-bg">
        <svg
          class="meter-circle"
          width="96"
          height="96"
          viewBox="0 0 260 260"
          fill="none"
          stroke-width="12"
        >
          <path
            stroke="#0002"
            class="background"
            d="M130 10a120 120 0 1 1 0 240 120 120 0 0 1 0-240"
          ></path>
          <path
            stroke="#000"
            class="value"
            stroke-linecap="round"
            stroke-dasharray="754.09 754.09"
            stroke-dashoffset="565.57"
            d="M130 10a120 120 0 1 1 0 240 120 120 0 0 1 0-240"
          ></path>
        </svg>
        <h3>Nature</h3>
        <button>Continue</button>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
progress{
       width:300px;
       margin-bottom:30px;
}
.content {
  background: #12194d;
  height: 100vh;
 padding-top:140px;
 padding-left: 20rem;

}
section {
  display: flex;
  flex-direction: column;
 align-items: center;
 justify-content: center;
 align-content: center;
  gap: 40px;

}
.wht-bg {
  background: #ffffff;
  border-radius: 10px;
}
.quiz {
 position: relative;
  padding: 60px;
  text-align: center;
  width:400px;
  max-width: 400px;
  height:50vh;
}
h3 {
  font-size: 22px;
  line-height: 30px;
}
 /* Apply margin to create space between radio inputs */
 input[type="radio"] {
            margin-right: 20px; /* Adjust the value as needed */
        }
.quiz fieldset {
  display: flex;
  flex-direction: column;
  border: none;
  align-items: flex-start;
  justify-content: center;
  padding-bottom: 40px;
  gap:10px;
  font-size:20px;
  padding:25px 70px 40px 80px;
}
footer{
       position: absolute;
       bottom:0;
       left:0;
       right:0;
       font-size:22px;
       line-height: 25px;
       /* background:#FF9A2C; */
}
footer button {
       width:520px;
       block-size: 3rem;
       border:none;
       border-top:1px solid rgba(128, 128, 128, 0.83);
}
footer div{
       display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
       width:520px;
       block-size: 5rem;
       background:#FF9A2C;
       border-radius:0px 0px 10px 10px;
}

fieldset{
       padding-top:30px;

}
.slide-in-up {
  opacity: 0; /* Initially set opacity to 0 */
  transform: translateY(100%); /* Move the box down by its height */
  animation: slideUp 1s ease-out forwards; /* Use the slideUp animation for 1 second */
}

@keyframes slideUp {
  to {
    opacity: 1; /* At the end of the animation, set opacity to 1 */
    transform: translateY(0); /* Move the box up to its original position */
  }
}
/* TIER STYLE */
.tier{
       width:300px;
       max-width:300px;
       padding:30px;
       transform: translate(-33rem, -27rem);
     

       
}
.tier p{
       width:200px;
}
.tier span{
       font-weight: 600;
       font-size:19px;
       display: block;
}
.tier button{
       background:none;
       border:1px solid #FF9A2C;
       border-radius: 15px;
       width:80px;
       /* transition-property:transform ;
       transition-duration:0.5s;
       transition-delay: 0s;
       transition-timing-function:ease; */

}
.tier button:hover{
       background:#FF9A2C;
       /* transform:translateY(-3px) */
}
.tier ul{
       display: flex;
       flex-direction: column;
       gap:40px;
       justify-content: space-between;
       width:300px;
       margin:0;
       padding: 0;
     
}
.tier li{
       display: flex;
       gap:20px;
       padding: 10px;
    
}
.tier li:hover{
       background:#EAEDFA;
       border-radius:9px;
       padding: 10px;
       cursor: pointer;
       
}
/* .slide-in-left {
  opacity: 0;
  animation: slideInLeft 1s ease-out forwards;
}

@keyframes slideInLeft {
       from {
    transform: translateX(-100%) translateY(-27rem);
  }
  to {
    transform: translateX(0) translateY(-27rem);
  }
} */



/* PROGRESS STYLE */
.progress{
       display: flex;
       flex-direction: column;
       align-items: center;
       justify-content: center;
       width:250px;
       max-width: 250px;
       height:30vh;
       transform:translate(-20rem, -30rem);
       box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
}
.progress button{
       border:1px solid #FF9A2C;
       border-radius:10px;
       margin-top:20px;
       background: none;
       width:130px;
       height:5vh;
}
.progress button:hover{
       background: #FF9A2C;
       color:#ffffff;
}
div{
       animation: var(500ms) var(400ms) 0s backwards scale-up;
    transition: transform var(500ms) var(200ms);
}


</style>
