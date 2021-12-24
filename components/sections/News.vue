<template>
  <base-section
    id="news"
    dividerRight
    leftStyle="cols-12"
    rightStyle="d-none"
  >
    <template v-slot:left-side >
      <h4 class="section-title mb-0">Noticias destacadas</h4>
      <b-container>
        <b-row>
          <b-col
            v-for="(newsItem, index) in news" 
            :key="index"
            cols="12"
            sm="6"
            lg="4"
          >
            <div class="news-card mx-auto">
              <a 
                href="#"
              >
                <img 
                  :src="require(`~/assets/images/${newsItem.imgSrc}.png`)" 
                  :alt="newsItem.title"
                  width="336" 
                  height="186" 
                  class="img-fluid mx-auto"
                >
                <p>{{ newsItem.title }}</p>
              </a>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </template>
  </base-section>
</template>

<script>
export default {
  data() {
    return {
      news: [
        {
          imgSrc: 'news-1',
          title: 'Open Web y 4ta Revolución Industrial Un breve informativo'
        },
        {
          imgSrc: 'news-2',
          title: 'El futuro de las finanzas y la Open Web'
        },
        {
          imgSrc: 'news-3',
          title: 'La Open Web y la Privacidad'
        }
      ]
    }
  },
}
</script>

<style scoped>
#news {
  padding-top: 26px !important;
}
.section-title {
  margin-bottom: 50px !important;
}
.news-card {
  max-width: 100%;
  margin-bottom: 32px;
}

.col-12:last-child .news-card{
  margin-bottom: 0;
}

.news-card a {
  display: flex;
  flex-direction: column;
}

.news-card img {
  max-width: 100%;
  max-height: 186px;
  margin-bottom: 24px;
}

.news-card a:hover {
  color: #29c44d;
}
.news-card p {
  color: #29c44d;
  text-align: center;
}

@media (min-width: 768px) { 
  .news-card p {
    text-align: left;
  }
}

@media (min-width: 992px) { 
  .news-card {
    margin-bottom: 0;
  }
}
</style>