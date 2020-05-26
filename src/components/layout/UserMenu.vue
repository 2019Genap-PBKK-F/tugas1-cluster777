<template>
  <li class="dropdown user user-menu">
    <a href="javascript:;" class="dropdown-toggle" data-toggle="dropdown">
      <!-- The user image in the navbar-->
      <img :src="user.avatar" class="user-image" alt="User Image">
      <!-- hidden-xs hides the username on small devices so only the image appears. -->
      <span class="hidden-xs">{{user.displayName}}</span>
    </a>
    <!-- Account Info and Menu -->
    <ul class="dropdown-menu">
      <li class="user-header" style="height:auto;min-height:85px;padding-bottom:15px;">
        <p>
          <span>{{user.displayName}}</span>
          <small v-for="role in user.roles" :key="role">{{role}}</small>
        </p>
      </li>
      <li class="user-footer">
        <div>
          <button v-on:click="logouut()">
            <i class='fa fa-sign-out'></i>
            <span>logout</span>
          </button>
        </div>
      </li>
    </ul>
  </li>
</template>

<script>
export default {
  name: 'UserMenu',
  props: ['user'],
  methods: {
    logouut: function() {
      this.$store.commit('SET_USER', null)
      this.$store.commit('SET_TOKEN', null)

      if (window.localStorage) {
        window.localStorage.setItem('user', null)
        window.localStorage.setItem('token', null)
      }
      this.$router.push('/login')
    }
  }
}
</script>
