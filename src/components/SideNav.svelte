<nav>
  <ul>
    <li><a href={"#"}>home</a></li>
    <li><a href={"#"}>about</a></li>
    <li class="dropdown">
      <a href={"#"}>tools <span> &rsaquo; </span></a>
      <ul class="sub">
        <li><a href={"#"}>home</a></li>
        <li class="dropdown_tow">
          <a href={"#"}>good <span> &rsaquo; </span> </a>
          <ul class="sub">
            <li><a href={"#"}>home</a></li>
            <li><a href={"#"}>good</a></li>
            <li><a href={"#"}>home</a></li>
            <li><a href={"#"}>about</a></li>
          </ul>
        </li>
        <li><a href={"#"}>home</a></li>
        <li><a href={"#"}>about</a></li>
      </ul>
    </li>
    <li><a href={"#"}>contact</a></li>
    <li><a href="#projects">projects</a></li>
    <li class="dropdown">
      <a href={"#"}>manifesto <span> &rsaquo; </span> </a>
      <ul class="sub">
        <li><a href={"#"}>home</a></li>
        <li><a href={"#"}>good</a></li>
        <li><a href={"#"}>home</a></li>
        <li><a href={"#"}>about</a></li>
      </ul>
    </li>
  </ul>
</nav>

<style lang="scss">
  nav {
    width: 15rem;
    background-color: rgba(228, 224, 224);
    margin: 1rem 0 0 0.3rem;
    padding: 1rem 0 1rem 1rem;
    position: absolute;
    top: 0;
    bottom: 0;
    border-radius: 1rem;
    box-shadow: 1rem 0.7rem 1rem 0 rgba(46, 45, 45, 0.815);
    ul {
      position: relative;
      list-style-type: none;

      ul {
        // background-color: rgba(65, 62, 62, 0.7);
        background-color: rgba(228, 224, 224);
        box-shadow: 1rem 0.7rem 1rem 0 rgba(46, 45, 45, 0.815);
        border-radius: 0 2rem;
        display: none;
        width: 14rem;
        position: absolute;
        top: 0rem;
        left: 14rem;
      }
      .dropdown {
        position: relative;
        display: block;
        &:hover > ul {
          display: initial;
        }
      }
      .dropdown_tow ul {
        position: absolute;
        top: 0rem;
        display: initial;
        &:hover ul {
          display: initial;
        }
      }
      li {
        a {
          text-decoration: none;
          font-size: 1.5em;
          font-family: Arial, Helvetica, sans-serif;
          display: flex;
          align-items: center;
          justify-content: space-between;
          color: black;
          border-radius: 0 2rem;
          padding: 0.7rem 1rem;
          transition: 0.2s ease;

          &:hover {
            background-color: rgba(65, 62, 62, 0.7);
          }
        }
      }
    }
    span {
      position: absolute;
      font-size: 3rem;
      right: 1rem;
    }
  }
</style>
