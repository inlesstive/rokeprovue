<template>
  <button class="Faq-button">
    <span>
      <slot>Оплата/Доставка</slot>
    </span>
    <svg
      xmlns="http://www.w3.org/2000/svg"
      width="10"
      height="10"
      viewBox="0 0 10 10"
      fill="none"
      class="icon"
    >
      <circle cx="5" cy="5" r="5" fill="#D9D9D9" />
    </svg>
  </button>
</template>

<style lang="scss" scoped>
.Faq-button {
  display: flex;
  padding: 20px;
  align-items: center;
  width: 100%;
  justify-content: space-between;
  border: 1px solid #d9d9d9;
  cursor: pointer;
  transition: background-color 0.3s, color 0.3s;
  background-color: white;
  color: #17172d;

  & span {
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    text-transform: uppercase;
    text-align: left;
  }
  & svg {
    width: 10px;
    height: 10px;
  }
}

.Faq-button:hover {
  color: white;
  background-color: #3064c7;
}

.Faq-button:hover .icon circle {
  fill: #fff;
  transition: fill 0.3s;
}
</style>
