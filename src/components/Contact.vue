<template>
<section id="contact-page">
    <div class="contact-wrapper">
        <header class="contact-heading">
            <h1>Contact</h1>
        </header>
        <div class="form-container">
            <form @submit.prevent="handleSubmit">
            <label>Name</label>
            <input type="text" name="name" placeholder="name" required v-model="name">
            <label>Email</label>
            <input type="email" name="email" placeholder="email" required v-model="email">
            <label>Message</label>
            <textarea name="message" id="message-area" placeholder="message" required v-model="message"></textarea>
            <button type="submit">Send Message</button>
        </form>
        </div>
    </div>
</section>
</template>

<script>
export default {
name: "Contact",
data() {
    return {
        name: "",
        email: "",
        message: "",
    }
},
methods: {
    handleSubmit () {
        console.log("Form Submitted")
        console.log(this.name)
        console.log(this.email)
        console.log(this.message)
    }
},
}
</script>

<style>
body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
#contact-page {
    display: flex;
    background: #eee;
    flex-direction: column;
    justify-content: flex-start;
    row-gap: 3rem;
    align-items: center;
    height: 100vh;
    margin: 0;
    padding: 0;
}
.contact-heading {
    font-size: 3rem;
    padding: 0;
}
.contact-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
}
.form-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 30%;
    padding: 20px;
}
form {
     display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 2rem;
    width: 100%;
    padding: 20px;
}
input {
    width: 80%;
    padding: 20px;
    height: 10px;
}
textarea {
    width: 80%;
    height: 200px;
    padding: 20px;
}
</style>