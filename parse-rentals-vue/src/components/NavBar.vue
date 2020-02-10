<template>
  <div>
    <md-app>
      <md-app-drawer md-permanent="card">
        <md-list>
          <div id="field">
            <md-field v-for="item in thisitems" v-bind:key="item.id">
              <label>{{item.title}}</label>
              <span class="md-prefix">R$</span>
              <md-input v-model="empty"></md-input>
            </md-field>
          </div>
          <md-list-item>
            <md-icon>send</md-icon>
            <span class="md-list-item-text">Sent Mail</span>
          </md-list-item>

          <md-list-item>
            <md-icon>delete</md-icon>
            <span class="md-list-item-text">Trash</span>
          </md-list-item>

          <md-list-item>
            <md-icon>error</md-icon>
            <span class="md-list-item-text">Spam</span>
          </md-list-item>
        </md-list>
      </md-app-drawer>
    </md-app>
  </div>
</template>

<script>
export default {
  data() {
    return {
      thisitems: [
        { id: 0, title: "Preço" },
        { id: 1, title: "Aluguel" }
      ]
    };
  },
  name: "PermanentCard"
};
</script>

<style lang="scss" scoped>
.md-app {
  min-height: 100vh;
  border: 1px solid rgba(#000, 0.12);
}

// Demo purposes only
.md-drawer {
  width: 230px;
  max-width: calc(100vw);
}
#field {
  padding: 10px 20px 20px 10px;
}
</style>
