<script>
  import Contact from "./components/Contact/index.svelte";
  import Footer from "./components/Footer/index.svelte";
import Good from "./components/Good/Good.svelte";
  import Header from "./components/Header/index.svelte";
  import Manifesto from "./components/Manifesto/index.svelte";
  import Projects from "./components/projects/index.svelte";
  import Skills from "./components/Skills/index.svelte";
  import WorkHistory from "./components/WorkHistory.svelte";
</script>

<Header />
<main>
  <Good /> 
  <Skills />
  <Projects />
  <Manifesto />
  <WorkHistory />
  <Contact />
</main>
<Footer />

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen,
      Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }
</style>
