<script setup>
import { ref } from 'vue'
const target = ref("typescript")
const videos = {
  typescript: 'https://www.youtube.com/embed/d56mG7DezGs',
  js: 'https://www.youtube.com/embed/W6NZfCO5SIk'
}
//yellow border
// const border="border: 0.5em solid #f0db4f; padding:5px;"
const displayBorder = ref(false)
function toggleBorder() {
  displayBorder.value = !displayBorder.value
}
const showModal = ref(false);

const countries = {
  bangladesh: {
    capital: 'Dhaka',
    population: 161356039,
    area: 147570
  },
  india: {
    capital: 'New Delhi',
    population: 1380004385,
    area: 3287240
  },
  nepal: {
    capital: 'Kathmandu',
    population: 29996478,
    area: 147181
  },
  bhutan: {
    capital: 'Thimphu',
    population: 754388,
    area: 38394
  },
}

function capitalizeFirstLetter(string) {
  return string.charAt(0).toUpperCase() + string.slice(1);
}
</script>



<!-- <template>
  <div v-if="target == 'typescript'">
    <iframe :class="displayBorder ? 'border':''" width="560" height="315" :src="videos.typescript" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
  <div v-else>
    <iframe :class="displayBorder ? 'border':''" width="560" height="315" :src="videos.js" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
  <button @click="toggleBorder()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
    Toggle Border {{ displayBorder }}
  </button>
  <div>
    what do you want to learn?
    <button @click="target='js'" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
      JS
    </button>
    <button @click="target='typescript'" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
      TS
    </button>
  </div>
</template> -->
<!-- <template>
<div class="max-w-2xl mx-auto">
    <div class="border-b border-gray-200 dark:border-gray-700 mb-4">
        <ul class="flex flex-wrap -mb-px" >
            <li class="mr-2">
                <button class="inline-block text-gray-500 border border-2 border-gray-400 py-4 px-5 hover:text-gray-600 hover:border-gray-300 rounded-t-lg py-4 px-4 text-sm font-medium text-center border-transparent border-b-2 dark:text-gray-400 dark:hover:text-gray-300" type="button">Profile</button>
            </li>
            <li class="mr-2">
                <button class="inline-block text-gray-500 border border-2 border-gray-400 py-4 px-5 hover:text-gray-600 hover:border-gray-300 rounded-t-lg py-4 px-4 text-sm font-medium text-center border-transparent border-b-2 dark:text-gray-400 dark:hover:text-gray-300 active" type="button" >Dashboard</button>
            </li>
            <li class="mr-2">
                <button class="inline-block text-gray-500 border border-2 border-gray-400 py-4 px-5 hover:text-gray-600 hover:border-gray-300 rounded-t-lg py-4 px-4 text-sm font-medium text-center border-transparent border-b-2 dark:text-gray-400 dark:hover:text-gray-300" type="button">Settings</button>
            </li>
            <li>
                <button class="inline-block text-gray-500 border border-2 border-gray-400 py-4 px-5 hover:text-gray-600 hover:border-gray-300 rounded-t-lg py-4 px-4 text-sm font-medium text-center border-transparent border-b-2 dark:text-gray-400 dark:hover:text-gray-300" type="button">Contacts</button>
            </li>
        </ul>
    </div>
    <div id="myTabContent">
        <div class="bg-gray-50 p-4 rounded-lg dark:bg-gray-800 hidden">
            <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5 dark:text-gray-400 text-sm">This is some placeholder content the <strong class="font-medium text-gray-800 dark:text-white">Profile tab's associated content</strong>. Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps classes to control the content visibility and styling.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg dark:bg-gray-800" >
            <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5 dark:text-gray-400 text-sm">This is some placeholder content the <strong class="font-medium text-gray-800 dark:text-white">Dashboard tab's associated content</strong>. Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps classes to control the content visibility and styling.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg dark:bg-gray-800 hidden">
            <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5 dark:text-gray-400 text-sm">This is some placeholder content the <strong class="font-medium text-gray-800 dark:text-white">Settings tab's associated content</strong>. Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps classes to control the content visibility and styling.</p>
        </div>
        <div class="bg-gray-50 p-4 rounded-lg dark:bg-gray-800 hidden">
            <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5 dark:text-gray-400 text-sm">This is some placeholder content the <strong class="font-medium text-gray-800 dark:text-white">Contacts tab's associated content</strong>. Clicking another tab will toggle the visibility of this one for the next. The tab JavaScript swaps classes to control the content visibility and styling.</p>
        </div>
    </div>

</div>

