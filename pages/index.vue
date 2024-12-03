<template>
  <div>
    <section class=" flex flex-row" id="cardDesign">
    </section>
    <!-- main section -->
    <section class=" flex flex-col gap-5 ">
      <!-- header section -->
      <header class="flex flex-row justify-between py-4 sticky mx-3 sm:mx-4 md:mx-10 lg:mx-32">
        <div class="flex grow items-center">
          <img class="h-10" src="/public/png-icons/logo-hapdays.png" alt="logo">
        </div>
        <div class=" hidden lg:flex grow justify-center items-center font-noto font-medium text-xl">
          <ul class="list-none flex gap-6 font-normal text-base text-black-2">
            <li>Home</li>
            <li>Package</li>
            <li>Mytrips</li>
            <li>Contact</li>
            <li>About</li>
          </ul>
        </div>
        <div class="hidden lg:flex flex-row grow justify-end items-center gap-4">
          <img class="w-7" src="/public/icon/Internet.svg" alt="language">
          <div class="rounded-full overflow-hidden bg-cover">
            <img class="w-17" src="/public/Profile-img/profile-image.jpg" alt="profile">
          </div>
        </div>
        <div class="lg:hidden flex items-center justify-center">
          <img src="/public/icon/menu-icon.svg" alt="menu_icon">
        </div>
      </header>
      <!-- Search Main service section -->
      <section
        class="grid grid-cols-1 sm:grid-cols-3 md:grid-cols-2 lg:grid-cols-7 border-[0.6px] border-Gray-3 p-3 rounded-2xl gap-3 font-noto mx-4 sm:mx-4 md:mx-5 lg:mx-16 xl:mx-20 ">
        <div class="grow flex flex-row gap-2 items-center bg-gray-100 rounded-lg px-3 py-2">
          <img class="h-6" src="/public/png-icons/hap-icon.png" alt="icon">
          <div class="flex flex-col">
            <p class="text-sm font-semibold mt-[-4px] text-black-2 ">What</p>
            <p class="text-xs text-Gray-6 mt-2-4px]">trip</p>
          </div>
        </div>
        <div class="grow flex flex-row gap-2 items-center bg-gray-100 rounded-lg px-3 py-2">
          <img class="h-6" src="/public/png-icons/location-icon.png" alt="icon">
          <div class="flex flex-col">
            <p class="text-sm font-semibold text-black-2  mt-[-4px]">Where from</p>
            <p class="text-xs text-Gray-6  mt-[-2px]">destination</p>
          </div>
        </div>
        <div class="grow flex flex-row gap-2 items-center bg-gray-100 rounded-lg px-3 py-2">
          <img class="h-6" src="/public/png-icons/location-icon.png" alt="icon">
          <div class="flex flex-col">
            <p class="text-sm font-semibold text-black-2  mt-[-4px]">Where to</p>
            <p class="text-xs text-Gray-6  mt-[-2px]">destination</p>
          </div>
        </div>
        <div class="grow flex flex-row gap-2 items-center bg-gray-100 rounded-lg px-3 py-2">
          <img class="h-6" src="/public/png-icons/calendar-icon.png" alt="icon">
          <div class="flex flex-col">
            <p class="text-sm font-semibold text-black-2  mt-[-4px]">Dates</p>
            <p class="text-xs text-Gray-6  mt-[-2px]">dd/mm/yyyy</p>
          </div>
        </div>
        <div class="grow flex flex-row gap-2 items-center bg-gray-100 rounded-lg px-3 py-2">
          <img class="h-6" src="/public/png-icons/iprofile-icon.png" alt="icon">
          <div class="flex flex-col">
            <p class="text-sm font-semibold text-black-2  mt-[-4px]">Who</p>
            <p class="text-xs text-Gray-6  mt-[-2px]">0 Male ,0 Female </p>
          </div>
        </div>
        <div class="grow flex flex-row gap-2 items-center bg-gray-100 rounded-lg px-3 py-2">
          <img class="h-6" src="/public/png-icons/category-icon.png" alt="icon">
          <div class="flex flex-col">
            <p class="text-sm font-semibold text-black-2  mt-[-4px]">Classes</p>
            <p class="text-xs text-Gray-6  mt-[-2px]">budget</p>
          </div>
        </div>
        <div
          class="flex items-center rounded-lg overflow-hidden text-lg text-gray-50 sm:col-span-3 md:col-span-2 lg:col-auto ">
          <button class="bg-yellow-300 text-white w-full h-full font-medium px-3 py-2 text-base">Search</button>
        </div>
      </section>

      <!-- Popular package section -->

      <section class="flex flex-col gap-4 font-noto mx-3 sm:mx-4 md:mx-8 lg:mx-16 xl:mx-20 relative">
        <div class="flex w-full justify-between">
          <h1 class="text-2xl font-medium text-black-3">Popular packages</h1>
        </div>
        <div
          class="absolute hidden  lg:flex flex-row w-[104%] mr-[-2%] ml-[-2%] justify-between  z-10 h-1/3 top-1/3 bottom-1/3 items-center">
          <div class="w-12 flex justify-center items-center h-12 bg-Gray-1/90 drop-shadow-xl rounded-full">
            <img class="h-4 ml-[-0.1rem]" src="/public/icon/arrow-Vector-left.svg" alt="arrow">
          </div>
          <div class="w-12 flex justify-center items-center h-12 bg-Gray-1/90 drop-shadow-xl rounded-full">
            <img class="h-4 mr-[-0.1rem]" src="/public/icon/arrow-Vector-right.svg" alt="arrow">
          </div>
        </div>
        <div class="flex flex-row gap-4 overflow-hidden">
          <div v-for="(card, index) in cardDesign" :key="index"
            class="flex flex-col max-w-60 min-w-60 gap-3 border-[0.6px] p-2 rounded-xl sm:p-3 lg:p-3 sm:max-w-60 sm:min-w-60 md:max-w-60 md:min-w-60 lg:max-w-64 lg:min-w-64">
            <div class="relative">
              <img class="w-full" :src="card.imgUrl" alt="Country Image" />
              <div style="border-top-right-radius: 24px"
                class="absolute w-10 h-10 bg-Gray-1/90 flex justify-center items-center right-3 top-3 rounded-b-full rounded-l-full">
                <img class="h-5" src="/icon/share-icon.svg" alt="Share Icon" />
              </div>
            </div>
            <div class="flex flex-row justify-between">
              <div class="flex flex-row items-center gap-1">
                <img class="w-5" src="/png-icons/location-icon.png" alt="Location Icon" />
                <p class="text-black-3 h2">{{ card.contry }}</p>
              </div>
              <p class="bg-Gray-2 text-black-3 rounded-lg px-3 pt-1 pb-2 flex justify-center items-center h2">
                {{ card.packages }}
              </p>
            </div>
          </div>
        </div>
      </section>
      <!-- Trending designations -->
      <section class="flex flex-col gap-4 font-noto mx-3 sm:mx-4 md:mx-8 lg:mx-16 xl:mx-20 relative">
        <div class="flex w-full justify-between">
          <h1 class="text-2xl font-medium text-black-3">Trending designations</h1>
        </div>
        <div
          class="absolute hidden lg:flex flex-row w-[104%] mr-[-2%] ml-[-2%] justify-between z-10 h-1/3 top-1/3 bottom-1/3 items-center">
          <div class="w-12 flex justify-center items-center h-12 bg-Gray-1/90 drop-shadow-xl rounded-full">
            <img class="h-4 ml-[-0.1rem]" src="/public/icon/arrow-Vector-left.svg" alt="arrow">
          </div>
          <div class="w-12 flex justify-center items-center h-12 bg-Gray-1/90 drop-shadow-xl rounded-full">
            <img class="h-4 mr-[-0.1rem]" src="/public/icon/arrow-Vector-right.svg" alt="arrow">
          </div>
        </div>
        <div class="flex flex-row gap-4 overflow-hidden">
          <div v-for="(card, index) in cardDesign1" :key="index"
            class="flex flex-col max-w-60 min-w-60 gap-3 border-[0.6px] p-2 rounded-xl sm:p-3 lg:p-3 sm:max-w-60 sm:min-w-60 md:max-w-60 md:min-w-60 lg:max-w-64 lg:min-w-64">
            <div class="relative">
              <img class="w-full" :src="card.imgUrl" alt="Country Image" />
              <div style="border-top-right-radius: 24px"
                class="absolute w-10 h-10 bg-Gray-1/90 flex justify-center items-center right-3 top-3 rounded-b-full rounded-l-full">
                <img class="h-5" src="/public/icon/share-icon.svg" alt="Share Icon" />
              </div>
            </div>
            <div class="flex flex-row justify-between">
              <div class="flex flex-row items-center gap-1">
                <img class="w-5" src="/public/png-icons/location-icon.png" alt="Location Icon" />
                <p class="text-black-3 h2">{{ card.contry }}</p>
              </div>
              <p class="bg-Gray-2 text-black-3 rounded-lg px-3 pt-1 pb-2 flex justify-center items-center h2">
                {{ card.packages }}
              </p>
            </div>
          </div>
        </div>
      </section>
      <!-- addSection -->
      <section>
        <div class="flex flex-row  gap-4 bg-primary-3 p-4 rounded-xl mx-3 sm:mx-4 md:mx-8 lg:mx-16 xl:mx-20">
          <div class="w-3/5 lg:w-1/5 rounded-lg overflow-hidden ">
            <img class="h-full sm:h-full lg:h-full" src="/public/banners/add-image-01.jpg" alt="banner-1">
          </div>
          <div class="w-3/5 flex flex-col justify-between">
            <div class="flex flex-col gap-1 sm:gap-4 ">
              <h2 class=" font-semibold lg:text-2xl md:text-xl sm:text-lg">Unlock seamless travels with our app</h2>
              <ul class="lg:text-base md:text-sm sm:text-xs text-xs ">
                <li>Receive flight alerts </li>
                <li>Access offline travel details</li>
                <li>Conveniently message your hotel</li>
              </ul>
            </div>
            <p class="lg:text-xl font-medium md:text-lg sm:text-base text-sm">Scan the QR code with your device camera
              and download our app</p>
          </div>
          <div class="lg:w-1/5 hidden lg:block w-1/5">
            <img class="w-full" src="/public/banners/or-code.png" alt="QR">
          </div>
        </div>
      </section>
    </section>
    <footer class="pt-10 bg-Gray-2 px-3 sm:px-4 md:px-8 lg:px-16 xl:px-20 flex flex-col gap-4">
      <div class="flex flex-col md:flex-row gap-8">
        <div class=" w-full md:w-1/4 flex flex-col gap-4">
          <h1 class="lg:text-xl font-semibold md:text-lg sm:text-base text-sm"><span
              class="text-primary-1">hap</span>days</h1>
          <div class="flex flex-col lg:flex-row md:justify-between gap-4 lg:gap-0 ">
            <div class="flex flex-row items-center gap-2 justify-start">
              <img class=" lg:w-6 md:w-6 w-4" src="/public/icon/Internet.svg" alt="internet">
              <p class="lg:text-base md:text-base sm:text-sm text-xs">English(IN)</p>
            </div>
            <div class="flex flex-row gap-2 border-[1px] border-gray-400 px-2 py-1 rounded-md w-fit">
              <img class="lg:w-6 md:w-6 w-4" src="/public/icon/flag-india.svg" alt="flag">
              <p class="lg:text-base md:text-base sm:text-sm text-xs">INR</p>
              <img class="lg:w-6 md:w-6 w-4" src="/public/icon/arrow-down.svg" alt="arrow">
            </div>
          </div>
        </div>
        <div class=" w-full md:w-1/4 flex flex-col gap-4">
          <h1 class="lg:text-xl font-semibold md:text-lg sm:text-base text-sm">Company</h1>
          <div class="flex flex-col lg:text-base md:text-base sm:text-sm text-xs">
            <a href="">Jobs</a>
            <a href="">Press</a>
            <a href="">Investor relations</a>
            <a href="">Mobile app- searching on the go</a>
            <a href="">Hapdays business Studio</a>
          </div>
        </div>
        <div class=" w-full md:w-1/4 flex flex-col gap-4">
          <h1 class="lg:text-xl font-semibold md:text-lg sm:text-base text-sm">Help</h1>
          <div class="flex flex-col lg:text-base md:text-base sm:text-sm text-xs">
            <a href="">Learn how hapdays works</a>
            <a href="">Terms and conditions</a>
            <a href="">Legal information</a>
            <a href="">Do not sell my personal information</a>
            <a href="">Privacy notice</a>
            <a href="">Cyber security</a>
          </div>
        </div>
        <div class=" w-full md:w-1/4 flex justify-end ">
          <div class="flex flex-row gap-4">
            <img class="md:w-8 md:h-8 w-4 h-4" src="/public/icon//twiter.svg" alt="icon">
            <img class="md:w-8 md:h-8 w-4 h-4" src="/public/icon/facebook-icon.svg" alt="icon">
            <img class="md:w-8 md:h-8 w-4 h-4" src="/public/icon/linkedin-icon.svg" alt="icon">
            <img class="md:h-8 md:w-8 w-4 h-4" src="/public/png-icons/instagram-icon.png" alt="icon">
          </div>
        </div>
      </div>
      <div class="flex flex-row gap-6 font-noto font-medium text-Gray-6 lg:text-lg md:text-base sm:text-sm text-[10px]">
        <a href="">© 2024 Hapdays , inc.</a>
        <a href="">Privacy</a>
        <a href="">Terms</a>
        <a href="">Company details</a>
        <a href="">Sitemap</a>
      </div>
    </footer>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cardDesign: [
        {
          imgUrl: '/papular-plans/india.jpg',
          contry: 'India',
          packages: '90 Package',
        },
        {
          imgUrl: '/papular-plans/america.jpg',
          contry: 'America',
          packages: '45 Package',
        },
        {
          imgUrl: '/papular-plans/Dubai.jpg',
          contry: 'Dubai',
          packages: '25 Package',
        },
        {
          imgUrl: '/papular-plans/africa.jpg',
          contry: 'Africa',
          packages: '124 Package',
        },
        {
          imgUrl: '/papular-plans/africa.jpg',
          contry: 'Africa',
          packages: '124 Package',
        },
      ],
      cardDesign1: [
        {
          imgUrl: '/papular-plans/london.jpg',
          contry: 'London',
          packages: '12 Days',
        },
        {
          imgUrl: '/papular-plans/japan.jpg',
          contry: 'Japan',
          packages: '1 Week',
        },
        {
          imgUrl: '/papular-plans/hanoi.jpg',
          contry: 'Hanoi',
          packages: '17 Days',
        },
        {
          imgUrl: '/papular-plans/bali.jpg',
          contry: 'Bali',
          packages: '1 Month',
        },
        {
          imgUrl: '/papular-plans/bali.jpg',
          contry: 'Bali',
          packages: '1 Month',
        },
      ],
    };
  },
};
</script>