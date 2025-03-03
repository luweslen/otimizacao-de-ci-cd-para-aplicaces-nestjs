<template>
  <div class="slidev-layout content">
    <div class="relative h-full w-full flex-col flex justify-start items-left">
      <slot></slot>
      <Bird class="absolute bottom-0 right-0 h-[24px] w-[24px]" color="white"/>
    </div>
  </div>
</template>
