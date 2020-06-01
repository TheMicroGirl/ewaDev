<template>
  <div class="container">
    <div class="">
       <div class="greetingStyle anime"> {{greeting}}</div>
       <!-- <p> Welcome to my corner of the internet</p> -->
       
       
    </div>

  </div>
  
</template>

<script lang="ts">

export default {

  asyncData (context) {
 
    function determineGreeting() : string {
      const greetings = ['Hello.', 'O hai there.', 'Howdy.', 'Awright?']
      const rand = Math.floor(Math.random() * greetings.length);
      return greetings[rand];
    }

     return { greeting: determineGreeting() }
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.greetingStyle{
    font-family: 'Montserrat', sans-serif;
    font-weight: 900;
    font-size: 100px;
}

.anime {
    overflow: hidden; /* Ensures the content is not revealed until the animation */
        border-right: .15em solid black; /* The typwriter cursor */
        white-space: nowrap; /* Keeps the content on a single line */
        margin: 1 auto; /* Gives that scrolling effect as the typing happens */
        letter-spacing: .15em; /* Adjust as needed */
        animation: 
          typing 0.5s steps(40, end),
          blink-caret 0.8s step-end infinite;
    
      }
 
  /* The typing effect */
  @keyframes typing {
    from { width: 0 }
    to { width: 100% }
  }
  
  /* The typewriter cursor effect */
  @keyframes blink-caret {
    from, to { border-color: transparent }
    50% { border-color: black; }
  }
</style>
