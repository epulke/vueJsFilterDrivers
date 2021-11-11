<template>
  <div>
    <h1>Welcome to F1 drivers page</h1>
  </div>
  <div class="home">
    <div>
      <Button msg="All drivers" />
      <Button msg="Mercedes" />
      <Button msg="Red Bull" />
      <Button msg="Ferrari" />
      <Button msg="McLaren" />
    </div>

    <div class="image-container" >
      <Image v-for="driver in drivers" :key="driver.id" :msg="driver.name" :style="{'background-image': 'url(' + driver.imageUrl + ')'}" />
    </div

  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Button from "@/components/Button/Button.vue";
import Image from "@/components/Image/Image.vue"; // @ is an alias to /src

export default defineComponent({
  name: "Home",
  components: {
    Image,
    Button,
  },
  data: () => {
    return {
      drivers: [
        {
          id: 1,
          name: "Lewis Hamilton",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/lewis-hamilton/_jcr_content/image.img.640.medium.jpg/1617101457462.jpg",
          team: "Mercedes"
        },
        {
          id: 2,
          name: "Valtteri Bottas",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/valtteri-bottas/_jcr_content/image.img.640.medium.jpg/1617101457255.jpg",
          team: "Mercedes"
        },
        {
          id: 3,
          name: "Max Verstappen",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/max-verstappen/_jcr_content/image.img.640.medium.jpg/1617101447981.jpg",
          team: "Red Bull"
        },
        {
          id: 4,
          name: "Sergio Perez",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/sergio-perez/_jcr_content/image.img.640.medium.jpg/1617101446970.jpg",
          team: "Red Bull"
        },
        {
          id: 5,
          name: "Charles Leclerc",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/charles-leclerc/_jcr_content/image.img.640.medium.jpg/1617101453619.jpg",
          team: "Ferrari"
        },
        {
          id: 6,
          name: "Carlos Sainz",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/carlos-sainz/_jcr_content/image.img.640.medium.jpg/1617101457421.jpg",
          team: "Ferrari"
        },
        {
          id: 7,
          name: "Lando Norris",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/lando-norris/_jcr_content/image.img.640.medium.jpg/1617101457428.jpg",
          team: "McLaren"
        },
        {
          id: 8,
          name: "Daniel Ricciardo",
          imageUrl: "https://www.formula1.com/content/fom-website/en/drivers/daniel-ricciardo/_jcr_content/image.img.640.medium.jpg/1617101458318.jpg",
          team: "McLaren"
        }
      ]
    }
  }
});
</script>

<style lang="scss">
.image-container {
  display: inline-flex;
  justify-content: center;
  flex-wrap: wrap;
  margin-left: 200px;
  margin-right: 200px;
  margin-top: 30px;
}
</style>