<template>
  <header class="menu-superior">
    <div class="menu-esquerdo">
      <span><RouterLink to="/jogadores">jogadores</RouterLink> </span>
      <span><RouterLink to="/times">times</RouterLink> </span>
      <span><RouterLink to="/">Home</RouterLink> </span>
    </div>

    <div class="Menu Direito">
      <span>Sair</span>
    </div>
  </header>
</template>

<style>
header span {
  padding: 0 20px;
}

header.menu-superior {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
