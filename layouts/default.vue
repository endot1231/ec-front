<template>
<div>
  <div class="header">
    <OrganismsHeader/>
  </div>
  <main>
    <slot/>
  </main>
</div>
</template>

<style scoped lang="scss">
.header,main{
  max-width: 1024px;
  width: 1024px;
  margin: auto;
}
main{
  margin-top: 40px;
}
  
</style>