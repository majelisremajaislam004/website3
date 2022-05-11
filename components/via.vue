<template>
  <main>
    <header>
      <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.5.0/css/font-awesome.min.css" />
    </header>
    <body>
      <ul class="share-icons">
        <li class="share-icons__item">
          <a href="">
            <span>
              <i class="fa fa-facebook text-black"></i>
            </span>
          </a>
        </li>
        <li class="share-icons__item">
          <a href="">
            <span>
              <i class="fa fa-whatsapp text-black"></i>
            </span>
          </a>
        </li>
        <li class="share-icons__item">
          <a href="">
            <span>
              <i class="fa fa-instagram text-black"></i>
            </span>
          </a>
        </li>
        <li class="share-icons__item">
          <a href="">
            <span>
              <i class="fa fa-youtube-square text-black"></i>
            </span>
          </a>
        </li>
        <li class="share-icons__block">
          <div class="share-icons__block-left"><i class="fa fa-arrows-alt text-primary"></i></div>
          <div class="share-icons__block-right"><i class="fa fa-arrows-alt text-primary"></i></div>
        </li>
      </ul>
    </body>
  </main>
</template>

<style lang="scss" scoped>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
}

ul {
  padding: 0;
  margin: 0;
  list-style-type: none;
}

.share-icons {
  position: relative;
  display: flex;
  box-shadow: inset 0 -6px 10px -8px rgba(0, 0, 0, 0.3), inset 0 6px 10px -8px rgba(0, 0, 0, 0.3);
  cursor: pointer;

  &__block {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    transform: translateZ(0);
    transition: transform 0.3s, filter 0.2s;
    transition-timing-function: ease-in-out;

    &-left,
    &-right {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 100%;
      background: rgb(30, 254, 0);
      transition: 0.6s;
    }

    &-left {
      clip-path: inset(0 50% 0 0);
    }

    &-right {
      clip-path: inset(0 0 0 50%);
    }
  }

  &__item {
    padding: 0.75rem;
  }

  &:hover {
    .share-icons__block {
      filter: drop-shadow(0 0 8px rgba(0, 0, 0, 0.3));

      &-left {
        transform: translateX(-50%) scale(1.2);
      }

      &-right {
        transform: translateX(50%) scale(1.2);
      }
    }
  }
}

</style>