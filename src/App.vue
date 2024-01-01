<script setup>
import { ref } from 'vue'
const text = "I love riding motorcycle anywhere on any given day. I have three different types of motorcycle in my garage at home. My first bike is a 2013 Yamaha underbone bike. It has two main colours, red and black, but most of its body is covered by red rather than black."
const imageSrc = '//images.unsplash.com/photo-1558981359-219d6364c9c8?q=80&w=3870&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
const width = 1000

const displayText = ref(true)
const displayImage = ref(true)

const showItems = ref(true)

const favColor = 'red'

const activeCountry = ref('Nepal')

// function setActiveCountry() {
//   const userInput = prompt('Enter a country name')
//   activeCountry.value = userInput
// }

function setBhutan() {
  activeCountry.value = 'Bhutan'
}

const showCart = ref(false)

const number = ref(16)

const activeIndex = ref(0)
</script>
 
<!-- <template>
  <div>
    <h1 class="text-2xl">Country Information - {{ activeCountry }}</h1>
    <ul>
      <li class="p-5" v-show="activeCountry=='Bangladesh'">
        <h2><strong>Bangladesh</strong></h2>
        <p><strong>Capital:</strong> Dhaka</p>
        <p><strong>Population:</strong> 161356039</p>
        <p><strong>Area:</strong> 147570</p>
      </li>
      <li class="p-5" v-show="activeCountry=='India'">
        <h2><strong>India</strong></h2>
        <p><strong>Capital:</strong> New Delhi</p>
        <p><strong>Population:</strong> 1380004385</p>
        <p><strong>Area:</strong> 3287240</p>
      </li>
      <li class="p-5" v-show="activeCountry=='Nepal'">
        <h2><strong>Nepal</strong></h2>
        <p><strong>Capital:</strong> Kathmandu</p>
        <p><strong>Population:</strong> 29996478</p>
        <p><strong>Area:</strong> 147181</p>
      </li>
      <li class="p-5" v-show="activeCountry=='Bhutan'">
        <h2><strong>Bhutan</strong></h2>
        <p><strong>Capital:</strong> Thimphu</p>
        <p><strong>Population:</strong> 754388</p>
        <p><strong>Area:</strong> 38394</p>
      </li>
    </ul>

    <div>
      <button @click="setActiveCountry()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Set Active Country
      </button> 
      <button @click="activeCountry='Bangladesh'" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Bangladesh
      </button>
      <button @click="activeCountry='Nepal'" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Nepal
      </button>
      <button @click="setBhutan()" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Bhutan
      </button>
      <button @click="activeCountry='India'" class="ml-5 bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        India
      </button>
    </div>
  </div> 

  <div class="container mx-auto">
    <div>
      <h1 class="text-2xl">A Beautiful Motorcycle</h1>
      <img v-show="displayImage" class="mt-5" :width="width" :src="imageSrc" alt="logo" />
      <p v-show="displayText" class="mt-5 text-xl">
        {{ text }}
      </p>
      <button @click="displayImage = !displayImage" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Toggle Image
      </button>
      <button @click="displayText = !displayText" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded ml-5">
        Toggle Text
      </button>
    </div>
  </div> 
</template> -->

