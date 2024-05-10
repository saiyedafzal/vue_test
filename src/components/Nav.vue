<template>
  <header class="header">
    <nav class="brand container navbar">
      Brand
      <svg
        class="burger"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <g clipPath="url(#a)">
          <path
            d="M3 6h18M3 12h18M3 18h18"
            stroke="#292929"
            strokeWidth="2.5"
            strokeLinecap="round"
            strokeLinejoin="round"
          />
        </g>
        <defs>
          <clipPath id="a">
            <path fill="#fff" d="M0 0h24v24H0z" />
          </clipPath>
        </defs>
      </svg>
      <div class="menu">
        <ul class="menu-inner">
          <li class="menu-item">
            <span class="menu-link">Home</span>
          </li>
          <li class="menu-item">
            <span class="menu-link">Feature</span>
          </li>
          <li class="menu-item">
            <span class="menu-link">Pricing</span>
          </li>
          <li class="menu-item">
            <span class="menu-link">Support</span>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<style scoped></style>
