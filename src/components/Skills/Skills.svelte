<script>
  import Bootstrap from "./icons/bootstrap.svelte";
  import Firebase from "./icons/firebase.svelte";
  import Github from "./icons/github.svelte";
  import Go from "./icons/go.svelte";
  import Heroku from "./icons/heroku.svelte";
  import JavaScript from "./icons/javaScript.svelte";
  // import Next from "../../../svg-icons/next.svelte";
  import Nextjs from "./icons/nextjs.svelte";
  import Node from "./icons/node.svelte";
  import Nodejs from "./icons/nodejs.svelte";
  import React from "./icons/react.svelte";
  import Svelte from "./icons/svelte.svelte";
  import TailwindcssIcon from "./icons/tailwindcss-icon.svelte";
  // import Tailwindcss from "./icons/tailwindcss.svelte";
  import Typescript from "./icons/typescript.svelte";
  import Vercel from "./icons/vercel.svelte";
  import Vite from "./icons/vite.svelte";
  import Postcss from "./icons/postcss.svelte";
  import Pwa from "./icons/pwa.svelte";
  import Netlify from "./icons/netlify.svelte";
  import Scss from "./icons/scss.svelte";
  import Git from "./icons/git.svelte";
</script>

<section class="skills">
  <h2>🏆 skills set</h2>
  <div class="flex">
    <div class="css box">
      <h1>css technologies</h1>
      <!-- <Tailwindcss value="6rem" /> -->
      <Bootstrap value="6rem" />
      <TailwindcssIcon value="6rem" />
      <Scss />
      <Postcss />
    </div>
    <div class="framework box">
      <h1>front framework technologies</h1>
      <Svelte />
      <React />
      <Nextjs />
    </div>
    <div class="langauge box">
      <h1>programming langauge</h1>
      <Go />
      <JavaScript />
      <Typescript />
    </div>
    <div class="backend box">
      <h1>backend and deployment</h1>
      <Node />
      <Nodejs />
      <Heroku />
      <Vercel />
      <Netlify />
      <Firebase value="6rem" />
    </div>
    <div class="other box">
      <Pwa value="6rem" />
      <Git />
      <Github />
      <Vite />
    </div>
  </div>

  <blockquote>
    <p>The best way out is always through <br />-Robert Frost</p>
  </blockquote>
</section>

<style>
  .skills {
    background-color: rgba(179, 176, 176, 0.192);
    background-repeat: no-repeat;
    /* box-shadow: 0 0 3rem #808080dc; */
    border: 3px solid #333;
    border-radius: 2rem;
    padding: 1rem 3rem;
  }
  .box {
    background-color: rgba(218, 215, 213, 0.445);
    box-shadow: 0 0 3rem #808080dc;
    padding: 1rem;
    margin: 0.2rem;
    border-radius: 2rem;
  }
  .box > h1 {
    font-size: 1.2rem;
    margin-bottom: 1rem;
    /* background-color: blue; */
  }

  .flex {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }
</style>
