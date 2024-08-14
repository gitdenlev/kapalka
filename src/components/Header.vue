<script></script>

<template>
  <header>
    <div class="logo__container">
      <img src="/logo.svg" alt="" width="35" />
      <h1>Kapalka</h1>
    </div>
    <div class="score__container">
      <div class="score"><img src="/check.svg" alt="" width="30" />3</div>
    </div>
  </header>
</template>

<style scoped lang="scss">
@import "../assets/styles/_vars.scss";
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px;
  height: 60px;
  background-color: $header-bg;
  color: #fff;

  .logo__container {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
    gap: 10px;

    h1 {
      font-size: 39px;
      margin-top: 10px;
      background: linear-gradient(
        90deg,
        rgba(121, 25, 255, 0.685),
        rgba(255, 200, 200, 0.685),
        rgba(121, 25, 255, 0.685)
      );
      background-size: 300%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: text-glow 2s ease-in-out infinite;

      @keyframes text-glow {
        0% {
          background-position: 0% 50%;
        }
        50% {
          background-position: 100% 50%;
        }
        100% {
          background-position: 0% 50%;
        }
      }
    }
  }
}

.score__container {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
  gap: 10px;
  margin-top: 10px;

  .score {
    min-width: 100px;
    height: 50px;
    border-radius: 10px;
    border: 1px solid #aaf76f;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 30px;
    gap: 10px;
    padding: 0 15px;
    white-space: nowrap;
  }
}
</style>
