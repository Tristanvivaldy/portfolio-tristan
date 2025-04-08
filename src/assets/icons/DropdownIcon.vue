<template>
    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path
        :class="{ hidden: isOpen, block: !isOpen }"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M4 6h16M4 12h16M4 18h16"
      />
      <path
        :class="{ block: isOpen, hidden: !isOpen }"
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M6 18L18 6M6 6l12 12"
      />
    </svg>
  </template>
  
  <script>
  export default {
    name: "DropdownLogo",
    props: {
      isOpen: {
        type: Boolean,
        default: false,
      },
    },
  };
  </script>
  
  <style>
  </style>