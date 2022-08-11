<script>
  import axios from "axios";
  import { fly } from "svelte/transition";

  axios
    .get("https://alsadig-ahmed.netlify.app/.netlify/functions/index")
    .then((res) => console.log({ res }));
  let name, message, email;
  let msg = {
    status: false,
    text: "",
    btn: "",
  };
  // onMount(()=>{
  //   msg.status = false
  // })
  $: msg;
  function handleSubmit(data) {
    let formData = new FormData(data.currentTarget);
    console.log(formData.get("name"));
    console.log(formData.get("message"));
    console.log(formData.get("email"));
    // console.log(new URLSearchParams(formData.toString()));
    console.log(new URLSearchParams(formData).toString());
    fetch("/", {
      method: "POST",
      headers: { "Content-Type": "application/x-www-form-urlencoded" },
      body: new URLSearchParams(formData).toString(),
    })
      .then((res) => {
        console.log(res);
        if (res.ok) {
          msg = {
            status: true,
            text: "Form successfully submitted <h1> thank you for your time :) </h1>",
            btn: "show the form ",
          };
          console.log("Form successfully submitted");
        } else {
          msg = {
            status: true,
            text: "Form submition failed",
            btn: "try again",
          };
          console.log("Form submition failed");
          throw res;
        }
      })
      .catch((error) => console.log(error));

    let newMessage = { name, message, email };
    (name = ""), (message = ""), (email = "");
  }
</script>

<div class="form">
  <h1>get in touch</h1>
  {#key msg.status}
    <div
      out:fly={{ duration: 500, x: -200 }}
      in:fly={{ duration: 500, x: 200, delay: 550 }}
    >
      {#if msg.status}
        <h3 class={msg.text === "Form submition failed" ? "red" : ""}>
          {@html msg.text}
        </h3>
        <button on:click={() => (msg.status = false)}> {msg.btn}</button>
      {:else}
        <form
          name="contact"
          on:submit|preventDefault={handleSubmit}
          method="POST"
          data-netlify="true"
        >
          <p>
            <label for="name"
              >Your Name: <input
                type="text"
                placeholder="enter your name"
                id="name"
                name="name"
                bind:value={name}
              /></label
            >
          </p>
          <p>
            <label for="email"
              >Your Email: <input
                type="email"
                placeholder="whats your email "
                id="email"
                name="email"
                bind:value={email}
              /></label
            >
          </p>
          <p>
            <label for="message"
              >Message: <textarea
                placeholder="what's on your mind ?"
                id="message"
                name="message"
                bind:value={message}
              /></label
            >
          </p>
          <p>
            <button type="submit">Send</button>
          </p>
        </form>
      {/if}
    </div>
  {/key}
</div>

<style>
  p {
    padding: 0;
    margin: 0.2rem 0;
  }
  .form {
    box-shadow: 0 0 2rem 0 rgba(39, 38, 38, 0.76);
    border-radius: 1.3rem;
    padding: 1rem 2rem;
    text-align: center;
  }
  textarea,
  input {
    width: 80%;
    padding: 0.5rem 1rem;
    border-radius: 0.4rem;
  }
  button {
    width: 70%;
    padding: 0.5rem 1rem;
    border-radius: 0.4rem;
  }
  .red {
    background-color: red;
    padding: 2rem 5rem;
    border-radius: 0.4rem;
    margin: 1rem auto;
    max-width: max-content;
  }
</style>
