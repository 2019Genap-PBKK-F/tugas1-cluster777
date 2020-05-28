<template>
  <ul class="sidebar-menu">
    <li class="header">TOOLS</li>
    <router-link tag="li" class="pageLink" to="/">
      <a>
        <i class="fa fa-desktop"></i>
        <span class="page">Dashboard</span>
      </a>
    </router-link>
    <router-link tag="li" class="pageLink" to="/konkin">
      <a>
        <i class="fa fa-desktop"></i>
        <span class="page">konkin</span>
      </a>
    </router-link>
    <li class="treeview">
      <a href="#">
        <i class="fa fa-folder-o"></i>
        <span class="treeview-title">WDR</span>
        <span class="pull-right-container pull-right">
          <i class="fa fa-angle-left fa-fw"></i>
        </span>
      </a>
      <ul class="treeview-menu">
        <router-link tag="li" class="pageLink" to="/publikasiView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">publikasiView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/abmasView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">abmasView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/dosenView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">dosenView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/penelitianView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">penelitianView</span>
          </a>
        </router-link>
      </ul>
    </li>
    <li class="treeview">
      <a href="#">
        <i class="fa fa-folder-o"></i>
        <span class="treeview-title">CRUD</span>
        <span class="pull-right-container pull-right">
          <i class="fa fa-angle-left fa-fw"></i>
        </span>
      </a>
      <ul class="treeview-menu">
        <router-link tag="li" class="pageLink" to="/DataDasarView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">DataDasarView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/JenisSatkerView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">JenisSatkerView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/AspekView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">AspekView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/MasterIndikatorView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">MasterIndikatorView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/PeriodeView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">PeriodeView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/MasterIndikatorFullView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">MasterIndikatorFullView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/Indikator_PeriodeView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">Indikator_PeriodeView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/SatuanKerjaView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">SatuanKerjaView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/Capaian_UnitView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">Capaian_UnitView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/Indikator_SatuanKerjaView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">Indikator_SatuanKerjaView</span>
          </a>
        </router-link>
        <router-link tag="li" class="pageLink" to="/Indikator_SatuanKerja_LogView">
          <a>
            <i class="fa fa-desktop"></i>
            <span class="page">Indikator_SatuanKerja_LogView</span>
          </a>
        </router-link>
      </ul>
    </li>
    <li class="header">PAGES</li>
    <router-link tag="li" class="pageLink" to="/login">
      <a>
        <i class="fa fa-circle-o text-yellow"></i>
        <span class="page"> Login</span>
      </a>
    </router-link>
  </ul>
</template>
<script>
export default {
  name: 'SidebarMenu'
}
</script>
<style>
/* override default */
.sidebar-menu > li > a {
  padding: 12px 15px 12px 15px;
}

.sidebar-menu li.active > a > .fa-angle-left,
.sidebar-menu li.active > a > .pull-right-container > .fa-angle-left {
  animation-name: rotate;
  animation-duration: 0.2s;
  animation-fill-mode: forwards;
}

.treeview-title {
  z-index: 1;
}

@keyframes rotate {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(-90deg);
  }
}
</style>
