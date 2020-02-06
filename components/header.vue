<template>
  <header class="header">
    <a href="#" class="logo">
      <img src="/logo.png" alt />
    </a>
    <nav class="nav">
      <a href="#">Commercial</a>
      <a href="#">Editorial</a>
      <a href="#">Reportage</a>
      <a href="#">Meet me</a>
    </nav>
  </header>
</template>

<style lang="less">
.header {
  display: flex;
  justify-content: space-between;
  padding: 40px 3.334% 0;

  .nav {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 83px;

    a {
      font-family: "Travels";
      font-style: normal;
      font-weight: 300;
      font-size: 15px;
      line-height: 13px;
      text-align: right;
      letter-spacing: 0.02em;
      text-transform: capitalize;
      color: #000000;
    }
  }
}

@media only screen and (max-width: 414px) {
  .header {
    .nav {
      height: 9px;
      a {
        display: none;
      }

      &::before {
        content: '';
        width: 20px;
        height: 1px;
        background: rgba(40, 40, 40, 0.57);
      }

      &::after {
        content: '';
        width: 20px;
        height: 1px;
        background: rgba(40, 40, 40, 0.57);
      }
    }
  }
}
</style>

