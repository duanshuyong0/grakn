<template>
  <transition name="slide-fade" appear> 
        <div class="wrapper">
            <app-bar></app-bar>
            <div class="main-wrapper">
                <div class="side">
                    <epics-bar></epics-bar>
                </div>
                <div class="content">
                    <keep-alive>
                        <router-view></router-view>
                    </keep-alive>
                </div>
            </div>
        </div>
    </transition>
</template>

<style scoped>
.slide-fade-enter-active {
    transition: all 1s ease;
}
.slide-fade-enter,
.slide-fade-leave-active {
    opacity: 0;
}

.wrapper {
    display: flex;
    flex-direction: column;
    height: 100vh;
    flex: 1;
}
.main-wrapper {
    display: flex;
    flex-direction: row;
    height: 100vh;
}

.content {
    display: flex;
    flex-direction: row;
    flex: 1;
    position: relative;
}

.left-side{
    position: relative;
}

.center{
    position: relative;
    display: flex;
    flex: 1;
}

</style>

<script>
import AppBar from './Appbar.vue';
import EpicsBar from './EpicsBar.vue';


export default {
  name: 'MainTemplate',
  components: { AppBar, EpicsBar },
  data() {
    return {
    };
  },

  created() {

  },

  mounted() {
    this.$nextTick(() => {
    });
  },
  watch: {

  },
  methods: {

  },
};
</script>
