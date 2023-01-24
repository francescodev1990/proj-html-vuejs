<script>
export default {
  data() {
    return {
      menu: [
        {
          label: "HOME",
          url: "#",
          active: false,
        },
        {
          label: "MISSION",
          url: "#",
          active: false,
        },
        {
          label: "CAUSES",
          url: "#",
          active: false,
        },
        {
          label: "JOURNAL",
          url: "#",
          active: false,
        },
        {
          label: "DONATE",
          url: "#",
          active: false,
        },
      ],
    };
  },
};
</script>


<template lang="">
  <header>
    <a href="/" class = "brand">
      <img src="../assets/images/avada-logo.png">
    </a>
    <nav>
      <ul>
        <li v-for = "(item, index) in menu" ::key = "i">
          <a :href="item.url" :class = "item.active ? 'active' :''"> {{item.label}}
          </a>

        </li>
      </ul>
    </nav>
  </header>
</template>



<style lang="scss">
header {
  text-align: center;
  margin-top: 25px;
  display: flex;
  justify-content: space-around;
}
ul {
  list-style-type: none;
  display: flex;
}
ul li {
  padding: 25px;
  margin-left: 2px;
}
</style>