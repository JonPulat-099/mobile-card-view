<script setup>
const products = [


  {
    id: 1,
    name: 'Карта Visa Start',
    href: '/view?version=v2',
    imageSrc: 'https://ru.ipakyulibank.uz/uploads/images/widget/2024/05/widget_1715843113_2633.png.webp',
    imageAlt: "Front of men's Basic Tee in black.",
    price: '0 UZS',
    color: 'Black',
  },
  {
    id: 1,
    name: 'Карта Mastercard Virtual',
    href: '/view?version=v3',
    imageSrc: 'https://ru.ipakyulibank.uz/uploads/images/widget/2022/10/widget_1666789327_1834.png',
    imageAlt: "Front of men's Basic Tee in black.",
    price: '0 UZS',
    color: 'Black',
  },
  // More products...
]
</script>

<template>
  <main>
    <div>
    <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
      <h2 class="text-2xl font-bold tracking-tight dark:text-white">Банковские платежные карты</h2>

      <div class="mt-6 grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
        <div v-for="product in products" :key="product.id" class="group relative">
          <div class="flex items-center justify-center p-2  aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-md bg-gray-200 lg:aspect-none group-hover:opacity-75 lg:h-80">
            <img :src="product.imageSrc" :alt="product.imageAlt" class="object-cover object-center" />
          </div>
          <div class="mt-4 flex justify-between">
            <div>
              <h3 class="text-sm dark:text-white">
                <RouterLink :to="product.href">
                  <span aria-hidden="true" class="absolute inset-0" />
                  {{ product.name }}
                </RouterLink>
              </h3>
            </div>
            <p class="text-sm font-medium dark:text-[#9EAEBC]">{{ product.price }}</p>
          </div>
        </div>
      </div>
    </div>
  </div> 
  </main>
</template>
