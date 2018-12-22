<template lang="pug">
  <header class="header">
    <div class="header__left">
      <g-image src="~/static/images/tigw/tigw-logo.png" width="400" class="header__logo" alt="Things I Got Wrong"/>
    </div>
    <div class="header__right">
      <div class="title">
        <h2 class="tagline">Your favorite general trivia podcast with a healthy dose of internet and media things.</h2>
      </div>
      <div class="people">
        <div class="person">
        <g-image src="~/static/images/tigw/ryan_400.jpg" alt="headshot of Ryan Bott" width="300" class="avatar"/>
          <h3>Ryan Bott</h3>
          <a target="_blank" href="https://instagram.com/ryanbott" class="person__social person__social--instagram">@ryanbott</a>
          <p>Web Developer in Chicago. Music Maker. Food Crafter. Board Gamer.
            <a target="_blank" href="https://ryanbott.com/">ryanbott.com</a>
          </p>
        </div>
        <div class="person">
        <g-image src="~/static/images/tigw/rachel_400.jpg" alt="headshot of Rachel Miller" width="300" class="avatar"/>
          <h3>Rachel Miller</h3>
          <a target="_blank" href="https://instagram.com/rachelsmfr" class="person__social person__social--instagram">@rachelsmfr</a>
          <p>Lover of French and Netflix Binging. Avid Traveler and Fried Chicken Eater.
            <a target="_blank" href="https://rsmfr.com">rsmfr.com</a>
          </p>
        </div>
        <div class="person">
        <g-image src="~/static/images/tigw/stu_400.jpg" alt="headshot of Stuart Hopkins" width="300" class="avatar"/>
          <h3>Stuart Hopkins</h3>
          <a target="_blank" href="#" class="person__social link-hidden">##</a>
          <p>Web Developer, blacksmith, woodworker and plant lover.
          </p>
        </div>
        <div class="person">
        <g-image src="~/static/images/tigw/mark_400.jpg" alt="headshot of Mark Spirek" width="300" class="avatar"/>
          <h3>Mark Spirek</h3>
          <a target="_blank" href="https://instagram.com/mspirek" class="person__social person__social--twitter">@mspirek</a>
          <p>Web Developer, UI/UX expert, with a passion for product.
            <a target="_blank" href="https://markspirek.com">markspirek.com</a>
          </p>
        </div>
      </div>
    </div>
  </header>
</template>


<script>
export default {
  name: 'Header',
  data () {
    return {
      message: 'Try change me!'
    }
  },
  methods: {
    onClick () {
      this.message = 'Here you go :)'
    }
  }
}
</script>
