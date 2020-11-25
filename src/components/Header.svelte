<script>
  import analyticsTracking from '../utils/analytics';
</script>
<style>
  .Header {
    background-color: #fafbfc;
    color: #191a22;
    padding: 1em 0 0 0;
  }
  .Header-container {
    display: grid;
    grid-template-columns: minmax(auto,1024px);
    justify-content: center;
    align-items: center;
  }
  .Header-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .Header h2 {
    color: #191a22;
    font-size: 20px;
    font-weight: 700;
    letter-spacing: 0.8px;
    cursor: pointer;
  }
  .Header ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  .Header li {
    display: inline-block;
    margin: 0 0.5em 0 0;
  }
  .Header a {
    text-decoration: none;
    font-weight: 300;
    font-size: 14px;
  }
  .Header-social img {
    width: 20px;
  }

</style>
<header class="Header">
  <div class="Header-container">
    <div class="Header-content">
      <div class="Header-logo">
        <img src="https://futuromdrss.s3-us-west-1.amazonaws.com/HeaderMesa+de+trabajo+1.png" alt="Logo">
        <h2>Blog de educación en medicina</h2>
      </div>
      <div class="Header-social">
        <ul>
          <li>
            <a href="https://www.linkedin.com/in/jesusdavidemiliano" target="_blank" rel="noreferrer" on:click={analyticsTracking('linkedin')}>
              <img src="linkedin-icon.png" alt="LinkedIn">
            </a>
            <a href="https://twitter.com/jdemiliano" target="_blank" rel="noreferrer" on:click={analyticsTracking('twitter')}>
              <img src="twitter-icon.png" alt="Twitter">
            </a>
            <a href="https://github.com/jesusreynosos" target="_blank" rel="noreferrer" on:click={analyticsTracking('github')}>
              <img src="github-icon.png" alt="GitHub">
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</header>