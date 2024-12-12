<template>
  <div class="coffee">
    <button class="menu-btn" @click="$router.push('/Navigation')">
      <img src="../assets/graphics/navicon.svg" />
    </button>
    <div class="about">
      <!-- Header background image -->
      <h1 class="text-background">Vårt Kaffe</h1>

      <h4 class="text-background">
        Pumpkin spice mug, barista cup, sit
        macchiato, kopi-luwak, doppio, grounds
        dripper, crema, strong whipped, variety
        extra iced id lungo half and half mazagran.
        Pumpkin spice.
      </h4>

      <p class="text-background">
        Que dark fair trade, spoon decaffeinated, barista
        wings whipped, as rich aftertaste, con panna milk
        black, arabica white rich beans single shot extra
        affogato. So affogato macchiato sit extraction
        instant grinder seasonal organic, turkish single shot,
        single origin, and robusta strong to go so dripper.
        Viennese froth, grounds caramelization skinny
        aromatic cup kopi-luwak, fair trade flavour,
        frappuccino medium, café au lait flavour cultivar ut
        bar instant kopi-luwak.
      </p>

      <p class="text-background">
        Roast id macchiato, single shot siphon mazagran
        milk fair trade est aroma a half and half and, so,
        galão iced to go, whipped as cream cup pumpkin
        spice iced. At extra, rich grinder, brewed to go,
        steamed half and half at, that, percolator macchiato
        trifecta and body as arabica dripper. In galão black
        java milk sit trifecta, robusta, acerbic café au lait instant shop latte.
        <br />
        
      </p>

      <!-- Person Section -->
      <div class="person">
        <img class="VD" src="../assets/graphics/eva-cortado.jpg" alt="Eva Cortado" />
        <h2>Eva Cortado</h2>
        <h5>VD & Grundare</h5>
      </div>
      
    </div>
  </div>

</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css?family=Open+Sans&display=swap");


.coffee {
  padding: 6rem 1.3rem;
  box-sizing: border-box;

  /* Add top graphics */
  background-image: url("../assets/graphics/graphics-header.svg");
  background-position: top center, bottom center;
  background-repeat: no-repeat, no-repeat;
  background-size: 100%, 100%;
  background-color: #f3e4e1; /* Base background color */
  color: black;
}

/* Add a background color for text sections */
.about {
  background-color: rgba(255, 255, 255, 0.8); /* Flat white background with slight transparency */
  padding: 1rem; /* Spacing inside the background */
  margin-bottom: 1rem; /* Space between text sections */
  border-radius: 8px; /* Rounded corners */
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Subtle shadow */
  margin-top: 20vh;
}

/* Header Styling */
h1 {
  padding-top: 20px;
  font-family: "PT Sans", sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 42px;
}

/* Subheader Styling */
h4 {
  font-weight: bold;
  font-family: "Open Sans", sans-serif;
  text-align: center;
}

/* Paragraph Text Styling */
p {
  font-family: "Work Sans", sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 14px;
  line-height: 160%;
}

/* Person Section Styling */
.person {
  display: flex;
  flex-direction: column;
  align-items: center;
}

/* Round Person Image */
.VD {
  border-radius: 50%;
}

/* Menu Button Styling */
.menu-btn {
  border: none;
  cursor: pointer;
  width: 4.8rem;
  height: 4.8rem;
  border-radius: 50%;
  // box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
  margin: 2rem;
  background-color: #ffffff00;
}

.menu-btn img {
  width: 2.6rem;
  height: 2rem;
}
</style>
