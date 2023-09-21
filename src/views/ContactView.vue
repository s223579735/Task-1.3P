<template>
  <div class="contact">
    <div style="margin: auto; width: 50%; margin-bottom: 5px;">
      <h1 style="font-size: 24px; margin-bottom: 5px;">Contact Information</h1>
    </div>
    <div style="display: flex; align-items: flex; margin-top: 25px; ">
      <div style="margin-left: 5%">
        <iframe width="500px" height="400px"
          src="https://www.google.com/maps/embed/v1/place?q=deakin+university+melbourne+burwood+campus&key=AIzaSyBFw0Qbyq9zTFTd-tUY6dZWTgaQzuU17R8" />
      </div>
      <div class="form" style="margin-left: 50px;">
        <div style="text-align: left;">
          <input type="text" v-model="name" placeholder="Name" />
        </div>
        <div style="text-align: left; margin-top: 10px;">
          <input type="text" v-model="email" placeholder="Email" />
        </div>
        <div style="text-align: left; margin-top: 10px;">
          <input type="text" v-model="subject" placeholder="Subject" />
        </div>
        <div style="text-align: left; margin-top: 10px;">
          <textarea style="height: 120px; width: 300px" v-model="message" placeholder="Message" />
        </div>
        <div v-if="errors.length" style="width: 100%; height: 20px;">
          <ul>
            <li v-for="(error, index) in errors" v-bind:key="index">{{ error }}</li>
          </ul>
        </div>
        <div style="margin-top: 75px; text-align: left">
          <button @click="submitForm" type="submit">Submit</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.contact {
  width: 100vw;
  overflow-x: hidden;
}

input[type=text],
textarea {
  padding: 12px;
  border: 1px solid #ccc;
  border-radius: 4px;
  resize: vertical;
  width: 250px;
}

li {
  text-align: left;
}

button {
  width: 100%;
  height: 30px;
  cursor: pointer;
  border: none;
  border-radius: 8px;
  color: white;
  background-color: green;
}

@media only screen and (max-device-width: 400px) {
  iframe {
    width: 40vw;
    height: 50vh;
  }

  input[type=text],
  textarea {
    max-width: 100px;
  }
}
</style>

<script>
export default ({
  data() {
    return {
      name: '',
      email: '',
      subject: '',
      message: '',
      errors: [],
    }
  },

  methods: {
    async submitForm() {
      this.errors = [];
      if (!this.name) this.errors.push("Name is required")
      if (!this.subject) this.errors.push("Subject is required")
      if (!this.message) this.errors.push("Message is required")
      if (!this.email) {
        this.errors.push("Email is required")
      } else {
        // eslint-disable-next-line
        const regex = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/ // regex taken from w3schools
        if (!regex.test(this.email)) {
          this.errors.push("Please enter a valid email")
        }
      }
      if (this.errors.length == 0) {
        console.log("This doesn't actually do anything i wish it did")
      }
    }
  }

})
</script>
