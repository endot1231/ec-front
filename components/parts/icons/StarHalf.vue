<template>
  <div class="star-half">
    <svg fillrule="evenodd" viewBox="0 0 24 24" class="star-filled" width="16" height="16">
      <path class="cls-1"
        d="M11.37,2.83,8.66,8.32,2.6,9.2A.74.74,0,0,0,2,9.68a.72.72,0,0,0,.18.72L6.6,14.67l-1,6a.72.72,0,0,0,.28.69.73.73,0,0,0,.74.05L12,18.6V2.47A.69.69,0,0,0,11.37,2.83Z">
      </path>
    </svg>

    <svg fillrule="evenodd" viewBox="0 0 24 24" class="star-empty" width="16" height="16">
      <path class="cls-1"
        d="M22,9.69a.72.72,0,0,0-.57-.48l-6.06-.88L12.63,2.86a.73.73,0,0,0-1.26,0L8.66,8.33,2.6,9.21A.72.72,0,0,0,2,9.69a.69.69,0,0,0,.18.71L6.6,14.66l-1,6a.71.71,0,0,0,.28.69.73.73,0,0,0,.74.05L12,18.58l5.42,2.84a.72.72,0,0,0,.74-.05.71.71,0,0,0,.28-.69l-1-6,4.39-4.26A.69.69,0,0,0,22,9.69Z">
      </path>
    </svg>
  </div>
</template>

<style lang="scss" scoped>
.star-half {
  position: relative;
  display: inline-block;
}

.star-filled {
  fill: #ffb818;
  z-index: 2;
  position: relative;
}

.star-empty {
  position: absolute;
  left: 0;
  fill: #ccc;
}
</style>  