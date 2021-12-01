<template>
  <div container>
    <div main>
      <div header>
        <p title v-text="name" />
        <p v-text="description" />
      </div>
      <div linkscontainer>
        <div links v-for="(link, index) in links" v-bind:key="index">
          <a :href="link.url" target="_blank" v-text="'+ '+link.label" />
        </div>
      </div>
    </div>
    <img landingimg src="./assets/kid.png" />
  </div>
</template>
<script>

  export default {
    name: 'App',
    data: () => ({
      url: "https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxjb2xsZWN0aW9uLXBhZ2V8MXw3NjA4Mjc3NHx8ZW58MHx8fHw%3D&w=1000&q=80",
      name: 'BOBBY',
      links: [
        {
          label: 'Youtube',
          url: 'http://google.com',
        },
        {
          label: 'Spotify',
          url: 'http://google.com'
        },
        {
          label: 'Discord',
          url: 'http://google.com',
        },
        {
          label: 'Tiktok',
          url: 'http://google.com',
        },
      ],
      description: "Loren ipsum dolor set a met, consectetur adipising elit, sed to eiusmod tempor incididunt ut labore et dolore magnaaliqua.",
  })
  }
</script>

<style>
  body {
    background: #ffff55;
    color: #000;
    font-family: 'Courier New';
    font-size: 12px;
    margin: 0;
  }
  [container] {
    min-height: 100vh;
  }
  [main] {
    padding: 2vh 0;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    max-height: 50vh;
    height: 48vh;
  }
  [header] {
    display: flex;
    flex-direction: column;
    padding: 0 15px;
  }
  a {
    font-size: 26px;
    color: #000;
    font-weight: bold;
    text-decoration: none;
  }
  [linkscontainer] {
    height: 35vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  [links] {
    border-bottom: 1px dotted black;
    padding: 0 15px;
  }
  [title] {
    font-size: 80px;
    font-weight: bold;
    margin: 0;
    margin-left: auto;
    margin-right: auto;
  }
  [landingimg] {
    width: 100%;
    height: 48vh;
    background-color: #4900c2;
  }
</style>
