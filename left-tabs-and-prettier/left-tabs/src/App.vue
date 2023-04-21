<script>
import AO from "./AO.vue";
import Hierarchy from "./Hierarchy.vue";
import Groups from "./Groups.vue";
import New from "./New.vue";

export default {
  components: {
    AO,
    Hierarchy,
    Groups,
    New,
  },
  data() {
    return {
      currentTab: "AO",
      tabs: ["AO", "Hierarchy", "Groups", "New"],
    };
  },
};
</script>

<template>
  <div class="mainframe">
    <button
      v-for="tab in tabs"
      :key="tab"
      :class="['tab-button', { active: currentTab === tab }]"
      @click="currentTab = tab"
    >
      {{ tab }}
    </button>
    <component :is="currentTab" class="tab"></component>
  </div>
</template>

<style>
.main-frame {
  /* width: nnn; tms yms
  Tähän voi alkaa määritellä framen kokoja yms*/
}

.tab-button {
  padding: 6px 10px;
  border: 1px solid #ccc;
  cursor: pointer;
  background: #f0f0f0;
  margin-bottom: -1px;
  margin-right: -1px;
}

.tab-button:hover {
  background: #879d80;
}

.tab-button.active {
  background: #a3a4d7;
}

.tab {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
