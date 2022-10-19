<template>
  <Popover as="header" class="relative">
    <div class="bg-stone-50">
      <nav
        class="relative mx-auto flex max-w-7xl items-center justify-between px-6 pt-12 xl:px-8"
        aria-label="Global"
      >
        <div class="flex flex-1 items-center justify-between">
          <div class="flex w-full items-center justify-between lg:w-auto">
            <div>
              <span class="sr-only">Scotia Property Services</span>
              <div class="h-8 w-auto text-teal-500 sm:h-10">
                <h3
                  class="text-7xl font-extrabold uppercase leading-6 tracking-wider"
                >
                  Scotia
                </h3>
                <p class="mt-6 text-2xl tracking-widest">
                  Property Services Ltd.
                </p>
              </div>
            </div>
            <div class="-mr-2 flex items-center lg:hidden">
              <PopoverButton
                class="inline-flex items-center justify-center rounded-md bg-stone-50 p-2 text-stone-400 focus-ring-inset hover:bg-stone-100 focus:outline-none focus:ring-2 focus:ring-teal-500"
              >
                <span class="sr-only">Open main menu</span>
                <Bars3Icon class="h-6 w-6" aria-hidden="true" />
              </PopoverButton>
            </div>
          </div>
          <div class="hidden space-x-10 lg:ml-10 lg:flex">
            <a
              v-for="item in navigation"
              :key="item.name"
              :href="item.href"
              class="text-base font-medium text-stone-500 hover:text-stone-900"
              >{{ item.name }}</a
            >
          </div>
        </div>
      </nav>
    </div>

    <transition
      enter-active-class="duration-150 ease-out"
      enter-from-class="scale-95 opacity-0"
      enter-to-class="scale-100 opacity-100"
      leave-active-class="duration-100 ease-in"
      leave-from-class="scale-100 opacity-100"
      leave-to-class="scale-95 opacity-0"
    >
      <PopoverPanel
        focus
        class="absolute inset-x-0 top-0 z-30 origin-top transform p-2 transition lg:hidden"
      >
        <div
          class="overflow-hidden rounded-lg bg-white shadow-lg ring-1 ring-black ring-opacity-5"
        >
          <div class="flex items-center justify-between px-5 pt-4">
            <div></div>
            <div class="-mr-2">
              <PopoverButton
                class="inline-flex items-center justify-center rounded-md bg-white p-2 text-stone-400 hover:bg-stone-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-teal-500"
              >
                <span class="sr-only">Close menu</span>
                <XMarkIcon class="h-6 w-6" aria-hidden="true" />
              </PopoverButton>
            </div>
          </div>
          <div class="pt-5 pb-6">
            <div class="px-2 space-y-1">
              <a
                v-for="item in navigation"
                :key="item.name"
                :href="item.href"
                class="block rounded-md px-3 py-2 text-base font-medium text-stone-900 hover:bg-stone-50"
                >{{ item.name }}</a
              >
            </div>
            <div class="mt-6 px-5">
              <a
                href="#"
                class="block w-full rounded-md border border-transparent bg-teal-500 px-4 py-2 text-center font-medium text-white shadow hover:bg-teal-600"
                >Login</a
              >
            </div>
          </div>
        </div>
      </PopoverPanel>
    </transition>
  </Popover>
</template>

<script setup>
import { Popover, PopoverButton, PopoverPanel } from "@headlessui/vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";
const navigation = [
  { name: "FAQ", href: "#" },
  { name: "Contact", href: "#" },
  { name: "About", href: "#" },
];
</script>
