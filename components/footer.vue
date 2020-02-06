<template>
  <footer class="footer">
    <div class="social">
      <a href="#">Inst</a>
      <span></span>
      <a href="#">Fb</a>
    </div>
  </footer>
</template>

<style lang="less">
.footer {
  padding: 0 3.334% 0;
  position: fixed;
  bottom: 32px;
}

.social {
  display: flex;
  justify-content: space-between;
  width: 112px;

  a {
    font-family: "Travels";
    font-size: 15px;
    line-height: 13px;
    letter-spacing: 0.02em;
    color: #000000;
  }

  span {
    width: 56px;
    height: 1px;
    background: #393939;
    opacity: 0.24;
    align-self: center;
    background: #393939;
    opacity: 0.24;
    margin: 0 8px;
  }
}
</style>