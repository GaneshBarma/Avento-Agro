<template>
  <div class="about">
    <div class="flex justify-content-between align-items-center w-full">
      <div class="w-3" style="position: relative; left: 10%">
        <h1>About avento</h1>
        <span style="word-break: break-all; width: 20%">
          avento is one of the world leaders in crop protection. With our complete portfolio of
          solutions, we put into practice our purpose of bringing simplicity to agriculture.
        </span>
      </div>
      <img src="@/assets/sprayer.jpg" alt="sprayer" class="sprayer-img" />
    </div>

    <div class="flex justify-content-between align-items-center w-full">
      <img src="@/assets/wheat.jpg" alt="sprayer" class="wheat-img" />
      <div class="w-3" style="position: relative; right: 10%">
        <h1>Our Story</h1>
        <span style="word-break: break-all; width: 20%">
          avento is one of the world leaders in crop protection. With our complete portfolio of
          solutions, we put into practice our purpose of bringing simplicity to agriculture.
        </span>
      </div>
    </div>

    <div class="flex justify-content-between align-items-center w-full">
      <div class="w-3" style="position: relative; left: 10%">
        <h1>Vision</h1>
        <span style="word-break: break-all; width: 20%">
          avento is one of the world leaders in crop protection. With our complete portfolio of
          solutions, we put into practice our purpose of bringing simplicity to agriculture.
        </span>
      </div>
      <img src="@/assets/sprayer.jpg" alt="sprayer" class="sprayer-img" />
    </div>

    <div class="flex justify-content-between align-items-center w-full">
      <img src="@/assets/wheat.jpg" alt="sprayer" class="wheat-img" />
      <div class="w-3" style="position: relative; right: 10%">
        <h1>Mission</h1>
        <span style="word-break: break-all; width: 20%">
          avento is one of the world leaders in crop protection. With our complete portfolio of
          solutions, we put into practice our purpose of bringing simplicity to agriculture.
        </span>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style scoped>
.about {
  text-align: center;
  /* margin-top: 2rem; */
}

.sprayer-img {
  background-size: cover;
  border-bottom-left-radius: 19rem;
}

.wheat-img {
  background-size: cover;
  clip-path: polygon(0 0, 100% 30%, 100% 70%, 0 100%);
  overflow: hidden;
  border-top-right-radius: 25rem;
  border-bottom-right-radius: 25rem;
}
</style>
