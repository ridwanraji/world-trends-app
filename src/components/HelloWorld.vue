<template>
  <v-container>
    <v-layout
      text-xs-center
      wrap
    >
      <v-flex xs12>
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="100"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="headline text-uppercase font-weight-bold">
          WORLD TRENDS
        </h1>
        <p class="subheading font-weight-regular">
          Whats Trending on various socials media around the world.
          <br>
        </p>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline text-uppercase">WHATS TRENDING ON TWITTER?</h2>

        <v-layout justify-center>
          <v-card
            class="mx-auto"
            color="#26c6da"
            dark
            max-width="400"


            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            target="_blank"
            
          >
            <v-card-title>
              <v-icon
                large
                left
              >
                mdi-twitter
              </v-icon>
              <span class="title font-weight-light">Twitter</span>
            </v-card-title>
            
            <v-card-text class="headline font-weight-bold">
              {{ next.text }}
            </v-card-text>

            <v-card-actions>
              <v-list-tile class="grow">
                <v-list-tile-avatar color="grey darken-3">
                  <v-img
                    class="elevation-6"
                    src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
                  ></v-img>
                </v-list-tile-avatar>

                <v-list-tile-content>
                  <v-list-tile-title> World Trends </v-list-tile-title>
                </v-list-tile-content>

                <v-layout
                  align-center
                  justify-end
                >
                
                <v-icon class="mr-1">mdi-heart</v-icon>
                <span class="subheading mr-2">256</span>
                <span class="mr-1">·</span>
                <v-icon class="mr-1">mdi-share-variant</v-icon>
                <span class="subheading">45</span>
                </v-layout>
              </v-list-tile>
            </v-card-actions>
          </v-card>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      whatsNext: [
        {
          text: 'Explore components',
          href: 'https://vuetifyjs.com/components/api-explorer'
        },
        {
          text: 'Select a layout',
          href: 'https://vuetifyjs.com/layout/pre-defined'
        },
        {
          text: 'Frequently Asked Questions',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions'
        }

      ]
    })
  }
</script>

<style>

</style>
