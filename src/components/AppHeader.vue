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
      ],
    };
  },
};
</script>


<template lang="">

<!-- INIZIO HEADER -->

  <header>
    <a href="/" class = "brand">
      <img class="logo" src="../assets/images/avada-logo.png">
    </a>
    <nav>
      <ul>
        <li v-for = "(item, index) in menu" :key = "index">
          <a :href="item.url" :class = "item.active ? 'active' :''"> {{item.label}}
          </a>

        </li>
      </ul>
    </nav>
    <button class="header-button">
        DONATE
      </button>
  </header>
</template>



<style lang="scss">
.logo {
  margin-top: 30px;
}
.header-button {
  vertical-align: middle;
  padding: 0;
  width: 150px;
  height: 50px;
  background-color: #fec96b;
  font-size: 20px;
  font-weight: bold;
  border-radius: 7px;
  border: none;
  color: white;
}

header {
  width: 100%;
  top: 0;
  position: fixed;
  text-align: center;
  display: flex;
  justify-content: space-around;
  background-image: url(../assets/images/jumbo.jpeg);
}

ul {
  list-style-type: none;
  display: flex;
}
ul li {
  padding: 25px;
  margin-left: 2px;
  display: flex;
  justify-content: flex-end;
}
li a {
  display: inline-block;
  padding: 1rem;
  text-decoration: none;
  font-weight: 600;
  transition: 0.3s;
  color: white;

  &.active,
  &:hover {
    border-bottom: 4px solid white;
  }
}
button {
  background-color: #fec96b;
  font-size: 20px;
  border-radius: 7px;
  border: none;
  padding: 20px;
  color: white;
  height: 25px;
  margin: 15px;
}
</style>