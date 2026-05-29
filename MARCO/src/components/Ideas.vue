<template>
  <section class="ideas">
    <div class="ideas__intro">
        <div class="ideas__cta">
      <h3>AKO JE MESO KVALITETNO, JELO NE MOŽE BITI LOŠE</h3>
      <p>
        Preko 500.000 zadovoljnih kupaca već je uživalo u MARCO proizvodima.
        Budi i ti jedan od njih.
      </p>
      <p>Otkrij naše proizvode</p>
    </div>
      <span class="ideas__eyebrow">MARCO Taste Inspiration</span>
      <h2>Inspiracija za svaki zalogaj</h2>
      <p>
        Od tradicionalnog doručka do modernih gourmet jela — MARCO proizvodi daju
        svakom obroku karakter, miris i ukus koji se pamti.
      </p>
      
    </div>

    <div
      v-for="category in categories"
      :key="category.title"
      class="ideas__category"
    >
      <div class="ideas__category-head">
        <div>
          <span>{{ category.label }}</span>
          <h3>{{ category.title }}</h3>
        </div>
        <p>{{ category.description }}</p>
      </div>

      <div class="ideas__slider">
        <article
          v-for="item in category.items"
          :key="item.title"
          class="ideas__card"
        >
          <img :src="item.image" :alt="item.title" />

          <div class="ideas__card-overlay">
            <span>{{ item.product }}</span>
            <h4>{{ item.title }}</h4>
            <p>{{ item.text }}</p>
          </div>
        </article>
      </div>
    </div>

    
  </section>
</template>

<script setup>
import "../assets/styles/Ideas.css";

const categories = [
  {
    label: "01",
    title: "Njeguški pršut",
    description: "Tradicionalan, elegantan i savršen za svaki sto.",
    items: [
      {
        title: "Njeguška plata",
        product: "Pršut",
        text: "Sir, masline, domaći hljeb i pršut — klasik koji uvijek prodaje.",
        image: "/src/assets/images-food/njeguska-plata.webp"
      },
      {
        title: "Pizza sa pršutom",
        product: "Pršut",
        text: "Topla pizza, rukola i tanko sječena pršuta za premium ukus.",
        image:
         "https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&w=900&q=80",
      },
      {
        title: "Pasta sa pršutom",
        product: "Pršut",
        text: "Kremasta pasta u kojoj pršuta daje dubinu i aromu.",
        image:
          "https://images.unsplash.com/photo-1551183053-bf91a1d81141?auto=format&fit=crop&w=900&q=80",
      },
      {
        title: "Pršut i dinja",
        product: "Pršut",
        text: "Slatko i slano u savršenom balansu.",
        image:
          "https://images.unsplash.com/photo-1604908176997-125f25cc6f3d?auto=format&fit=crop&w=900&q=80",
      },
    ],
  },
  {
    label: "02",
    title: "Panceta",
    description: "Bogata, hrskava i stvorena za jela punog ukusa.",
    items: [
      {
        title: "Burger sa pancetom",
        product: "Panceta",
        text: "Hrskava panceta podiže burger na potpuno novi nivo.",
        image:
          "https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=900&q=80",
      },
      {
        title: "Carbonara",
        product: "Panceta",
        text: "Kremasta pasta sa komadima pancete i punim ukusom.",
        image:
          "https://images.unsplash.com/photo-1608756687911-aa1599ab3bd9?auto=format&fit=crop&w=900&q=80",
      },
      {
        title: "Jaja sa pancetom",
        product: "Panceta",
        text: "Doručak koji miriše na domaću kuhinju.",
        image:
          "https://images.unsplash.com/photo-1525351484163-7529414344d8?auto=format&fit=crop&w=900&q=80",
      },
      {
        title: "Krompir sa pancetom",
        product: "Panceta",
        text: "Jednostavno jelo koje postaje posebno uz dobar mesni ukus.",
        image:
          "https://images.unsplash.com/photo-1518013431117-eb1465fa5752?auto=format&fit=crop&w=900&q=80",
      },
    ],
  },
  {
    label: "03",
    title: "Suvi vrat",
    description: "Mekan, aromatičan i odličan za lagane premium obroke.",
    items: [
      {
        title: "Ciabatta sa suvim vratom",
        product: "Suvi vrat",
        text: "Idealan sendvič za brz, ali kvalitetan obrok.",
        image:
          "/src/assets/images-food/ciabata.jpg",
      },
      {
        title: "Burata sa suvim vratom",
        product: "Suvi vrat",
        text: "Kremasta burrata i pažljivo odležani suvi vrat u savršenoj harmoniji ukusa.",       
         image:
          "/src/assets/images-food/buratasa-suvim-vratom.jpg",
      },
      {
        title: "Plata za vino",
        product: "Suvi vrat",
        text: "Suvi vrat, pršut i tvrdi sirevi — kombinacija za uživanje.",
        image:
          "/src/assets/images-food/plata-za-vino.jpg",
      },
    ],
  },
  {
    label: "04",
    title: "Pečenica",
    description: "Čist, nježan i prepoznatljiv ukus mesa.",
    items: [
      {
        title: "Premium panini",
        product: "Pečenica",
        text: "Topao sendvič sa sirom, pečenicom i hrskavom koricom.",
        image:
          "https://images.unsplash.com/photo-1553909489-cd47e0907980?auto=format&fit=crop&w=900&q=80",
      },
      {
        title: "Club sandwich",
        product: "Pečenica",
        text: "Slojevi mesa, sira i svježeg povrća.",
        image:
          "https://images.unsplash.com/photo-1567234669003-dce7a7a88821?auto=format&fit=crop&w=900&q=80",
      },
      {
        title: "Pečenica i sir",
        product: "Pečenica",
        text: "Jednostavno, elegantno i uvijek primamljivo.",
        image:
          "https://images.unsplash.com/photo-1452195100486-9cc805987862?auto=format&fit=crop&w=900&q=80",
      },
    ],
  },
];
</script>