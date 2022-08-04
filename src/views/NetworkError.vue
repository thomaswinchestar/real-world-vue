<!-- eslint-disable vue/valid-template-root -->
<template>
  <div class="networkError">
    <h1>Uh-Oh!</h1>

    <h3>
      It looks like you're experencing some network issues, please take a breath
      and <a href="#" @click="$router.go(-1)">Click Here</a> to try again.
    </h3>
  </div>
</template>
