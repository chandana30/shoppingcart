<template>
  <div>
    <h1>Products</h1>
    <div class="products">
      <div v-for="(product, index) in products" :key="index">
        <h3>{{product.name}}</h3>
        <div class="cost">{{product.cost}}</div>
        <img :src="product.image" />
        <button v-on:click="addItemToCart(product)">Add to cart+</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      products: [
        {
          name: "Watch",
          cost: "$2999",
          image:
            "https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcR4V_7MbYvjZRLby04QzouxNBbOHoBHzHKt3vTnR5EW0CSIDr2I3jtN9VLXDM33BQ&usqp=CAc"
        },
        {
          name: "Phone",
          cost: "$15,990",
          image:
            "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcSoy4UU_xLsd9bYZ78gABCKmeAJ9TKmkazLDe43VI0qe3Sv4PxrrjKxp4Mb_h8vd321bPgeT3AbVw&usqp=CAc"
        },
        {
          name: "Teddy Bear",
          cost: "$330",
          image:
          "https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcTlN9l5VRyMnNKdz5noivit0dArIkjwsagPPiXkt3DeuvnZLvqnGfTWEc-1U-I2u9F0p-4MDZkVqG2Oc8yVQ5DcuoT0NTDcyCRQdloKmqjmuaL_Avc30y4q&usqp=CAE "
        },
        { 
          name: "Jwellery Set",
          cost: "$545",
          image: "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcQZiP-AS9VrPXozITB2vkZTS2-H_yE_n6DoGkKAPE0G_gfzlq1QSirC-4jGpP9GQqxBi5qcGedTgKC58M_rZsP6q8lneM6JfoIeCy44a_JZpno6-QcANFPg&usqp=CAE "
        },

       
           {
          name: "Fridge",
          cost: "$19999",
          image:
            "https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcSmFHRSZT_TIIxDPXoR8FX5zuDp0B8V8nhYNL_s7jzDD2ugR9tB2_1N54fMufG211p5R4Bvki5rCiqzM1gMf2GggcGsbxwbUiH3myN7aXIHQ5KTHvqXkVaynQ&usqp=CAE"
        },
        {
          name: "Waching Machine",
          cost: "$32000",
          image: 
            "https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcSgKy-z0z5Zquo9g2JxDoYpkXGW6KOT3vkjbn-3DQ1LqYhwXKtLwSO9TphFmVIOqHeyB5dwrw4KBeKGGp8glVjNI47OOFQsSIBrHf8Nf0cd2WcXiGkoEVs5&usqp=CAE "
        }

      ]
    };
  },
  methods: {
    addItemToCart(product) {
      this.$emit("addItemToCart", product);
    }
  }
};
</script>

<style>
</style>