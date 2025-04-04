<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value
}

const handleMenuClick = () => {
  isMenuOpen.value = false // Close menu when clicking an item
}

</script>

<template>
  <div>
    <!-- nav bar -->
    <div
    class="fixed top-0 left-0 right-0 bg-[#EEEEEE] z-50 border-b-2 border-border-color padding py-6  flex items-center justify-between"
  >
    <!-- Logo -->
    <div class="w-[80px]">
      <a href="#">
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6628074b71d6e1e95593d310_Logo.svg"
          alt="logo"
        />
      </a>
    </div>

    <!-- Desktop Menu -->
    <div class="lg:flex hidden items-center gap-6">
      <ul class="flex items-center gap-6 text-lg font-medium">
        <li><a href="#process">Process</a></li>
        <li><a href="#integrations">Integrations</a></li>
        <li><a href="#pricing">Pricing</a></li>
        <li><a href="#faq">FAQ</a></li>
        <li><a href="#reviews">Reviews</a></li>
      </ul>
      <button class="btn lg:flex hidden">Buy Template</button>
    </div>

    <!-- Hamburger / Close Icon -->
    <button @click="toggleMenu" class="lg:hidden block">
      <svg
        v-if="!isMenuOpen"
        xmlns="http://www.w3.org/2000/svg"
        width="30"
        height="30"
        viewBox="0 0 24 24"
      >
        <path
          fill="currentColor"
          d="M4 18q-.425 0-.712-.288T3 17t.288-.712T4 16h16q.425 0 .713.288T21 17t-.288.713T20 18zm0-5q-.425 0-.712-.288T3 12t.288-.712T4 11h16q.425 0 .713.288T21 12t-.288.713T20 13zm0-5q-.425 0-.712-.288T3 7t.288-.712T4 6h16q.425 0 .713.288T21 7t-.288.713T20 8z"
        />
      </svg>
      <svg
        v-else
        xmlns="http://www.w3.org/2000/svg"
        width="30"
        height="30"
        viewBox="0 0 24 24"
      >
        <path
          fill="currentColor"
          d="M18.3 5.71a1 1 0 0 0-1.41 0L12 10.59 7.11 5.7a1 1 0 1 0-1.41 1.41L10.59 12l-4.89 4.89a1 1 0 1 0 1.41 1.41L12 13.41l4.89 4.89a1 1 0 0 0 1.41-1.41L13.41 12l4.89-4.89a1 1 0 0 0 0-1.4z"
        />
      </svg>
    </button>
  </div>

  <!-- Mobile Menu -->
  <div
    v-if="isMenuOpen"
     class="lg:hidden z-50 fixed bg-[#202831] w-full md:h-auto sm:h-full top-[80px] left-0 right-0 shadow-lg p-6"
  >
    <ul class="flex flex-col  md:gap-6 gap-4 md:py-8 py-6 text-4xl  font-semibold text-own-primary ">
      <li><a href="#process" @click="handleMenuClick">Process</a></li>
      <li><a href="#integrations" @click="handleMenuClick">Integrations</a></li>
      <li><a href="#pricing" @click="handleMenuClick">Pricing</a></li>
      <li><a href="#faq" @click="handleMenuClick">FAQ</a></li>
      <li><a href="#reviews" @click="handleMenuClick">Reviews</a></li>
    </ul>
    <!--divider-->
    <div class="border-t-2 border-[#464D54] md:my-6 my-4"></div>
    <button class="outline-btn mt-4 bg-white">Learn More</button>
  </div>

    <!-- Startups section -->
    <div
      id="#"
      class="flex padding md:gap-0 gap-8 md:flex-row flex-col hero-bg-image pb-20 lg:items-end items-start bg-no-repeat mt-[150px] md:bg-[url(https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/665b169cd354209f30160ac5_Square-Shapes.svg)]"
    >
      <div class="md:w-[50%] w-full">
        <div class="xl:w-[70%] w-full flex flex-col gap-4">
          <h1 class="lg:text-6xl text-5xl leading-[1.1] font-bold">
            Landing Page Template for
            <span class="text-own-primary">Startups</span>
          </h1>
          <p>
            Use our template to quickly and efficiently brand your growing
            business.
          </p>
          <div class="flex md:flex-row flex-col items-center flex-grow gap-3">
            <button
              class="btn !px-8 md:basis-auto shrink-0 md:w-auto w-full !py-4"
            >
              Preview Template
            </button>
            <button
              class="outline-btn !px-8 md:basis-auto shrink-0 md:w-auto w-full !py-4"
            >
              Learn More
            </button>
          </div>
        </div>
      </div>
      <div class="md:w-[50%] w-full">
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/662a5c31b674b313da821db0_Hero-Illustration.svg"
          alt="section"
        />
      </div>
    </div>

    <!-- Companies section -->
    <div class="padding">
      <h1 class="text-lg font-semibold lg:text-center text-left">
        More than <span class="text-own-primary">1000+</span> Companies using
        our template
      </h1>
      <div
        class="grid md:grid-cols-6 grid-cols-2 gap-10 items-center justify-items-center mt-6"
      >
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6665ab9ed663c4f53ebba1e8_DotSquare-Logo.svg"
          alt="test"
        />
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6665abbcfc4dca184183e738_Wiggle-Logo.svg"
          alt="test"
        />
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6665abe3bb1cc3289b9bfd5a_Sealife-Logo.svg"
          alt="test"
        />
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6665ac001434b3a48f948b84_LoopMedia-Logo.svg"
          alt="test"
        />
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6665ac172b9167ca66cce90e_Tricole45-Logo.svg"
          alt="test"
        />
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6665ac32bb1cc3289b9c29a4_PlutoDelux-Logo.svg"
          alt="test"
        />
      </div>
    </div>

    <!-- Illustrations section -->
    <div class="padding mt-[150px]">
      <h1 class="section-heading">Including Custom-made Illustrations</h1>
      <p class="section-description">
        Our unique illustrations will allow you to explain concepts relevant to
        SaaS industry in an engaging and fun way.
      </p>
      <div class="grid md:grid-cols-3 grid-cols-1 gap-5 mt-10">
        <div
          class="border-[3px] card-hover flex flex-col gap-3 border-border-color rounded-2xl p-8"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="42"
            height="42"
            viewBox="0 0 32 32"
          >
            <!-- Icon from All by undefined - undefined -->
            <path fill="currentColor" d="M30 24h-4v-4h-2v4h-4v2h4v4h2v-4h4z" />
            <path
              fill="currentColor"
              d="M16 28H8V4h8v6a2.006 2.006 0 0 0 2 2h6v4h2v-6a.91.91 0 0 0-.3-.7l-7-7A.9.9 0 0 0 18 2H8a2.006 2.006 0 0 0-2 2v24a2.006 2.006 0 0 0 2 2h8Zm2-23.6l5.6 5.6H18Z"
            />
          </svg>

          <p class="text-2xl font-bold">Easy Setup</p>
          <p>Get going in days not months with our template.</p>
        </div>
        <div
          class="border-[3px] card-hover flex flex-col gap-3 border-border-color rounded-2xl p-8"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="42"
            height="42"
            viewBox="0 0 24 24"
          >
            <!-- Icon from All by undefined - undefined -->
            <g
              fill="none"
              stroke="currentColor"
              stroke-linecap="round"
              stroke-width="1.5"
            >
              <path
                d="M12 17v1m0-12v1m3 2.5C15 8.12 13.657 7 12 7S9 8.12 9 9.5s1.343 2.5 3 2.5s3 1.12 3 2.5s-1.343 2.5-3 2.5s-3-1.12-3-2.5"
              />
              <path
                d="M7 3.338A9.95 9.95 0 0 1 12 2c5.523 0 10 4.477 10 10s-4.477 10-10 10S2 17.523 2 12c0-1.821.487-3.53 1.338-5"
              />
            </g>
          </svg>
          <p class="text-2xl font-bold">Flexible Pricing</p>
          <p>Find the right pricing plan for your custom needs.</p>
        </div>
        <div
          class="border-[3px] card-hover flex flex-col gap-3 border-border-color rounded-2xl p-8"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="42"
            height="42"
            viewBox="0 0 24 24"
          >
            <!-- Icon from All by undefined - undefined -->
            <path
              fill="currentColor"
              d="M12 20.962q-3.014-.895-5.007-3.651T5 11.1V5.692l7-2.615l7 2.615V11.1q0 3.454-1.993 6.21T12 20.963m0-1.062q2.6-.825 4.3-3.3t1.7-5.5V6.375l-6-2.23l-6 2.23V11.1q0 3.025 1.7 5.5t4.3 3.3m-1.961-4.246h3.922q.344 0 .576-.232t.232-.576v-2.923q0-.343-.232-.575t-.576-.232h-.173v-1q0-.749-.51-1.26q-.51-.51-1.259-.51t-1.259.51t-.51 1.26v1h-.212q-.343 0-.575.232t-.232.575v2.923q0 .344.232.576t.576.232m.98-4.538v-1q0-.425.288-.713t.712-.288t.713.288t.287.713v1z"
            />
          </svg>
          <p class="text-2xl font-bold">Secure Solution</p>
          <p>Highest security standards will provide a peace of mind.</p>
        </div>
      </div>
    </div>

    <!-- How it works section -->
    <div id="process" class="padding mt-[150px]">
      <h1 class="section-heading">How it works</h1>
      <p class="section-description">
        Learn how we pinpoint issues in your product and get you to the finish
        line in no time.
      </p>
      <div class="grid md:grid-cols-3 grid-cols-1 md:gap-6 gap-24 mt-16">
        <div class="flex flex-col justify-between">
          <img
            class="md:w-[90%] w-[80%] mx-auto"
            src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6639f2ebe218fd42ecde7eea_discover-problem.svg"
            alt="test"
          />
          <div>
            <div class="px-2 py-1 rounded-md bg-black text-white w-max mt-10">
              Step 1
            </div>
            <h1 class="text-3xl mt-3 mb-4 text-own-primary font-semibold">
              Discover the Problem
            </h1>
            <p>
              Standing out from the competition is crucial for any Startups
              success. Pinpointing core issues in your business marketing and
              sales processes is vital for long-lasting brands.
            </p>
            <button class="outline-btn mt-5">Learn More</button>
          </div>
        </div>

        <div class="flex flex-col justify-between">
          <img
            class="md:w-[90%] w-[80%] mx-auto"
            src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6639f2c4e4e2a85572fbddf2_use-tool.svg"
            alt="test"
          />
          <div>
            <div class="px-2 py-1 rounded-md bg-black text-white w-max mt-10">
              Step 2
            </div>
            <h1 class="text-3xl mt-3 mb-4 text-own-primary font-semibold">
              Use the Template
            </h1>
            <p>
              Duo Web flow template is made in modern and bold style, and
              optimised for responsive devices. It's flexible to use and
              includes a style guide that allows for consistent brand image.
            </p>
            <button class="outline-btn mt-5">Learn More</button>
          </div>
        </div>

        <div class="flex flex-col justify-between">
          <img
            class="md:w-[90%] w-[80%] mx-auto"
            src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6639f5633925057c8fcbaf99_enjoy-results.svg"
            alt="test"
          />
          <div>
            <div class="px-2 py-1 rounded-md bg-black text-white w-max mt-10">
              Step 3
            </div>
            <h1 class="text-3xl mt-3 mb-4 text-own-primary font-semibold">
              Enjoy results
            </h1>
            <p>
              With our Startup Landing Page Template you will be able to see
              your sales sky rocket. Get noticed with your audience and create
              an everlasting brand image that lasts.
            </p>
            <button class="outline-btn mt-5">Learn More</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Integrations section -->
    <div id="integrations" class="padding mt-[150px]">
      <h1 class="section-heading">Integrations</h1>
      <p class="section-description">
        The integrations section showcases how our software seamlessly connects
        with other tools, enhancing functionality and streamlining workflows for
        maximum efficiency.
      </p>
      <button class="btn mt-4">Request a Demo</button>

      <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-8 mt-16">
        <div
          class="border-[3px] card-hover border-border-color rounded-xl relative"
        >
          <div class="p-8">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663ce3ad150cd4ef7c4a1b34_SynthoSphere-logo.svg"
              alt="test"
            />
            <p class="mt-3 pb-32">
              Elevate your business with our cloud-based solutions for seamless
              collaboration.
            </p>
          </div>
          <div
            class="bg-black p-8 mt-6 rounded-bl-xl rounded-br-xl absolute bottom-0 w-full"
          >
            <button class="btn">Connect Integration</button>
          </div>
        </div>

        <div
          class="border-[3px] card-hover border-border-color rounded-xl relative"
        >
          <div class="p-8">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663c9e10f72e7f086d44abf4_Streamline-logo.svg"
              alt="test"
            />
            <p class="mt-3 pb-32">
              Harness the power of data with our cutting-edge tools for analysis
              and insight generation.
            </p>
          </div>
          <div
            class="bg-black p-8 mt-6 rounded-bl-xl rounded-br-xl absolute bottom-0 w-full"
          >
            <button class="btn">Connect Integration</button>
          </div>
        </div>

        <div
          class="border-[3px] card-hover border-border-color rounded-xl relative"
        >
          <div class="p-8">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663ce3d9adb4b12431ea60d6_PolarStarHQ-logo.svg"
              alt="test"
            />
            <p class="mt-3 pb-32">
              Optimize your operations effortlessly with our intelligent
              workflow management platform.
            </p>
          </div>
          <div
            class="bg-black p-8 mt-6 rounded-bl-xl rounded-br-xl absolute bottom-0 w-full"
          >
            <button class="btn">Connect Integration</button>
          </div>
        </div>

        <div
          class="border-[3px] card-hover border-border-color rounded-xl relative"
        >
          <div class="p-8">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663c9e0a2867460c73781e9e_Nexus-Wave.svg"
              alt="test"
            />
            <p class="mt-3 pb-32">
              Stay in sync with real-time updates and insights for agile
              decision-making on the go.
            </p>
          </div>
          <div
            class="bg-black p-8 mt-6 rounded-bl-xl rounded-br-xl absolute bottom-0 w-full"
          >
            <button class="btn">Connect Integration</button>
          </div>
        </div>

        <div
          class="border-[3px] card-hover border-border-color rounded-xl relative"
        >
          <div class="p-8">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663ce411afd8c3befbd35c32_Cloudbloom-logo.svg"
              alt="test"
            />
            <p class="mt-3 pb-32">
              Transform raw data into actionable intelligence with our advanced
              synthesis technology.
            </p>
          </div>
          <div
            class="bg-black p-8 mt-6 rounded-bl-xl rounded-br-xl absolute bottom-0 w-full"
          >
            <button class="btn">Connect Integration</button>
          </div>
        </div>

        <div
          class="border-[3px] card-hover border-border-color rounded-xl relative"
        >
          <div class="p-8">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663ce3f9f342d2fe79c01387_Soucer-pass-logo.svg"
              alt="test"
            />
            <p class="mt-3 pb-32">
              Simplify complex processes and boost productivity with our
              intuitive automation software.
            </p>
          </div>
          <div
            class="bg-black p-8 mt-6 rounded-bl-xl rounded-br-xl absolute bottom-0 w-full"
          >
            <button class="btn">Connect Integration</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Template sample section -->
    <div class="padding md:flex-row flex-col items-center flex mt-[150px]">
      <div class="md:w-[50%] w-full">
        <h1 class="section-heading xl:w-[70%] w-[90%]">
          Accelerate your business growth with Duo Template
        </h1>
        <div
          class="xl:w-[60%] lg:w-[90%] w-full border-[3px] card-hover border-border-color rounded-xl p-8 mt-10"
        >
          <div class="flex items-center gap-3">
            <img
              class="w-[15px]"
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
              alt="test"
            />
            <p class="text-lg font-semibold">Create a memorable brand</p>
          </div>
          <p class="mt-2 mb-4">
            Stand out from the competition and get your target audiences
            attention with using Duo template.
          </p>
          <button class="outline-btn">Learn More</button>
        </div>

        <div
          class="xl:w-[60%] lg:w-[90%] w-full border-[3px] card-hover border-border-color rounded-xl p-8 mt-10"
        >
          <div class="flex items-center gap-3">
            <img
              class="w-[15px]"
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
              alt="test"
            />
            <p class="text-lg font-semibold">Launch Quickly</p>
          </div>
          <p class="mt-2 mb-4">
            Duo template allows you to launch your website fast. Whether you're
            building a landing page, a SaaS website, or a product MVP.
          </p>
          <button class="outline-btn">Learn More</button>
        </div>
      </div>
      <div class="md:w-[50%] w-full">
        <img
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663a2d0080227473fe678ddd_growth-duo.svg"
          alt="test"
        />
      </div>
    </div>

    <!-- Pricing plan section -->
    <div id="pricing" class="padding mt-[150px]">
      <h1 class="md:text-4xl text-3xl font-bold text-center">
        Choose the right Pricing Plan
      </h1>
      <p class="lg:w-[50%] md:w-[80%] w-full text-center mx-auto mt-3">
        Our pricing plans cater to diverse needs, offering flexible options to
        suit your budget and requirements.
      </p>
      <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-7 mt-14">
        <div
          class="border-[3px] border-transparent hover:border-own-primary transition-all rounded-xl bg-white p-8"
        >
          <img
            class="w-[80px]"
            src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/665af86f80a2c9f285836fc8_personal-plan-icon_1.svg"
            alt="test"
          />
          <p class="text-2xl font-medium mt-2">Personal</p>
          <p class="mt-2">
            Our Personal Plan offers essential features at an affordable price,
            without breaking the bank.
          </p>
          <p class="text-4xl font-bold mt-10 text-own-primary">$ 35.00</p>
          <p class="text-sm text-gray-600">/ Per Single License</p>
          <div class="mt-10 flex flex-col gap-3">
            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Basic Template Customization</p>
            </div>

            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Limited CMS Collections</p>
            </div>

            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Standard Hosting</p>
            </div>
          </div>
          <button class="outline-btn mt-10 !px-8 !py-4 md:w-auto w-full">
            Get Started
          </button>
        </div>

        <div
          class="border-[3px] border-transparent hover:border-own-primary transition-all rounded-xl bg-black text-white p-8"
        >
          <img
            class="w-[80px]"
            src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/665af904a98ef7d8d2a5ad7a_commercial-plan-icon_1.svg"
            alt="test"
          />
          <p class="text-2xl font-medium mt-2">Commercial</p>
          <p class="mt-2">
            Designed for small to medium-sized businesses, our Commercial Plan
            provides advanced tool.
          </p>
          <p class="text-4xl font-bold mt-10 text-own-primary">$ 55.00</p>
          <p class="text-sm text-white">/ Per Single License</p>
          <div class="mt-10 flex flex-col gap-3">
            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Full Template Customization</p>
            </div>

            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Expanded CMS Collections</p>
            </div>

            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Priority Support</p>
            </div>
          </div>
          <button class="btn mt-10 !px-8 !py-4 md:w-auto w-full">
            Get Started
          </button>
        </div>

        <div
          class="border-[3px] border-transparent hover:border-own-primary transition-all rounded-xl bg-white p-8"
        >
          <img
            class="w-[80px]"
            src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/665affecb78fada17882908a_extended-plan-icon.svg"
            alt="test"
          />
          <p class="text-2xl font-medium mt-2">Extended</p>
          <p class="mt-2">
            Tailored for large enterprises and organizations, our Extended Plan
            offers Enterprise solutions.
          </p>
          <p class="text-4xl font-bold mt-10 text-own-primary">$ 95.00</p>
          <p class="text-sm text-gray-600">/ Per Single License</p>
          <div class="mt-10 flex flex-col gap-3">
            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Enterprise Hosting Features</p>
            </div>

            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Unlimited CMS Collections</p>
            </div>

            <div class="flex items-center gap-2">
              <img
                class="w-[15px]"
                src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/663dd75610a305959e91ccb0_checkmark.svg"
                alt="test"
              />
              <p>Dedicated Support Manager</p>
            </div>
          </div>
          <button class="outline-btn mt-10 !px-8 !py-4 md:w-auto w-full">
            Get Started
          </button>
        </div>
      </div>
    </div>

    <!-- Frequently ask questions section -->
    <div id="faq" class="padding flex lg:flex-row flex-col mt-[150px] gap-10">
      <div class="xl:w-[50%] lg:w-[30%] md:w-[90%] w-full">
        <h1 class="xl:text-5xl text-4xl font-semibold">
          Frequently Asked Questions
        </h1>
        <img
          class="xl:w-[80%] w-full mt-10"
          src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/665aeb5025ec995f44e6c5fd_faq-section-illustration.svg"
          alt="test"
        />
      </div>
      <div class="xl:w-[50%] lg:w-[70%] md:w-[90%] w-full flex flex-col gap-6">
        <div
          class="bg-black flex items-center gap-8 px-8 py-4 rounded-2xl justify-between text-white"
        >
          <p class="text-xl font-bold">Is Webflow SEO-friendly?</p>
          <div class="w-[30px] shrink-0">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/664f58fe42043c5d4d79a1aa_Faq%20Open%20Icon.svg"
              alt="test"
            />
          </div>
        </div>
        <div
          class="bg-black flex items-center gap-8 px-8 py-4 rounded-2xl justify-between text-white"
        >
          <p class="text-xl font-bold">
            How can I ensure my site looks good on all devices?
          </p>
          <div class="w-[30px] shrink-0">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/664f58fe42043c5d4d79a1aa_Faq%20Open%20Icon.svg"
              alt="test"
            />
          </div>
        </div>
        <div
          class="bg-black flex items-center gap-8 px-8 py-4 rounded-2xl justify-between text-white"
        >
          <p class="text-xl font-bold">
            What if I need to add more pages to the template?
          </p>
          <div class="w-[30px] shrink-0">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/664f58fe42043c5d4d79a1aa_Faq%20Open%20Icon.svg"
              alt="test"
            />
          </div>
        </div>
        <div
          class="bg-black flex items-center gap-8 px-8 py-4 rounded-2xl justify-between text-white"
        >
          <p class="text-xl font-bold">
            How do I edit the content in a Webflow template?
          </p>
          <div class="w-[30px] shrink-0">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/664f58fe42043c5d4d79a1aa_Faq%20Open%20Icon.svg"
              alt="test"
            />
          </div>
        </div>
        <div
          class="bg-black flex items-center gap-8 px-8 py-4 rounded-2xl justify-between text-white"
        >
          <p class="text-xl font-bold">
            Can I customize the Webflow template to fit my brand?
          </p>
          <div class="w-[30px] shrink-0">
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/664f58fe42043c5d4d79a1aa_Faq%20Open%20Icon.svg"
              alt="test"
            />
          </div>
        </div>
      </div>
    </div>

    <!-- Customer reviews section -->
    <div id="reviews" class="padding bg-[#222831] mt-14 pt-[100px] pb-[200px]">
      <h1 class="text-white text-4xl font-bold text-center">
        Customer <span class="text-own-primary">Reviews</span>
      </h1>
      <div class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 gap-8 mt-14">
        <div
          class="border-[3px] border-black/20 text-white rounded-3xl card-hover p-8"
        >
          <p class="text-2xl font-medium">
            "I couldn't be happier with this Webflow template! As a small
            business owner with limited coding skills, I needed something that
            was easy to use but still looked professional - and it delivered."
          </p>
          <div
            class="w-[80px] h-[80px] rounded-full border-[3px] mt-5 border-own-primary"
          >
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6655ff5434a9a1d841b12c9b_avatar-1.webp"
              alt="test"
            />
          </div>
          <p class="text-2xl mt-4 text-own-primary">John Doe</p>
          <p class="text-sm">CEO / Flerp Studios</p>
        </div>
        <div
          class="border-[3px] border-black/20 text-white rounded-3xl card-hover p-8"
        >
          <p class="text-2xl font-medium">
            "This Webflow template has been a game-changer for my portfolio
            site. As a freelance designer, I needed a website that showcased my
            work beautifully and could be easily updated."
          </p>
          <div
            class="w-[80px] h-[80px] rounded-full border-[3px] mt-5 border-own-primary"
          >
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6655ff57a8c8e95a310bc29b_avatar-2.webp"
              alt="test"
            />
          </div>
          <p class="text-2xl mt-4 text-own-primary">Emma Frost</p>
          <p class="text-sm">Freelance Designer</p>
        </div>
        <div
          class="border-[3px] border-black/20 text-white rounded-3xl card-hover p-8"
        >
          <p class="text-2xl font-medium">
            "I was initially hesitant to use a template, but this Webflow
            template exceeded my expectations. The level of customization
            available is impressive, and the template was easy to work with."
          </p>
          <div
            class="w-[80px] h-[80px] rounded-full border-[3px] mt-5 border-own-primary"
          >
            <img
              src="https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6655ff5b17668f713e14de89_avatar-3.webp"
              alt="test"
            />
          </div>
          <p class="text-2xl mt-4 text-own-primary">Brian Choe</p>
          <p class="text-sm">Creative Director / Trix Agency</p>
        </div>
      </div>
    </div>

    <!-- Rebrand business section -->
    <div class="padding">
      <div
        style="background-position: 50%"
        class="bg-own-primary translate-y-[-50px] rounded-3xl md:px-0 px-8 flex flex-col items-center py-20 relative bg-auto bg-no-repeat bg-[url(https://cdn.prod.website-files.com/6627e9a3eba2a9009dbdeffe/6659dee649696d0bb3e27c7a_Background%20Shapes.svg)]"
      >
        <h1 class="lg:text-4xl text-3xl text-center font-semibold">
          Rebrand your business using Duo template
        </h1>
        <p class="text-white mt-7 xl:w-[50%] md:w-[70%] w- text-center">
          Our template will get your business from 0 to hero in no time. Grab
          your users attention and convert those visitors in paying customers.
        </p>
        <div class="flex items-center gap-3 mt-5 md:flex-row flex-col">
          <button class="btn !bg-black !px-8 !py-4">Preview Template</button>
          <button
            class="btn !bg-white !px-8 !py-4 !text-own-primary md:basis-auto shrink-0 md:w-auto w-full"
          >
            Learn More
          </button>
        </div>
      </div>
    </div>

    <!-- Footer section -->
    <div class="padding mt-[100px] pb-[100px]">
      <div class="grid lg:grid-cols-5 md:grid-cols-4 grid-cols-2 gap-7">
        <div>
          <p>© Duo Template</p>
          <p>Crafted by <span class="underline">Toms Design</span></p>
          <p>Powered by <span class="underline">Webflow</span></p>
        </div>
        <div>
          <h1 class="font-bold text-lg">Pages</h1>
          <ul class="mt-3 flex flex-col gap-3">
            <li>Style Guide</li>
            <li>Licensing</li>
            <li>Change Log</li>
            <li>Password</li>
            <li>404</li>
          </ul>
        </div>
        <div>
          <h1 class="font-bold text-lg">Social</h1>
          <ul class="mt-3 flex flex-col gap-3">
            <li>Instagram</li>
            <li>Facebook</li>
            <li>X</li>
            <li>Youtube</li>
            <li>Linkedin</li>
          </ul>
        </div>
        <div>
          <h1 class="font-bold text-lg">Contact</h1>
          <ul class="mt-3 flex flex-col gap-3">
            <li>Email me</li>
            <li>+959 969 253 847</li>
          </ul>
        </div>
        <div>
          <h1 class="font-bold text-lg">Pages</h1>
          <ul class="mt-3 flex flex-col gap-3">
            <li>Home</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
