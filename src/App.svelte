<script>
  import Contact from "./components/Contact/Contact.svelte";
  import Footer from "./components/Footer/Footer.svelte";
  import Header from "./components/Header/Header.svelte";
  import Manifesto from "./components/Manifesto/Manifesto.svelte";
  import Projects from "./components/projects/Projects.svelte";
  import Skills from "./components/Skills/Skills.svelte";
  import WorkHistory from "./components/WorkHistory.svelte";
</script>

<Header />
<main>
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
