<template>
  <header>
    <div class="header-container">
      <img src = "https://github.com/upc-aplicaciones-web-grupo-4/upc-pre-202401-si730-sw53-grupo4-report-tb1/assets/149616870/6a31f6dd-dfb3-4bf5-ba54-51c4e3fb4759" alt="Logo" class="logo-image" />
      <InputText v-model="searchText" placeholder="Search" class="search-input" />
      <img src="https://github.com/ReadWell-SW54-SI729/Informe/assets/149616870/29b7cd70-60d1-46f3-81b1-d999d4b2534f" alt="Calendar" class="calendar-image" />
      <img src="https://github.com/ReadWell-SW54-SI729/Informe/assets/149616870/918527bb-69a2-4615-8b58-27939e45a97c" alt="Messages" class="messages-image" />
      <img src="https://github.com/ReadWell-SW54-SI729/Informe/assets/149616870/288269e5-3b26-4b8c-ab3a-4b8b9c5d293e" class="notifications-image" />
      <img src="https://github.com/ReadWell-SW54-SI729/Informe/assets/149616870/0d566156-d9d1-415d-904a-9e07e7610d6e" alt="Profile" class="profile-image" />
    </div>
  </header>
</template>

<script>
import InputText from 'primevue/inputtext';


export default {
  name: 'AppHeader',
  components: {
    InputText
  },
  data() {
    return {
      searchText: '',
    };
  },
  methods: {
    handleSearch() {
      console.log('Searching for:', this.searchText);
    }
  }
};
</script>

<style scoped>
header {
  background-color: #A78AAB;
  padding: 16px 2px;
  text-align: center;
}

.header-container {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}


.search-input {
  width: 20%;
  margin-left: 100px;
  border-radius: 9999px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
  outline: none;

}

.search-input:focus {
  border-color: #A78AAB;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
}


.calendar-image {
  width: 50px;
  height: 50px;
  margin-left: 100px;
  cursor: pointer;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  background-color: rgba(255, 255, 255, 0);
}

.calendar-image:hover {
  background-color: rgba(255, 255, 255, 0.1);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.messages-image {
  width: 55px;
  height: 50px;
  margin-left: 120px;
  cursor: pointer;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  background-color: rgba(255, 255, 255, 0);
}

.messages-image:hover {
  background-color: rgba(255, 255, 255, 0.1);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.notifications-image {
  width: 50px;
  height: 50px;
  margin-left: 120px;
  cursor: pointer;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  background-color: rgba(255, 255, 255, 0);
}

.notifications-image:hover {
  background-color: rgba(255, 255, 255, 0.1);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.profile-image {
  width: 55px;
  height: 50px;
  margin-left: 350px;
  cursor: pointer;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  background-color: rgba(255, 255, 255, 0);
}

.profile-image:hover {
  background-color: rgba(255, 255, 255, 0.1);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.logo-image {
  width: 50px;
  height: 50px;
  margin-left: 100px;
  border-radius: 10%;
  cursor: pointer;
}



</style>