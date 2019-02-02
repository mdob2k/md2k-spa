<template>
  <footer class="footer">
    <div class="container">
      <div class="columns is-vcentered">
        <div class="column is-4">
          <div class="level">
            <div class="level-left">
              <a
                href="https://bulma.io"
                class="level-item"
              >
                <img
                  src="/images/made-with-bulma--dark.png"
                  alt="Made with Bulma"
                  width="128"
                  height="24"
                >
              </a>
              <p class="level-item">
                Build with
                <a
                  href="http://nuxtjs.org"
                  class="has-margin-left-xs"
                >Nuxt</a>
              </p>
              <a
                href="https://vuejs.org/"
                class="level-item"
              >
                <span class="icon">
                  <i class="fab fa-vuejs"/>
                </span>
                <span>Vue.js</span>
              </a>
            </div>
          </div>
        </div>
        <div class="column is-4">
          <div class="buttons is-centered">
            <a
              href="https://github.com/mdob2k"
              class="button"
            >
              <span class="icon">
                <i class="fab fa-github"/>
              </span>
              <span>Github</span>
            </a>
          </div>
        </div>
        <div class="column is-4">
          <div class="level">
            <div class="level-left"/>
            <div class="level-right">
              <p class="level-item">
                <span class="icon">
                  <i class="far fa-copyright"/>
                </span>
                <span>{{ currentYear }}</span>
                <a
                  class="has-text-weight-bold has-margin-left-xs"
                  href="https://md2k.de"
                >md2k.de</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "VFooter",
  data: () => {
    return {
      currentYear: new Date().getFullYear()
    };
  }
};
</script>

<style lang="scss">
$sizeUnit: rem;
$marginKey: "has-margin";
$paddingKey: "has-padding";
$separator: "-";
$sizes: (
  ("none", 0),
  ("xxs", 0.125),
  ("xs", 0.25),
  ("sm", 0.5),
  ("md", 1),
  ("lg", 2),
  ("xl", 4),
  ("xxl", 8)
);
$positions: (
  ("top", "top"),
  ("right", "right"),
  ("bottom", "bottom"),
  ("left", "left")
);

@function sizeValue($key, $value) {
  @return if($key == "none", 0, $value + $sizeUnit);
}

@each $size in $sizes {
  $sizeKey: nth($size, 1);
  $sizeValue: nth($size, 2);
  .#{$marginKey}#{$separator}#{$sizeKey} {
    margin: sizeValue($sizeKey, $sizeValue);
  }
  .#{$paddingKey}#{$separator}#{$sizeKey} {
    padding: sizeValue($sizeKey, $sizeValue);
  }
  @each $position in $positions {
    $posKey: nth($position, 1);
    $posValue: nth($position, 2);
    .#{$marginKey}#{$separator}#{$posKey}#{$separator}#{$sizeKey} {
      margin-#{$posValue}: sizeValue($sizeKey, $sizeValue);
    }
    .#{$paddingKey}#{$separator}#{$posKey}#{$separator}#{$sizeKey} {
      padding-#{$posValue}: sizeValue($sizeKey, $sizeValue);
    }
  }
}
</style>