<!-- <template>
  <div class="relative z-10" aria-labelledby="slide-over-title" role="dialog" aria-modal="true">
    <div class="fixed inset-0 p-10 bg-gray-100 bg-opacity-75 transition-opacity">
      <button @click="showCart=true" class="bg-blue-500 hover:bg-blue-700 z-50 text-white font-bold py-2 px-4 rounded">
        Display Shopping Cart
      </button>
    </div>
    <div v-show="showCart" class="pointer-events-none fixed inset-y-0 right-0 flex max-w-full pl-10">
      <div class="pointer-events-auto w-screen max-w-md">
        <div class="flex h-full flex-col overflow-y-scroll bg-white shadow-xl">
          <div class="flex-1 overflow-y-auto px-4 py-6 sm:px-6">
            <div class="flex items-start justify-between">
              <h2 class="text-lg font-medium text-gray-900" id="slide-over-title">Shopping cart</h2>
              <div class="ml-3 flex h-7 items-center">
                <button @click="showCart=false" type="button" class="relative -m-2 p-2 text-gray-400 hover:text-gray-500">
                  <span class="absolute -inset-0.5"></span>
                  <span class="sr-only">Close panel</span>
                  <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                  </svg>
                </button>
              </div>
            </div>

            <div class="mt-8">
              <div class="flow-root">
                <ul role="list" class="-my-6 divide-y divide-gray-200">
                  <li class="flex py-6">
                    <div class="h-24 w-24 flex-shrink-0 overflow-hidden rounded-md border border-gray-200">
                      <img src="https://tailwindui.com/img/ecommerce-images/shopping-cart-page-04-product-01.jpg" alt="Salmon orange fabric pouch with match zipper, gray zipper pull, and adjustable hip belt." class="h-full w-full object-cover object-center">
                    </div>

                    <div class="ml-4 flex flex-1 flex-col">
                      <div>
                        <div class="flex justify-between text-base font-medium text-gray-900">
                          <h3>
                            <a href="#">Throwback Hip Bag</a>
                          </h3>
                          <p class="ml-4">$90.00</p>
                        </div>
                        <p class="mt-1 text-sm text-gray-500">Salmon</p>
                      </div>
                      <div class="flex flex-1 items-end justify-between text-sm">
                        <p class="text-gray-500">Qty 1</p>

                        <div class="flex">
                          <button type="button" class="font-medium text-indigo-600 hover:text-indigo-500">Remove</button>
                        </div>
                      </div>
                    </div>
                  </li>
                  <li class="flex py-6">
                    <div class="h-24 w-24 flex-shrink-0 overflow-hidden rounded-md border border-gray-200">
                      <img src="https://tailwindui.com/img/ecommerce-images/shopping-cart-page-04-product-02.jpg" alt="Front of satchel with blue canvas body, black straps and handle, drawstring top, and front zipper pouch." class="h-full w-full object-cover object-center">
                    </div>

                    <div class="ml-4 flex flex-1 flex-col">
                      <div>
                        <div class="flex justify-between text-base font-medium text-gray-900">
                          <h3>
                            <a href="#">Medium Stuff Satchel</a>
                          </h3>
                          <p class="ml-4">$32.00</p>
                        </div>
                        <p class="mt-1 text-sm text-gray-500">Blue</p>
                      </div>
                      <div class="flex flex-1 items-end justify-between text-sm">
                        <p class="text-gray-500">Qty 1</p>

                        <div class="flex">
                          <button type="button" class="font-medium text-indigo-600 hover:text-indigo-500">Remove</button>
                        </div>
                      </div>
                    </div>
                  </li>

                </ul>
              </div>
            </div>
          </div>

          <div class="border-t border-gray-200 px-4 py-6 sm:px-6">
            <div class="flex justify-between text-base font-medium text-gray-900">
              <p>Subtotal</p>
              <p>$262.00</p>
            </div>
            <p class="mt-0.5 text-sm text-gray-500">Shipping and taxes calculated at checkout.</p>
            <div class="mt-6">
              <a href="#" class="flex items-center justify-center rounded-md border border-transparent bg-indigo-600 px-6 py-3 text-base font-medium text-white shadow-sm hover:bg-indigo-700">Checkout</a>
            </div>
            <div class="mt-6 flex justify-center text-center text-sm text-gray-500">
              <p>
                or
                <button type="button" class="font-medium text-indigo-600 hover:text-indigo-500">
                  Continue Shopping
                  <span aria-hidden="true"> &rarr;</span>
                </button>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template> -->

<!-- <template>
  <p class="mb-5">
    <span>{{  number  }}</span> -->
    <!-- <span v-show="number % 2 == 0"> is even </span>
    <span v-show="number % 2 == 1"> is odd</span> -->

    <!-- <span v-if="number % 2 == 0"> is even </span>
    <span v-if="number % 2 == 1"> is odd</span> -->

    <!-- <span v-if="number % 2 == 0"> is even </span>
    <span v-else> is odd</span> -->
  <!-- </p>
  <button @click="number++" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
    Increase
  </button>
</template> -->

<template>
  <div class="py-4 lg:py-20 flex flex-col gap-12 lg:flex-row">
    <div class="w-1/2 lg:w-5/12 overflow-hidden">
      <img src="//boonik.org/wp-content/themes/boonik-theme/images/faq.svg" alt="Faq">
    </div>
    <div>
      <h2 class="text-3xl font-bold mb-4">Frequently Asked Questions</h2>
      <div class="flex flex-col gap-4">
        <div class="flex flex-col gap-2">
          <h3 @click="activeIndex=0" class="cursor-pointer text-xl font-bold border border-2 border-gray-400 py-4 px-5">What is Lorem Ipsum?</h3>
          <p v-show="activeIndex==0" class=" text-gray-500 border border-2 border-gray-400 py-4 px-5">Lorem Ipsum is simply dummy text of the printing and typesetting industry.</p>
        </div>
        <div class="flex flex-col gap-2">
          <h3 @click="activeIndex=1" class="cursor-pointer  text-xl font-bold border border-2 border-gray-400 py-4 px-5">Why do we use it?</h3>
          <p v-show="activeIndex==1" class=" text-gray-500 border border-2 border-gray-400 py-4 px-5">It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.</p>
        </div>
        <div class="flex flex-col gap-2">
          <h3 @click="activeIndex=2" class="cursor-pointer text-xl font-bold border border-2 border-gray-400 py-4 px-5">Where does it come from?</h3>
          <p v-show="activeIndex==2" class=" text-gray-500 border border-2 border-gray-400 py-4 px-5">Contrary to popular belief, Lorem Ipsum is not simply random text.</p>
        </div>
        <div class="flex flex-col gap-2">
          <h3 @click="activeIndex=3" class="cursor-pointer  text-xl font-bold border border-2 border-gray-400 py-4 px-5">Where can I get some?</h3>
          <p v-show="activeIndex==3" class=" text-gray-500 border border-2 border-gray-400 py-4 px-5">There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.</p>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped></style>