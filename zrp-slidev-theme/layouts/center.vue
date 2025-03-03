<template>
  <div class="slidev-layout center">
    <div class="relative h-full w-full flex-col flex justify-center items-center">
      <slot></slot>
      <Bird class="absolute bottom-0 right-0 h-[24px] w-[24px]" color="white"/>
    </div>
  </div>
</template>
