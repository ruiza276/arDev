<template>
<div >
    <Header />
    <div class="container">
      <h1 class="title">About Me...</h1>
      <p>Hello Hi my name is Alex Ruiz. I'm a Software Engineer based in the Chicago-land area (Ask me about Malört or for a coffee shop recommendation!).</p>
      <h2 class="title"> The Past ☕</h2>
      <p>Before becoming a Software Engineer, I was a electronics technician with a decent talent in IPhone screen repairs and before that I was a barista, slinging out Instagram worthy lattes. 
        Even got third place in a latte art competition that I entered by accident.</p>
      <p>I graduated from DePaul University with a B.S, majoring in Computer Science with a concentration in Software Development and a minor in Data Analysis and Data Mining. 
        I was very disappointed to learn that the mouthful that is my major and minor would not be printed on the physical copy of my degree.</p>
      <h2 class="title"> The Present and Beyond 📊</h2>
      <p>Nowadays I work in primarily .NET and all related technologies. building features, apps,  debugging, etc. 
Going forward, I would love to one day leverage my Data Mining knowledge professionally. I absolutely love working with data and all the cool insights that are waiting to be discovered. </p>
<h1 class="sub-title">Some of the Tech I've worked/working with 💻</h1>
<ul>
  <li>.NET Core (C#)</li>
  <li>Vue.js (this site was built using Vue.js and Nuxt.js)</li>
  <li>HTML + CSS</li>
  <li>Git/Github + Bitbucket</li>
  <li>Python</li>
  <li>Java</li>
  <li>R</li>
</ul>
<h1 class="sub-title">Things I do/have interest in that are not Tech 🚴</h1>
<ul>
  <li>Making bad memes with GIMP</li>
  <li>Reading but mostly wishing I had more time to read</li>
  <li>Making <a class="links" href="https://open.spotify.com/playlist/6z7giYkmjrXW1B09gMRUTi?si=mTvDlOFOQkerhKMzjt3gCQ" target="_blank"> Spotify Playlists</a></li>
  <li>Biking</li>
  <li>Providing commnetary during movie nights a la Mystery Science Theater 3000</li>
  <li>Playing the Ukulele sometimes and re-learning the Saxophone</li>
  <li>Laughing at memes on Twitter</li>
</ul>

<Footer />
  </div>
  </div>
</template>

<script>
export default {

}
</script>
<style scoped>
.container {
  margin: 0 auto;
  text-align: left;
  padding-top: 25px;
  font-family: system-ui;
}


.links {
  color: #35495e;
  text-decoration: none;
}

.links:hover {
  color: #fff;
  background-color: #35495e;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  color: #35495e;
  letter-spacing: 1px;
}

.sub-title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 25px;
  color: #35495e;
}

</style>