</template> -->
<!-- <template>
  <div class="hidden fixed z-10 inset-0 overflow-y-auto">
    <div class="flex items-end justify-center min-h-screen pt-4 px-4 pb-20 text-center sm:block sm:p-0">
      <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" aria-hidden="true"></div>
      <span class="hidden sm:inline-block sm:align-middle sm:h-screen" aria-hidden="true">&#8203;</span>
      <div class="inline-block align-bottom bg-white rounded-lg text-left overflow-hidden shadow-xl transform transition-all sm:my-8 sm:align-middle sm:max-w-lg sm:w-full">
        <div class="bg-white px-4 pt-5 pb-4 sm:p-6 sm:pb-4">
          <div class="sm:flex sm:items-start">
            <div class="mt-3 text-center sm:mt-0 sm:ml-4 sm:text-left">
              <h3 class="text-lg leading-6 font-medium text-gray-900" id="modal-title">
                Modal Title
              </h3>
              <div class="mt-2">
                <p class="text-sm text-gray-500 border border-2 border-gray-400 py-4 px-5">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid pariatur, ipsum similique veniam quo totam eius aperiam dolorum.
                </p>
              </div>
            </div>
          </div>
        </div>
        <div class="bg-gray-50 px-4 py-3 flex px-6 flex-row-reverse">
          <button type="button" class="mt-3 w-full inline-flex items-center rounded-md border border-transparent shadow-sm px-4 py-2 bg-green-600 text-base font-medium text-white hover:bg-green-700 focus:outline-none sm:ml-3 sm:w-auto sm:text-sm" >
            Accept
          </button>
          <button type="button" class="mt-3 w-full inline-flex items-center rounded-md border border-gray-300 shadow-sm px-4" >
            Cancel
          </button>
        </div>
      </div>
    </div>
  </div>
  <button type="button" class="inline-flex justify-center py-2 px-4 border border-transparent shadow-sm text-sm font-medium rounded-md text-white bg-green-600 hover:bg-green-700 focus:outline-none">
    Open Modal
  </button>

</template> -->

<!-- <template>
  <div class="py-4 lg:py-20 flex flex-col gap-12 lg:flex-row">
    <div class="w-full lg:w-5/12 overflow-hidden">
      <img src="//boonik.org/wp-content/themes/boonik-theme/images/faq.svg" alt="Faq">
    </div>
    <div>
      <h2 class="text-3xl font-bold mb-4">Frequently Asked Questions</h2>
      <div class="flex flex-col gap-4">
        <div class="flex flex-col gap-2">
          <h3 class="text-xl font-bold border border-2 border-gray-400 py-4 px-5">What is Lorem Ipsum?</h3>
          <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5">Lorem Ipsum is simply dummy text of the printing and typesetting industry.</p>
        </div>
        <div class="flex flex-col gap-2">
          <h3 class="text-xl font-bold border border-2 border-gray-400 py-4 px-5">Why do we use it?</h3>
          <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5">It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout.</p>
        </div>
        <div class="flex flex-col gap-2">
          <h3 class="text-xl font-bold border border-2 border-gray-400 py-4 px-5">Where does it come from?</h3>
          <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5">Contrary to popular belief, Lorem Ipsum is not simply random text.</p>
        </div>
        <div class="flex flex-col gap-2">
          <h3 class="text-xl font-bold border border-2 border-gray-400 py-4 px-5">Where can I get some?</h3>
          <p class="text-gray-500 border border-2 border-gray-400 py-4 px-5">There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form.</p>
        </div>
      </div>
    </div>
  </div>
</template> -->

<!-- <template>
  <div class="relative z-10" aria-labelledby="slide-over-title" role="dialog" aria-modal="true">
    <div class="fixed inset-0 p-10 bg-gray-100 bg-opacity-75 transition-opacity">
      <button class="bg-blue-500 hover:bg-blue-700 z-50 text-white font-bold py-2 px-4 rounded">
        Display Shopping Cart
      </button>
    </div>
    <div class="pointer-events-none fixed inset-y-0 right-0 flex max-w-full pl-10">
      <div class="pointer-events-auto w-screen max-w-md">
        <div class="flex h-full flex-col overflow-y-scroll bg-white shadow-xl">
          <div class="flex-1 overflow-y-auto px-4 py-6 sm:px-6">
            <div class="flex items-start justify-between">
              <h2 class="text-lg font-medium text-gray-900" id="slide-over-title">Shopping cart</h2>
              <div class="ml-3 flex h-7 items-center">
                <button type="button" class="relative -m-2 p-2 text-gray-400 hover:text-gray-500">
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
<style scoped>
/* .border {
  border: 0.5em solid #f0db4f;
  padding: 5px;
} */
</style>
