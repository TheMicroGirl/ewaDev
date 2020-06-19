<template>

  <div class="container">
    <div class="mobileSpace">
       <div class="greetingStyle anime"> 
         <p>AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA</p>  
         </div>
       <!-- <p> Welcome to my corner of the internet</p> -->
    </div>
  </div>
</template>

<script lang="ts">

export default {

  asyncData () {
 
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

.greetingStyle{
    font-family: 'Montserrat', sans-serif;
    font-weight: 900;
    font-size: 100px;
}

.anime {
  width: inherit; 
  overflow: hidden; /* Ensures the content is not revealed until the animation */
        border-right: .15em solid black; /* The typwriter cursor */
       
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
  @media screen and (max-width: 600px) {
  .mobileSpace {
     width: inherit;
  }
  .greetingStyle{
    font-family: 'Montserrat', sans-serif;
    font-weight: 900;
    font-size: 50px;
  }

}
</style>
