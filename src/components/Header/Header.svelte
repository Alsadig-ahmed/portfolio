<header>
  <h1>🚀 Welcome to my portfolio website.</h1>
  <div>
    <span>
      <h2>I am Alsadig Ahmed</h2>
      <blockquote>
        <p>
          I love making software that other people can use and benefit from.
        </p>
      </blockquote>
    </span>
    <img src="/my-image.png" alt="Alsadig Ahmed" />
  </div>
</header>

<style lang="scss">
  header {
    padding: 0.3em 0.7em 0.7em 0.7em;
    margin: 2em auto;
    border-radius: 2em;
    box-shadow: inset 0em 0.2em 0.9em 0.5em rgba(255, 255, 255, 0.514);
    h1 {
      text-align: center;
    }
    @media (min-width: 600px) {
      div {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0.2rem 2rem;
      }
    }
    div img {
      transform: scale(1.08);
      margin-top: -4rem;
      width: 16em;
    }
    @media (min-width: 600px) {
      div img {
        width: 22em;
      }
    }
  }
</style>
