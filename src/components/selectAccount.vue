<template>
  <div class="wrapper">
    <section>
      <h3>Select Your Profile</h3>
      <p>
        Logged in users can view full bussiness profile and can save contact
        details
      </p>
    </section>
    <section class="profiles">
      <div>
        <img
          src="../assets/organic-flat-business-people-meditating-illustration_23-2148926706.avif"
        />
        <h4>Andrew Mart</h4>
        <button>...</button>
      </div>
      <div>
        <img
          src="../assets/organic-flat-business-people-meditating-illustration_23-2148926706.avif"
        />
        <h4>Andrew Mart</h4>
        <button>...</button>
      </div>
      <div class="last"></div>
    </section>
    <section class="edit">
      <div>
        <img src="../assets/edit.png" width="20" /> <button>Edit</button>
      </div>
      <div>
        <img src="../assets/delete.png" width="20" /> <button>Delete</button>
      </div>
    </section>

    <section class="progress">
      <div class="skill">
        <div class="outer">
          <div class="inner">
            <div id="number">
              {{ counter }}% <br />
              number content
            </div>
          </div>
        </div>
        <svg width="250" height="250" viewBox="0 0 200 200">
          <circle
            :style="{ animation: isAnimating ? 'anim 1s linear forwards' : '' }"
            r="70"
            cx="80"
            cy="80"
            fill="#000000"
            :stroke-dasharray="dashArray"
            :stroke-dashoffset="dashOffset"
            stroke="#e0e0e0"
            stroke-width="12px"
          ></circle>
        </svg>
        <!-- <svg width="250" height="250" viewBox="0 0 200 200">
  <circle r="70" cx="80" cy="80" fill="transparent" stroke="#e0e0e0" stroke-width="12px"></circle>
  <circle r="70" cx="80" cy="80" fill="transparent" stroke="#e0e0e0" stroke-width="12px"></circle>
</svg> -->
      </div>
      <h2>Curriculum</h2>
      <form>
        <div>
          <label>
            <input
              type="checkbox"
              name="introduction"
              value="introduction"
              v-model="checkboxes[0].checked"
              @change="updateCounter"
            />
            <span class="custom-checkbox"></span>
            <h4>Chapter 1 <span>Introduction</span></h4>
          </label>
        </div>
        <div>
          <label>
            <input
              type="checkbox"
              name="Introduction-Architecture"
              value="Introduction-Architecture"
              v-model="checkboxes[1].checked"
              @change="updateCounter"
            />
            <span class="custom-checkbox"></span>
            <h4>Chapter 2 <span>Introduction Architecture</span></h4>
          </label>
        </div>
        <div>
          <label>
            <input
              type="checkbox"
              name="Data and Security"
              value="Data and Security"
              v-model="checkboxes[2].checked"
              @change="updateCounter"
            />
            <span class="custom-checkbox"></span>
            <h4>Chapter 3 <span>Data and Security</span></h4>
          </label>
        </div>
      </form>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isAnimating: false,
      counter: 0,
      checkboxes: [
        { label: "introduction", checked: false },
        { label: "Introduction Architecture", checked: false },
        { label: "Data and Security", checked: false },
      ],
    };
  },
  computed: {
    dashArray() {
      const radius = 70;
      const circumference = 2 * Math.PI * radius;
      return `${circumference} ${circumference}`;
    },
    // Calculate the dash offset based on the percentage counter
    dashOffset() {
      const radius = 70;
      const circumference = 2 * Math.PI * radius;
      const percentage = this.counter / 100;
      return circumference - percentage * circumference;
    },
  },
  methods: {
    updateCounter() {
      this.counter =
        this.checkboxes.filter((checkbox) => checkbox.checked).length * 25;
      this.isAnimating = true;
    },
  },
};
</script>

<style scoped>
.wrapper {
  text-align: center;
  padding: 100px 40px;
}
.wrapper h3 {
  font-size: 35px;
  line-height: 40px;
  padding-bottom: 20px;
}
.wrapper p {
  font-size: 16px;
  line-height: 21px;
  padding-bottom: 50px;
}
.profiles img {
  width: 80px;
  border-radius: 50%;
  padding-top: 30px;
}
.profiles {
  display: flex;
  /* background: grey; */
  /* justify-content: center;;
        */
  gap: 40px;
}
.profiles div {
  width: 500px;
  height: 30vh;
  margin: 0 auto;
  background: #ffffff;
  border-radius: 10%;
}
.profiles h4 {
  font-size: 23px;
}
.profiles .last {
  background: transparent;
}
.edit {
  background: #ffffff;
  max-width: 200px;
  width: 200px;
  padding: 30px 20px;
  border-radius: 5px;
}
button {
  background: transparent;
  border: none;
}
.progress {
  /* display: flex;
     justify-content: center; */
  background: #ffffff;
  max-width: 400px;
  width: 400px;
  margin: 0 auto;
  padding: 20px 10px;
  border-radius: 15px;
}
.progress h2 {
  padding-top: 50px;
  text-align: left;
  margin-left: 40px;
}
.skill {
  width: 160px;
  height: 160px;
  position: relative;
  margin-left: auto;
  margin-right: auto;
}
.outer {
  width: 160px;
  height: 160px;
  padding: 20px;
  /* border:1px solid orangered; */
  box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
  border-radius: 50%;
  transform: rotate(90deg);
}
.inner {
  width: 160px;
  height: 160px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px 0px,
    rgba(0, 0, 0, 0.1) 0px 0px 1px 0px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  transform: rotate(-90deg);
}
circle {
  fill: none;
  stroke: #272359;
  stroke-width: 20px;
  stroke-dasharray: 440;
  stroke-dashoffset: 440;
  transition: stroke-dasharray 0.5s ease-in-out,
    stroke-dashoffset 0.5s ease-in-out;
  /* animation: anim 1s linear forwards; */
  animation: anim 1s linear forwards;

  /* transform: rotate(30deg); */
}
@keyframes anim {
  100% {
    stroke-dashoffset: 337.5;
  }
}

svg {
  position: absolute;
  top: 0;
  left: 0;
}
form div {
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px,
    rgba(60, 64, 67, 0.15) 0px 1px 3px 1px;
  margin: 15px auto;
  width: 311px;
  height: 75px;
  border-radius: 5px;
  text-align: left;
  padding: 20px 0px 20px 20px;
}

h4 span {
  display: block;
  font-weight: 400;
}

label h4 {
  margin-left: 30px;
  margin-top: -25px;
  cursor: pointer;
}
/* Hide the default checkbox */
input[type="checkbox"] {
  display: none;
}
/* Create a custom checkbox style */
.custom-checkbox {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  border: 2px solid #000; /* Set the border color and width */
  display: inline-block;
  position: relative;
  cursor: pointer;
}
/* Style the inner circle when the checkbox is checked */
input[type="checkbox"]:checked + .custom-checkbox::before {
  content: "\2713"; /* Unicode checkmark character */
  font-size: 16px; /* Adjust the size of the checkmark */
  color: #000; /* Set the color of the checkmark */
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>
