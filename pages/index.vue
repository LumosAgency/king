<template>
  <div>
    <Hero />
    <div class="container intro">
      <div class="col__100">
        <h2>Where cats come to <span>Play and Stay</span></h2>
      </div>
      <div class="col__50">
        <div class="intro__image">
          <XyzTransition appear-visible>
            <div
              class="xyz-appear"
              xyz="fade down"
              :appear-visible="{ threshold: 0.5, rootMargin: '50px' }"
            >
              <img
                src="~/assets/img/cat-friends.jpg"
                class="img__center img__rounded"
                alt="Picture of cute cats"
              />
            </div>
          </XyzTransition>
        </div>
        <div class="intro__text" xyz="appear-visible fade down">
          <h2><span>Where cats come to</span> Play and Stay</h2>
          <p>
            At The Cat's Meow, we understand that your cats are more than just
            pets - they are family. That's why we provide the highest quality
            care and attention for our four-legged guests in a safe and
            luxurious setting. Our resort is uniquely designed to provide
            enrichment and stimulation in a natural environment, with spacious
            suites, interactive toys, and plenty of fresh air.
          </p>
          <NuxtLink to="/about" v-bind:class="'button'">Book Meow</NuxtLink>
        </div>
      </div>
    </div>
    <div class="container purfection">
      <div class="col__50">
        <div>
          <h3>
            <span class="left">Pamper your cat to </span
            ><span class="right">Purrrrrrrrrrrfection</span>
          </h3>
          <Accordion :items="accordionItems" />
        </div>
        <XyzTransition appear-visible>
          <div
            class="xyz-appear"
            xyz="fade down"
            :appear-visible="{ threshold: 0.5, rootMargin: '50px' }"
          >
            <img
              src="~/assets/img/pamper.jpg"
              class="img__center img__rounded"
              alt="Photo of cat face"
            />
          </div>
        </XyzTransition>
      </div>
    </div>
    <div class="container carousel xyz-appear" xyz="fade down">
      <div class="col__100">
        <Carousel />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      accordionItems: [
        {
          title: 'Dining',
          content:
            "Grooming services include professional bathing, brush-outs, nail trims, ear cleaning, and even fur styling. The resort also offers spa services such as massages, facials, and aromatherapy treatments to pamper the cats. Grooming and spa services are designed to enhance the cat's physical appearance and overall well-being. Additionally, the resort provides personalized grooming services tailored to the specific needs of each cat, such as specialized shampoos for sensitive skin or hypoallergenic grooming products for cats with allergies. With professional grooming services, cats can look and feel their best during their stay at the luxury cat resort",
        },
        {
          title: 'Grooming and Spa Services',
          content:
            "Grooming services include professional bathing, brush-outs, nail trims, ear cleaning, and even fur styling. The resort also offers spa services such as massages, facials, and aromatherapy treatments to pamper the cats. Grooming and spa services are designed to enhance the cat's physical appearance and overall well-being. Additionally, the resort provides personalized grooming services tailored to the specific needs of each cat, such as specialized shampoos for sensitive skin or hypoallergenic grooming products for cats with allergies. With professional grooming services, cats can look and feel their best during their stay at the luxury cat resort",
        },
        {
          title: 'Playtime and Enrichment',
          content:
            "Grooming services include professional bathing, brush-outs, nail trims, ear cleaning, and even fur styling. The resort also offers spa services such as massages, facials, and aromatherapy treatments to pamper the cats. Grooming and spa services are designed to enhance the cat's physical appearance and overall well-being. Additionally, the resort provides personalized grooming services tailored to the specific needs of each cat, such as specialized shampoos for sensitive skin or hypoallergenic grooming products for cats with allergies. With professional grooming services, cats can look and feel their best during their stay at the luxury cat resort",
        },
        {
          title: 'Pet Photography and Social Media',
          content:
            "Grooming services include professional bathing, brush-outs, nail trims, ear cleaning, and even fur styling. The resort also offers spa services such as massages, facials, and aromatherapy treatments to pamper the cats. Grooming and spa services are designed to enhance the cat's physical appearance and overall well-being. Additionally, the resort provides personalized grooming services tailored to the specific needs of each cat, such as specialized shampoos for sensitive skin or hypoallergenic grooming products for cats with allergies. With professional grooming services, cats can look and feel their best during their stay at the luxury cat resort",
        },
      ],
    }
  },
}
</script>
