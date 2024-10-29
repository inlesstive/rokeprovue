<template>
  <Body>
      <NuxtLayout>
        <NuxtPage />
      </NuxtLayout>
  </Body>  
</template>


<style lang="scss">
@font-face {
  font-family: "CenturyGothic";  
  src: url("/public/Fonts/CenturyGothic/centurygothic_bold.ttf") format("truetype"); 
  font-style: normal; 
  font-weight: normal;
}

@font-face {
  font-family: "Myriad Pro";  
  src: url("/public/Fonts/MyriadPro/MYRIADPRO-SEMIBOLD.ttf") format("truetype"); 
  font-style: normal; 
  font-weight: 500;
}

@font-face {
  font-family: "Myriad Pro";  
  src: url("/public/Fonts/MyriadPro/MYRIADPRO-REGULAR.ttf") format("truetype"); 
  font-style: normal; 
  font-weight: 400;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: 'Myriad Pro', sans-serif;
  font-weight: 500;
}
</style>