<template>
<div class="min-h-screen bg-[#120725]">
    <!-- Header Navigation - Sticky -->
    <header class="w-full px-6 py-4 bg-[#120725]/95 backdrop-blur-sm border-b border-white/10 sticky top-0 z-50 transition-all duration-300">
      <nav class="flex items-center justify-between max-w-7xl mx-auto">
        <!-- Left side - Logo -->
        <div class="flex items-center">
          <h1 class="text-2xl font-bold text-white">Zeety<span class="text-[#8145E7]">.</span></h1>
        </div>
        
        <!-- Desktop Navigation -->
        <div class="hidden md:flex items-center space-x-6">
          <a href="#examples" class="px-4 py-2 text-white font-medium hover:bg-[#AC1EFF] hover:rounded-full transition-all duration-300">Examples</a>
          <a href="#reviews" class="px-4 py-2 text-white font-medium hover:bg-[#AC1EFF] hover:rounded-full transition-all duration-300">Reviews</a>
          <a href="#features" class="px-4 py-2 text-white font-medium hover:bg-[#AC1EFF] hover:rounded-full transition-all duration-300">Features</a>
          <a href="#faqs" class="px-4 py-2 text-white font-medium hover:bg-[#AC1EFF] hover:rounded-full transition-all duration-300">FAQs</a>
          <button class="px-6 py-2 bg-white text-black font-medium rounded-full border-2 border-white relative overflow-hidden transition-all duration-300 hover:border-[#AC1EFF] before:content-[''] before:absolute before:top-0 before:-left-full before:w-full before:h-full before:border-2 before:border-[#AC1EFF] before:rounded-full before:transition-all before:duration-300 before:-z-10 hover:before:left-0">
            Login
          </button>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button 
            @click="toggleMobileMenu"
            class="relative w-10 h-10 flex flex-col items-center justify-center space-y-1.5 focus:outline-none group"
            :class="{ 'open': isMobileMenuOpen }"
          >
            <!-- Hamburger Lines with Animation -->
            <span 
              class="w-6 h-0.5 bg-white transition-all duration-300 transform origin-center"
              :class="isMobileMenuOpen ? 'rotate-45 translate-y-2' : ''"
            ></span>
            <span 
              class="w-6 h-0.5 bg-white transition-all duration-300"
              :class="isMobileMenuOpen ? 'opacity-0 scale-0' : 'opacity-100 scale-100'"
            ></span>
            <span 
              class="w-6 h-0.5 bg-white transition-all duration-300 transform origin-center"
              :class="isMobileMenuOpen ? '-rotate-45 -translate-y-2' : ''"
            ></span>
          </button>
        </div>
      </nav>

      <!-- Mobile Menu Dropdown -->
      <div 
        class="md:hidden overflow-hidden transition-all duration-500 ease-in-out"
        :class="isMobileMenuOpen ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
      >
        <div class="pt-4 pb-6 space-y-2">
          <!-- Mobile Navigation Links -->
          <a 
            href="#examples" 
            @click="closeMobileMenu"
            class="block px-4 py-3 text-white font-medium hover:bg-[#AC1EFF]/20 rounded-lg transition-all duration-300 transform hover:translate-x-2"
          >
            Examples
          </a>
          <a 
            href="#reviews" 
            @click="closeMobileMenu"
            class="block px-4 py-3 text-white font-medium hover:bg-[#AC1EFF]/20 rounded-lg transition-all duration-300 transform hover:translate-x-2"
          >
            Reviews
          </a>
          <a 
            href="#features" 
            @click="closeMobileMenu"
            class="block px-4 py-3 text-white font-medium hover:bg-[#AC1EFF]/20 rounded-lg transition-all duration-300 transform hover:translate-x-2"
          >
            Features
          </a>
          <a 
            href="#faqs" 
            @click="closeMobileMenu"
            class="block px-4 py-3 text-white font-medium hover:bg-[#AC1EFF]/20 rounded-lg transition-all duration-300 transform hover:translate-x-2"
          >
            FAQs
          </a>
          <!-- Mobile Login Button -->
          <div class="pt-2">
            <button 
              @click="closeMobileMenu"
              class="w-full px-6 py-3 bg-white text-black font-medium rounded-full border-2 border-white transition-all duration-300 hover:border-[#AC1EFF] hover:bg-[#AC1EFF] hover:text-white transform hover:scale-105"
            >
              Login
            </button>
          </div>
        </div>
      </div>
    </header>

    <!-- Hero Section with Background Image -->
    <div class="relative bg-cover bg-center bg-no-repeat" style="background-image: url('/Backgrounds/topBg.png');">
      <!-- Overlay for better text readability -->
      <div class="absolute inset-0 bg-[#120725]/70"></div>
      
      <!-- Main Content -->
      <main class="relative z-10 max-w-7xl mx-auto px-6 py-12">
        <div class="text-center">
          <h2 class="text-5xl font-bold text-white mb-6">
          We'll build your small business <br>
          <span>website in 3 days. <span class="text-[#B78DFF]">For Free.</span></span>
          </h2>

          <p class="text-xl text-gray-300 mb-4 max-w-2xl mx-auto">
            Launch with no upfront cost. Only pay to keep it running, if you love it.
          </p>
          
          <!-- CTA Buttons -->
          <div class="flex items-center justify-center space-x-4">
            <button class="bg-gradient-to-r from-[#3A6FF8] to-[#AC1EFF] hover:from-[#2563eb] hover:to-[#9333ea] text-white font-bold py-4 px-8 rounded-full transition-all duration-300 transform hover:scale-105 flex items-center space-x-2">
              <span>Get Started</span>
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
              </svg>
            </button>
            
            <button class="bg-white text-black font-bold py-4 px-8 rounded-full transition-all duration-300 transform hover:scale-105 flex items-center space-x-3 border-2 border-white hover:border-[#AC1EFF] hover:shadow-[0_0_20px_rgba(172,30,255,0.5)]">
              <span>How it works</span>
              <div class="w-6 h-6 bg-black rounded-full flex items-center justify-center">
                <svg class="w-3 h-3 text-white fill-current" viewBox="0 0 24 24">
                  <path d="M8 5v14l11-7z"/>
                </svg>
              </div>
            </button>
          </div>
        </div>
        <br>
        
        <!-- Rating Section -->
        <div class="flex items-center justify-center space-x-2 mb-8">
          <span class="text-sm font-medium text-gray-300">RATED 4.8 EXCELLENT</span>
          <div class="flex space-x-1">
                  <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                    <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                      <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                    </svg>
                  </div>
                  <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                    <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                      <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                    </svg>
                  </div>
                  <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                    <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                      <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                    </svg>
                  </div>
                  <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                    <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                      <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                    </svg>
                  </div>
                  <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                    <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                      <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                    </svg>
                  </div>
                </div>
          <svg class="w-4 h-4 text-green-500 fill-current" viewBox="0 0 20 20">
            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
          </svg>
          <span class="text-sm font-medium text-gray-300">Trustpilot</span>
        </div>

         <!-- Landing Page Image -->
        <div class="flex justify-center mb-12">
          <div class="w-full max-w-4xl">
            <img 
              src="/Images/landingPage.png" 
              alt="Landing Page Preview"
              
              @error="handleImageError"
            />
          </div>
        </div>

  <!-- 3 Steps Section -->
        <div class="mt-20">
          <h3 class="text-3xl font-bold text-white text-center mb-12">
            <span>
              <span class="text-[#B78DFF]">3 Steps</span> to Get Your Business Online
            </span>
          </h3>
        <!-- Step Grid -->
  <div class="grid md:grid-cols-3 gap-8">
    <!-- Step Card -->
    <div
      v-for="(stepImage, index) in [step1Image, step2Image, step3Image]"
      :key="index"
      class="flex flex-col h-full border border-[#8145E780] rounded-2xl overflow-hidden transition-all duration-300 hover:shadow-lg"
    >
      <!-- Icon -->
      <div class="bg-gradient-to-b from-[#401E7A] to-[#8145E780] h-40 w-full">
        <img 
          :src="stepImage" 
          :alt="`Step ${index + 1}`" 
          class="w-full h-full object-cover"
          @error="handleImageError"
        />
      </div>

      <!-- Separator -->
      <div class="h-px bg-[#5F4F74] relative">
        <div class="absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2 w-12 h-12 bg-[#401E7A] border-2 border-[#8145E780] rounded-full flex items-center justify-center">
          <span class="text-white font-bold text-xl">{{ index + 1 }}</span>
        </div>
      </div>

      <!-- Content -->
      <div class="bg-[#201337] p-6 text-center flex-1 flex flex-col justify-between">
        <h4 class="text-xl font-semibold text-white mb-3">
          {{ index === 0 ? 'Complete the onboarding form' : index === 1 ? 'We build your website' : 'You review your website make request change and get it live' }}
        </h4>
        <div v-if="index !== 2" class="text-sm text-gray-300 mt-4">
          {{ index === 0 ? '5 mins' : '1-2 business days' }}
        </div>
      </div>
    </div>
  </div>
        </div>
      </main>
    </div>
<!-- Testimonial Section - Full Width -->
    <div class="mt-20 relative">
      <!-- Floating Badge positioned above the section -->
      <div class="absolute -top-16 right-8 lg:right-16 transform rotate-6 z-10">
        
        <!-- Larger Badge -->
        <div class="bg-white w-48 h-48 rounded-full border-4 border-[#00B67A] text-center shadow-2xl flex flex-col items-center justify-center text-sm px-4 text-gray-800 font-medium leading-tight">
          <div>
            Trusted by over<br>
            <br>
            <span class="bg-[#00B67A] text-white px-8 py-3 rounded font-bold text-base">10,000</span><br>
            <br>
            small business owner.
          </div>
        </div>
      </div>

      <!-- Full width testimonial background -->
      <div class="bg-gradient-to-br from-[#120725] via-[#00B67A80] to-[#05DA8E93] py-16 relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-6">
          <!-- Rating Section -->
          <div class="text-center mb-12">
            <div class="inline-flex items-center space-x-3 bg-white/10 backdrop-blur-sm rounded-full px-6 py-3 border border-white/20">
              <span class="text-sm font-medium text-white">RATED 4.8 EXCELLENT</span>
              <div class="flex space-x-1">
                <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                  <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                  </svg>
                </div>
                <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                  <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                  </svg>
                </div>
                <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                  <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                  </svg>
                </div>
                <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                  <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                  </svg>
                </div>
                <div class="w-6 h-6 rounded-full border border-white/30 flex items-center justify-center">
                  <svg class="w-3 h-3 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                  </svg>
                </div>
              </div>
              <svg class="w-4 h-4 text-[#00B67A] fill-current" viewBox="0 0 20 20">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
              </svg>
              <span class="text-sm font-medium text-white">Trustpilot</span>
            </div>
          </div>

          <!-- Testimonial Content -->
          <div class="max-w-4xl mx-auto text-center">
            <blockquote class="text-2xl md:text-3xl font-medium text-white leading-relaxed">
              "I was very dubious at first as the offer seemed too good to be true, but am very impressed with my website and the service provided"
            </blockquote>
          </div>
        </div>
      </div>
    </div>

      <!-- Comparison Section -->
<div class="mt-20 py-16 bg-[#1A0A30] rounded-3xl">
  <div class="max-w-6xl mx-auto px-6">
    <!-- Section Header -->
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
        What Makes Zeety <span class="text-[#B78DFF]">Better?</span>
      </h2>
      <p class="text-xl text-gray-300 max-w-2xl mx-auto">
        Compare Zeety with traditional methods of building websites.
      </p>
    </div>

    <!-- Comparison Items -->
    <div class="space-y-8">
      <!-- DIY Website Builders -->
      <div class="flex flex-wrap lg:flex-nowrap items-center gap-8 justify-center">
        <!-- Image Container -->
        <div class="flex-shrink-0 w-64 h-48 bg-gradient-to-br from-[#3D2A5F] to-[#2D1B4E] rounded-xl flex items-center justify-center overflow-hidden">
          <img 
            src="public/comparison_section/MaskGroup55.png" 
            alt="DIY Website Builders"
            class="w-full h-full object-cover rounded-xl"
            @error="(e) => e.target.style.display = 'none'"
          />
        </div>

        <!-- Content Box -->
        <div class="w-64 h-48 rounded-xl p-4 flex flex-col justify-center">
          <h3 class="text-base font-semibold text-white mb-2 leading-snug">Do-It-Yourself Website Builders</h3>
          <p class="text-gray-300 text-sm leading-snug">
            Easy to start, hard to finish. Prepare to sink hours into something that still won't look quite right.
          </p>
        </div>
      </div>

      <!-- Website Agencies -->
      <div class="flex flex-wrap lg:flex-nowrap items-center gap-8 justify-center lg:flex-row-reverse">
        <!-- Image Container -->
        <div class="flex-shrink-0 w-64 h-48 bg-gradient-to-br from-[#3D2A5F] to-[#2D1B4E] rounded-xl flex items-center justify-center overflow-hidden">
          <img 
            src="public/comparison_section/MaskGroup56.png" 
            alt="Website Agencies"
            class="w-full h-full object-cover rounded-xl"
            @error="(e) => e.target.style.display = 'none'"
          />
        </div>

        <!-- Content Box -->
        <div class="w-64 h-48 rounded-xl p-4 flex flex-col justify-center">
          <h3 class="text-base font-semibold text-white mb-2 leading-snug">Website Agencies</h3>
          <p class="text-gray-300 text-sm leading-snug">
            Looks great, might cost you a second mortgage, and you'll still need to learn how to maintain it.
          </p>
        </div>
      </div>

      <!-- Your cousin's mate "who does websites" -->
      <div class="flex flex-wrap lg:flex-nowrap items-center gap-8 justify-center">
        <!-- Image Container -->
        <div class="flex-shrink-0 w-64 h-48 bg-gradient-to-br from-[#3D2A5F] to-[#2D1B4E] rounded-xl flex items-center justify-center overflow-hidden">
          <img 
            src="public/comparison_section/MaskGroup57.png" 
            alt="Your cousin's mate"
            class="w-full h-full object-cover rounded-xl"
            @error="(e) => e.target.style.display = 'none'"
          />
        </div>

        <!-- Content Box -->
        <div class="w-64 h-48 rounded-xl p-4 flex flex-col justify-center">
          <h3 class="text-base font-semibold text-white mb-2 leading-snug">Your cousin's mate "who does websites"</h3>
          <p class="text-gray-300 text-sm leading-snug">
            Cheap and cheerful... until it breaks, disappears, or never gets done.
          </p>
        </div>
      </div>
    </div>
  </div>
</div>

      <!-- Comparison Table Section -->
<div id="features" class="mt-20 mx-9">
  <h3 class="text-3xl font-bold text-white text-center mb-12">Let's Compare</h3>
  
  <div class="bg-gray-900/50 rounded-2xl p-8 border border-gray-700">
    <!-- Desktop View -->
    <div class="hidden md:grid grid-cols-4 gap-4">
      <!-- Feature Column -->
      <div class="flex flex-col gap-4">
        <div class="text-white font-medium text-lg py-4">Feature</div>
        <div class="text-white font-medium py-4">Feature Name</div>
        <div class="text-white font-medium py-4">Feature Name</div>
        <div class="text-white font-medium py-4">Feature Name</div>
        <div class="text-white font-medium py-4">Feature Name</div>
        <div class="text-white font-medium py-4">Feature Name</div>
        <div class="text-white font-medium py-4">Feature Name</div>
        <div class="text-white font-medium py-4">Feature Name</div>
        <div class="text-white font-medium py-4">Feature Name</div>
      </div>

      <!-- Zeety Column -->
      <div class="flex flex-col rounded-lg text-center text-white border border-[#5F4F74] overflow-hidden">
              <!-- Solid header -->
              <div class="bg-[#5F4F74] py-4">
                <h4 class="font-bold text-xl text-white">Zeety.</h4>
              </div>
              <!-- Gradient body -->
              <div class="flex flex-col bg-gradient-to-b from-[#231045] to-[#05DA8E93] flex-1">
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
              </div>
            </div>

      <!-- DIY Builders Column -->
      <div class="flex flex-col rounded-lg text-center text-white border border-[#5F4F74] overflow-hidden">
              <!-- Solid header -->
              <div class="bg-[#5F4F74] py-4">
                <h4 class="font-bold text-xl text-white">DIY Builders</h4>
              </div>

              <!-- Gradient body -->
              <div class="flex flex-col bg-gradient-to-b from-[#231045] to-[#A855F7] flex-1">
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
              </div>
            </div>

      <!-- Agencies Column -->
      <div class="flex flex-col rounded-lg text-center text-white border border-[#5F4F74] overflow-hidden">
              <!-- Solid header -->
              <div class="bg-[#5F4F74] py-4">
                <h4 class="font-bold text-xl text-white">Agencies</h4>
              </div>

              <!-- Gradient body -->
              <div class="flex flex-col bg-gradient-to-b from-[#231045] to-[#A855F7] flex-1">
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
              </div>
            </div>
    </div>
    

    <!-- Mobile View -->
    <div id="features" class="md:hidden">
      <div class="grid grid-cols-[1fr_1fr] gap-4 relative">
        <!-- Feature Column -->
        <div class="flex flex-col gap-4">
          <div class="text-white font-medium text-lg py-4">Feature</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
          <div class="text-white font-medium py-4 text-sm">Feature Name</div>
        </div>

        <!-- Dynamic Comparison Column -->
        <div class="relative">
          <!-- Zeety Column -->
          <div 
            v-show="currentColumn === 0"
            class="flex flex-col rounded-lg text-center text-white border border-[#5F4F74] overflow-hidden transition-all duration-300"
          >
            <div class="bg-[#5F4F74] py-4">
              <h4 class="font-bold text-lg text-white">Zeety.</h4>
            </div>
            <div class="flex flex-col bg-gradient-to-b from-[#231045] to-[#05DA8E93] flex-1 py-4">
                <div class="flex-1 flex items-center justify-center py-4">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <span class="bg-teal-500 px-3 py-1 rounded-full text-sm font-medium w-fit">1-3 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
              </div>
          </div>

          <!-- DIY Builders Column -->
          <div 
            v-show="currentColumn === 1"
            class="flex flex-col rounded-lg text-center text-white border border-[#5F4F74] overflow-hidden transition-all duration-300"
          >
            <div class="bg-[#5F4F74] py-4">
              <h4 class="font-bold text-lg text-white">DIY Builders</h4>
            </div>
            <div class="flex flex-col bg-gradient-to-b from-[#231045] to-[#A855F7] flex-1">
                <div class="flex-1 flex items-center justify-center py-6">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">5 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                  </div>
                </div>
              </div>
          </div>

          <!-- Agencies Column -->
          <div 
            v-show="currentColumn === 2"
            class="flex flex-col rounded-lg text-center text-white border border-[#5F4F74] overflow-hidden transition-all duration-300"
          >
            <div class="bg-[#5F4F74] py-4">
              <h4 class="font-bold text-lg text-white">Agencies</h4>
            </div>
            <div class="flex flex-col bg-gradient-to-b from-[#231045] to-[#A855F7] flex-1">
                <div class="flex-1 flex items-center justify-center py-6">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-5">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <span class="bg-pink-500 px-3 py-1 rounded-full text-sm font-medium w-fit">10 days</span>
                </div>
                <div class="flex-1 flex items-center justify-center py-4">
                  <div class="w-8 h-8 border-2 border-white rounded-full flex items-center justify-center">
                    <svg class="w-5 h-5 stroke-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                    </svg>
                  </div>
                </div>
              </div>
          </div>

          <!-- Navigation Arrows -->
          <div class="absolute inset-y-0 -left-4 flex items-center">
            <button
              v-show="currentColumn > 0"
              @click="previousColumn"
              class="w-8 h-8 bg-[#AC1EFF] rounded-full flex items-center justify-center text-white hover:bg-[#9333ea] transition-all duration-300 transform hover:scale-110"
            >
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/>
              </svg>
            </button>
          </div>
          
          <div class="absolute inset-y-0 -right-4 flex items-center">
            <button
              v-show="currentColumn < 2"
              @click="nextColumn"
              class="w-8 h-8 bg-[#AC1EFF] rounded-full flex items-center justify-center text-white hover:bg-[#9333ea] transition-all duration-300 transform hover:scale-110"
            >
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
              </svg>
            </button>
          </div>
        </div>
      </div>

      <!-- Mobile Navigation Dots -->
      <div class="flex justify-center mt-4 space-x-2 md:hidden">
        <button
          v-for="(item, index) in ['Zeety', 'DIY Builders', 'Agencies']"
          :key="index"
          @click="currentColumn = index"
          class="w-2 h-2 rounded-full transition-all duration-300"
          :class="currentColumn === index ? 'bg-[#AC1EFF]' : 'bg-gray-600'"
        ></button>
      </div>
    </div>
  </div>
</div>


<!-- Your Free Website is waiting -->
<div class="bg-gradient-to-b from-[#120725] to-[#05DA8E93] py-20 relative overflow-hidden">
  <div class="max-w-7xl mx-auto px-6">
    <!-- Testimonial Content -->
    <div class="max-w-4xl mx-auto text-center">
      <blockquote class="text-2xl md:text-3xl font-medium text-white leading-relaxed">
        Your Free Website is Waiting
      </blockquote>
      <p class="text-white">Your website will be ready on Monday</p>
    </div>

    <!-- Centered Button -->
    <div class="flex justify-center mt-8">
      <button class="bg-white text-black font-bold py-4 px-8 rounded-full transition-all duration-300 transform hover:scale-105 flex items-center space-x-3 border-2 border-white hover:border-[#AC1EFF] hover:shadow-[0_0_20px_rgba(172,30,255,0.5)]">
        <span>Build My Website</span>
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
        </svg>
      </button>
    </div>
  </div>
</div>
<!-- Built Websites Section -->
<div id="examples" class="mt-20 py-16 bg-[#201337]">
  <div class="max-w-7xl mx-auto px-6">
    <!-- Section Header -->
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
        We've Built <span class="text-[#B78DFF]">Over 10,000</span> Websites
      </h2>
      <p class="text-xl text-gray-300 max-w-2xl mx-auto">
        New or established, local shop or online store, we're here to help your business grow.
      </p>
    </div>

    <!-- Website Gallery Grid -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-12">
      <div 
        v-for="(image, index) in websiteImages"
        :key="index"
        class="relative group cursor-pointer overflow-hidden rounded-lg border border-white/10 hover:border-[#AC1EFF]/50 transition-all duration-300 transform hover:scale-105 hover:shadow-2xl"
        @click="openLightbox(index)"
      >
        <img 
          :src="image.src" 
          :alt="image.alt"
          class="w-full h-64 object-cover transition-transform duration-300 group-hover:scale-110"
          @error="handleImageError"
        />
        <!-- Hover Overlay -->
        <div class="absolute inset-0 bg-black/50 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center">
          <div class="text-white text-center">
            <svg class="w-12 h-12 mx-auto mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0zM10 7v3m0 0v3m0-3h3m-3 0H7"/>
            </svg>
            <p class="text-sm font-medium">Click to view</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Ready for yours CTA -->
    <div class="text-center">
      <p class="text-2xl text-white mb-6">Ready for yours?</p>
      <button class="bg-gradient-to-r from-[#3A6FF8] to-[#AC1EFF] hover:from-[#2563eb] hover:to-[#9333ea] text-white font-bold py-4 px-8 rounded-full transition-all duration-300 transform hover:scale-105 flex items-center space-x-2 mx-auto">
        <span>Get Started</span>
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
        </svg>
      </button>
    </div>
  </div>
</div>

<!-- Lightbox Modal -->
<div 
  v-if="lightboxOpen"
  class="fixed inset-0 bg-black/90 z-50 flex items-center justify-center p-4"
  @click="closeLightbox"
>
  <!-- Close Button -->
  <button 
    @click="closeLightbox"
    class="absolute top-4 right-4 text-white hover:text-[#AC1EFF] transition-colors duration-200 z-10"
  >
    <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
    </svg>
  </button>

  <!-- Previous Button -->
  <button 
    @click.stop="previousImage"
    class="absolute left-4 top-1/2 transform -translate-y-1/2 text-white hover:text-[#AC1EFF] transition-colors duration-200 z-10"
    :class="{ 'opacity-50 cursor-not-allowed': currentImageIndex === 0 }"
  >
    <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/>
    </svg>
  </button>

  <!-- Next Button -->
  <button 
    @click.stop="nextImage"
    class="absolute right-4 top-1/2 transform -translate-y-1/2 text-white hover:text-[#AC1EFF] transition-colors duration-200 z-10"
    :class="{ 'opacity-50 cursor-not-allowed': currentImageIndex === websiteImages.length - 1 }"
  >
    <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
    </svg>
  </button>

  <!-- Image Container -->
  <div class="max-w-5xl max-h-full flex items-center justify-center" @click.stop>
    <img 
      :src="websiteImages[currentImageIndex].src"
      :alt="websiteImages[currentImageIndex].alt"
      class="max-w-full max-h-full object-contain rounded-lg shadow-2xl"
    />
  </div>

  <!-- Image Counter -->
  <div class="absolute bottom-4 left-1/2 transform -translate-x-1/2 text-white text-sm bg-black/50 px-3 py-1 rounded-full">
    {{ currentImageIndex + 1 }} / {{ websiteImages.length }}
  </div>
</div>

<!-- Wrapper with Gradient Background -->
<div class="bg-gradient-to-b from-[#120725] via-[#1b0b35] to-[#231045]">

<!-- Video Section -->
<div class="mt-20 py-16">
  <div class="max-w-6xl mx-auto px-6">
    <!-- Section Header -->
    <div class="text-center mb-12">
      <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
        Not Yet <span class="text-[#B78DFF]">Convinced?</span>
      </h2>
      <p class="text-lg text-gray-300 mb-8">
        Watch 2 minute explainer
      </p>
    </div>

    <!-- Video Container -->
    <div class="relative max-w-4xl mx-auto">
      <div class="relative rounded-2xl overflow-hidden bg-gradient-to-br from-[#8B5CF6] via-[#A855F7] to-[#9333EA] p-1">
        <div class="relative rounded-xl overflow-hidden bg-black">
          <!-- Video Element -->
          <video 
            ref="videoPlayer"
            class="w-full aspect-video object-cover"
            :poster="videoPoster"
            @click="togglePlay"
            preload="metadata"
          >
            <source src="/videos/placeholdervideo.mp4" type="video/mp4">
            Your browser does not support the video tag.
          </video>
          
          <!-- Custom Play Button Overlay -->
          <div 
            v-show="!isPlaying"
            @click="togglePlay"
            class="absolute inset-0 flex items-center justify-center bg-black/20 cursor-pointer group"
          >
            <div class="relative">
              <!-- Play Button Background Circle -->
              <div class="w-20 h-20 bg-white/90 backdrop-blur-sm rounded-full flex items-center justify-center shadow-2xl transform transition-all duration-300 group-hover:scale-110 group-hover:bg-white">
                <!-- Play Icon -->
                <svg 
                  class="w-8 h-8 text-black ml-1 transition-colors duration-300" 
                  fill="currentColor" 
                  viewBox="0 0 24 24"
                >
                  <path d="M8 5v14l11-7z"/>
                </svg>
              </div>
              
              <!-- Pulsing Ring Animation -->
              <div class="absolute inset-0 w-20 h-20 border-2 border-white/50 rounded-full animate-ping"></div>
            </div>
          </div>

          <!-- Video Duration Badge -->
          <!-- <div class="absolute bottom-4 right-4">
            <div class="bg-black/70 backdrop-blur-sm text-white text-sm font-medium px-3 py-1 rounded-full">
              02:17
            </div>
          </div> -->

          <!-- Video Controls (when playing) -->
          <div 
            v-show="isPlaying"
            class="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/70 to-transparent p-4 opacity-0 hover:opacity-100 transition-opacity duration-300"
          >
            <div class="flex items-center space-x-4">
              <!-- Play/Pause Button -->
              <button 
                @click="togglePlay"
                class="text-white hover:text-[#B78DFF] transition-colors duration-200"
              >
                <svg v-if="isPlaying" class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M6 4h4v16H6V4zm8 0h4v16h-4V4z"/>
                </svg>
                <svg v-else class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M8 5v14l11-7z"/>
                </svg>
              </button>
              
              <!-- Progress Bar -->
              <div class="flex-1 bg-white/20 rounded-full h-1 cursor-pointer" @click="seekVideo">
                <div 
                  class="bg-[#B78DFF] h-1 rounded-full transition-all duration-100"
                  :style="{ width: `${videoProgress}%` }"
                ></div>
              </div>
              
              <!-- Time Display -->
              <div class="text-white text-sm font-medium min-w-[80px]">
                {{ formatTime(currentTime) }} / {{ formatTime(duration) }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
<!-- Perks Section -->
<div class="py-20">
  <div class="max-w-7xl mx-auto px-6">
    <div class="grid lg:grid-cols-2 gap-16 items-center">
      <!-- Left Content -->
      <div>
        <h2 class="text-white text-3xl md:text-4xl font-normal mb-8">
          Why choose us?
        </h2>
        <h3 class="text-white text-4xl md:text-5xl font-bold leading-tight">
          Because we don't just build websites. We 
          <span class="text-[#B78DFF]">help grow</span> your business.
        </h3>
      </div>

      <!-- Right Content - Perks List -->
      <div class="space-y-8">
        <!-- Save Time & Money -->
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-12 h-12 bg-gradient-to-r from-[#3A6FF8] to-[#AC1EFF] rounded-full flex items-center justify-center">
            <svg width="30px" height="30px" viewBox="0 0 64 64" xmlns="http://www.w3.org/2000/svg" stroke-width="3" stroke="#FFFFFF" fill="none">
              <path d="M46.89,52.11H21.17a.2.2,0,0,1-.16-.33c1.76-1.89,10.17-11.52,7-20.19-3.59-9.66-1.27-25,16.08-17.87" stroke-linecap="round"/>
              <line x1="17.11" y1="31.84" x2="41.11" y2="31.84" stroke-linecap="round"/>
            </svg>
          </div>
          <div>
            <h4 class="text-white text-xl font-semibold mb-2">Save Time & Money</h4>
            <p class="text-gray-300 text-base">
              Launch faster and skip the agency price tag, without sacrificing quality.
            </p>
          </div>
        </div>

        <!-- Get Found Online -->
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-12 h-12 bg-gradient-to-r from-[#3A6FF8] to-[#AC1EFF] rounded-full flex items-center justify-center">
            <svg version="1.0" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
              width="25px" height="25px" viewBox="0 0 64 64" enable-background="new 0 0 64 64" xml:space="preserve">
            <path fill="#FFFFFF" d="M32,0C14.327,0,0,14.327,0,32s14.327,32,32,32s32-14.327,32-32S49.673,0,32,0z M49.972,31
              c-0.138-5.582-1.414-10.878-3.613-15.667c2.652-1.022,5.169-2.317,7.515-3.854c4.824,5.14,7.854,11.976,8.102,19.521H49.972z
              M33.333,61.966c-0.11,0.005-0.222,0.005-0.333,0.009V50.035c3.324,0.087,6.547,0.581,9.605,1.47
              C40.184,55.541,37.029,59.084,33.333,61.966z M44.549,52.141c2.283,0.801,4.462,1.817,6.523,3.018
              c-3.991,3.29-8.849,5.563-14.178,6.438C39.902,58.861,42.484,55.672,44.549,52.141z M21.394,51.505
              c3.059-0.89,6.282-1.383,9.606-1.47v11.939c-0.111-0.004-0.223-0.004-0.333-0.009C26.97,59.084,23.816,55.541,21.394,51.505z
              M27.105,61.596c-5.329-0.874-10.187-3.147-14.178-6.438c2.062-1.2,4.24-2.217,6.523-3.017
              C21.515,55.672,24.098,58.861,27.105,61.596z M2.025,31c0.248-7.545,3.277-14.381,8.102-19.521c2.346,1.536,4.862,2.831,7.515,3.854
              C15.442,20.122,14.166,25.418,14.028,31H2.025z M43.57,14.196c-3.345,1.069-6.894,1.67-10.57,1.766V2.025
              c0.111,0.004,0.223,0.004,0.333,0.009C37.541,5.314,41.047,9.453,43.57,14.196z M36.895,2.404
              c5.944,0.976,11.298,3.696,15.521,7.622c-2.176,1.391-4.496,2.57-6.944,3.499C43.278,9.326,40.369,5.562,36.895,2.404z M31,2.025
              v13.937c-3.677-0.096-7.226-0.696-10.57-1.766c2.523-4.743,6.029-8.882,10.237-12.162C30.777,2.029,30.889,2.029,31,2.025z
              M18.529,13.525c-2.448-0.929-4.769-2.108-6.944-3.499c4.223-3.926,9.576-6.646,15.521-7.622
              C23.631,5.562,20.722,9.326,18.529,13.525z M19.532,16.009c3.622,1.189,7.472,1.873,11.468,1.972V31H16.031
              C16.17,25.654,17.403,20.584,19.532,16.009z M31,33v15.036c-3.684,0.092-7.245,0.665-10.615,1.689
              C17.732,44.712,16.188,39.029,16.031,33H31z M33,48.036V33h14.969c-0.156,6.029-1.701,11.712-4.354,16.726
              C40.245,48.701,36.684,48.128,33,48.036z M33,31V17.98c3.996-0.099,7.846-0.782,11.468-1.972c2.129,4.575,3.362,9.646,3.501,14.991
              H33z M2.025,33h12.003c0.154,6.253,1.74,12.146,4.447,17.369c-2.496,0.899-4.871,2.044-7.109,3.396
              C5.827,48.513,2.294,41.172,2.025,33z M52.634,53.766c-2.238-1.353-4.613-2.497-7.109-3.396c2.707-5.224,4.293-11.116,4.447-17.369
              h12.003C61.706,41.172,58.173,48.513,52.634,53.766z"/>
            </svg>
          </div>
          <div>
            <h4 class="text-white text-xl font-semibold mb-2">Get Found Online</h4>
            <p class="text-gray-300 text-base">
              Our SEO-friendly sites help your business show up where it matters: in search results.
            </p>
          </div>
        </div>

        <!-- Make It Yours -->
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-12 h-12 bg-gradient-to-r from-[#3A6FF8] to-[#AC1EFF] rounded-full flex items-center justify-center">
            <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 5H6a2 2 0 00-2 2v11a2 2 0 002 2h11a2 2 0 002-2v-5m-1.414-9.414a2 2 0 112.828 2.828L11.828 15H9v-2.828l8.586-8.586z"/>
            </svg>
          </div>
          <div>
            <h4 class="text-white text-xl font-semibold mb-2">Make It Yours</h4>
            <p class="text-gray-300 text-base">
              Easily update content, images, and more. Your site, your way, anytime.
            </p>
          </div>
        </div>

        <!-- Support That Cares -->
        <div class="flex items-start gap-4">
          <div class="flex-shrink-0 w-12 h-12 bg-gradient-to-r from-[#3A6FF8] to-[#AC1EFF] rounded-full flex items-center justify-center">
            <svg fill="#FFFFFf" height="25px" width="25px" version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
              viewBox="0 0 512 512" xml:space="preserve">
            <g>
              <g>
                <path d="M144.34,179.427h-10.894v0c-10.876,0-20.116,7.123-23.311,16.948c-19.214,3.319-33.88,20.095-33.88,40.243v65.68
                  c0,20.149,14.666,36.925,33.88,40.244c3.195,9.824,12.435,16.947,23.311,16.947h10.894c28.619,0,51.904-23.284,51.904-51.904
                  V231.33C196.244,202.711,172.96,179.427,144.34,179.427z M179.904,307.586c0,19.61-15.954,35.563-35.563,35.563h-10.894
                  c-4.506,0-8.17-3.665-8.17-8.17v-49.18c0-4.512-3.657-8.17-8.17-8.17c-4.513,0-8.17,3.658-8.17,8.17v39.605
                  c-9.509-3.373-16.34-12.454-16.34-23.105v-65.68c0-10.651,6.831-19.733,16.34-23.105v39.604c0,4.512,3.657,8.17,8.17,8.17
                  c4.513,0,8.17-3.658,8.17-8.17v-49.18c0-4.506,3.665-8.17,8.17-8.17h10.894c19.61,0.001,35.563,15.955,35.563,35.564V307.586z"/>
              </g>
            </g>
            <g>
              <g>
                <path d="M432.146,176.547C415.192,93.185,341.111,32.681,256,32.681c-84.963,0-159.018,60.379-176.087,143.568
                  c-0.907,4.421,1.94,8.738,6.361,9.645c4.422,0.904,8.739-1.941,9.645-6.362C111.437,103.91,178.76,49.021,256,49.021
                  c77.374,0,144.722,55.002,160.134,130.782c0.788,3.873,4.194,6.544,7.998,6.544c0.539,0,1.087-0.053,1.637-0.166
                  C430.191,185.282,433.046,180.968,432.146,176.547z"/>
              </g>
            </g>
            <g>
              <g>
                <path d="M256,0C138.869,0,43.574,95.294,43.574,212.426v166.128c0,58.566,47.647,106.213,106.213,106.213h28.196
                  C181.683,500.36,195.716,512,212.426,512h87.149c19.522,0,35.404-15.883,35.404-35.404c0-19.521-15.882-35.404-35.404-35.404
                  h-87.149c-16.71,0-30.743,11.64-34.442,27.234h-28.196c-49.555,0-89.872-40.316-89.872-89.872V212.426
                  C59.915,104.304,147.879,16.34,256,16.34s196.085,87.964,196.085,196.085v57.191c0,10.651-6.831,19.733-16.34,23.105v-56.103
                  c0-20.149-14.666-36.925-33.88-40.244c-3.195-9.825-12.435-16.947-23.311-16.947H367.66c-28.619,0-51.904,23.284-51.904,51.904
                  v76.255c0,28.62,23.284,51.904,51.904,51.904h10.894c10.876,0,20.116-7.123,23.311-16.947
                  c16.779-2.899,30.081-16.062,33.183-32.771c18.967-3.522,33.378-20.182,33.378-40.154v-57.193C468.426,95.294,373.131,0,256,0z
                  M212.426,457.532h2.723v13.617c0,4.512,3.657,8.17,8.17,8.17s8.17-3.658,8.17-8.17v-13.617h68.085
                  c10.511,0,19.064,8.553,19.064,19.064s-8.553,19.064-19.064,19.064h-87.149c-10.511,0-19.064-8.553-19.064-19.064
                  S201.914,457.532,212.426,457.532z M419.404,302.298c0,10.651-6.831,19.733-16.34,23.105v-39.605c0-4.512-3.657-8.17-8.17-8.17
                  s-8.17,3.658-8.17,8.17v49.18c0,4.506-3.665,8.17-8.17,8.17H367.66c-19.61,0-35.563-15.954-35.563-35.563V231.33
                  c0-19.61,15.954-35.563,35.563-35.563h10.894c4.506,0,8.17,3.665,8.17,8.17v49.18c0,4.512,3.657,8.17,8.17,8.17
                  s8.17-3.658,8.17-8.17v-39.604c9.509,3.373,16.34,12.454,16.34,23.105V302.298z"/>
              </g>
            </g>
            </svg>
          </div>
          <div>
            <h4 class="text-white text-xl font-semibold mb-2">Support That Cares</h4>
            <p class="text-gray-300 text-base">
              Real help from real people, whenever you need it. We've got your back.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</div>

<!-- Sliding Reviews Section -->
<div id="reviews" class="relative bg-cover bg-center bg-no-repeat py-15" style="background-image: url('/Backgrounds/ReviewsBg.png');">
  <!-- Overlay for better text readability -->
  <!-- <div class="absolute inset-0 bg-[#120725]/80"></div> -->
  
  <!-- Main Content -->
  <div class="relative z-10 max-w-7xl mx-auto px-6">
    <!-- Section Header -->
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
        We're <span class="text-[#B78DFF]">Not Your Average</span> Web Agency
      </h2>
    </div>

    <!-- Reviews Container -->
    <div class="relative max-w-6xl mx-auto">
      <!-- Navigation Buttons -->
      <button 
        @click="previousReview"
        :disabled="currentReview === 0"
        class="absolute left-4 top-1/2 transform -translate-y-1/2 z-20 w-12 h-12 bg-white/10 backdrop-blur-sm border border-white/20 rounded-full flex items-center justify-center text-white hover:bg-white/20 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/>
        </svg>
      </button>

      <button 
        @click="nextReview"
        :disabled="currentReview === reviews.length - 1"
        class="absolute right-4 top-1/2 transform -translate-y-1/2 z-20 w-12 h-12 bg-white/10 backdrop-blur-sm border border-white/20 rounded-full flex items-center justify-center text-white hover:bg-white/20 transition-all duration-300 disabled:opacity-50 disabled:cursor-not-allowed"
      >
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
        </svg>
      </button>

      <!-- Reviews Slider -->
      <div class="overflow-hidden rounded-2xl">
        <div 
          class="flex transition-transform duration-500 ease-in-out"
          :style="{ transform: `translateX(-${currentReview * 100}%)` }"
        >
          <!-- Review Cards -->
          <div 
            v-for="(review, index) in reviews" 
            :key="index"
            class="w-full flex-shrink-0 px-8"
          >
            <div class="grid md:grid-cols-3 gap-8">
              <!-- Review Card Template -->
              <div 
                v-for="(card, cardIndex) in review.cards" 
                :key="cardIndex"
                class="bg-[#2A1A3E]/80 backdrop-blur-sm border border-white/10 rounded-2xl p-6 hover:border-[#AC1EFF]/30 transition-all duration-300 flex flex-col h-full"
              >
                <!-- Top Content Container -->
                <div class="flex-1">
                  <!-- Star Rating -->
                  <div class="flex items-center mb-4">
                    <div class="flex space-x-1 mr-3">
                      <div v-for="n in 5" :key="n" class="w-5 h-5 rounded-sm bg-[#00B67A] flex items-center justify-center">
                        <svg class="w-3 h-3 text-white fill-current" viewBox="0 0 20 20">
                          <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                        </svg>
                      </div>
                    </div>
                  </div>

                  <!-- Review Text -->
                  <p class="text-gray-300 leading-relaxed">
                    {{ card.text }}
                  </p>
                </div>

                <!-- User Info - Always at bottom -->
                <div class="flex items-center mt-6 pt-4 border-t border-white/10">
                  <div class="w-10 h-10 bg-gray-600 rounded-full flex items-center justify-center mr-3">
                    <svg class="w-6 h-6 text-gray-300" fill="currentColor" viewBox="0 0 20 20">
                      <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd"/>
                    </svg>
                  </div>
                  <div>
                    <h4 class="text-white font-medium">{{ card.userName }}</h4>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Dots Indicator -->
      <div class="flex justify-center mt-8 space-x-2">
        <button
          v-for="(review, index) in reviews"
          :key="index"
          @click="goToReview(index)"
          class="w-3 h-3 rounded-full transition-all duration-300"
          :class="currentReview === index ? 'bg-[#AC1EFF]' : 'bg-white/30 hover:bg-white/50'"
        ></button>
      </div>
    </div>

    <!-- Bottom Rating Section -->
    <div class="text-center mt-16">
      <div class="inline-flex items-center space-x-3 bg-white/10 backdrop-blur-sm rounded-full px-6 py-3 border border-white/20">
        <span class="text-sm font-medium text-white">RATED 4.8 EXCELLENT</span>
        <div class="flex space-x-1">
          <div v-for="n in 5" :key="n" class="w-5 h-5 rounded-sm bg-[#00B67A] flex items-center justify-center">
            <svg class="w-3 h-3 text-white fill-current" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
            </svg>
          </div>
        </div>
        <svg class="w-4 h-4 text-[#00B67A] fill-current" viewBox="0 0 20 20">
            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
        </svg>
        <span class="text-sm font-medium text-white">Trustpilot</span>
      </div>
    </div>
  </div>
</div>

<!-- FAQs Section -->
<section id="faqs" class="relative bg-cover bg-center bg-no-repeat py-20" style="background-image: url('/Backgrounds/FAQsBg.png');">
  <!-- Overlay for better text readability -->
  <div class="absolute inset-0 bg-[#120725]/70"></div>
  
  <div class="relative z-10 max-w-4xl mx-auto px-6">
    <!-- Section Header -->
    <div class="text-center mb-16">
      <h2 class="text-4xl md:text-5xl font-bold text-white mb-4">
        Frequently Asked Questions
      </h2>
    </div>

    <!-- FAQ Items -->
    <div class="space-y-4">
      <!-- FAQ Item 1 -->
      <div class="border border-white/20 rounded-lg overflow-hidden bg-white/5 backdrop-blur-sm">
        <button 
          @click="toggleFAQ(0)"
          class="w-full px-6 py-6 text-left flex items-center justify-between hover:bg-white/10 transition-all duration-300"
        >
          <span class="text-lg font-medium text-white">How do I start?</span>
          <svg 
            class="w-6 h-6 text-white transition-transform duration-300"
            :class="{ 'rotate-180': activeFAQ === 0 }"
            fill="none" 
            stroke="currentColor" 
            viewBox="0 0 24 24"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
          </svg>
        </button>
        <div 
          class="overflow-hidden transition-all duration-500 ease-in-out"
          :class="activeFAQ === 0 ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
        >
          <div class="px-6 pb-6 text-gray-300">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </div>
        </div>
      </div>

      <!-- FAQ Item 2 -->
      <div class="border border-white/20 rounded-lg overflow-hidden bg-white/5 backdrop-blur-sm">
        <button 
          @click="toggleFAQ(1)"
          class="w-full px-6 py-6 text-left flex items-center justify-between hover:bg-white/10 transition-all duration-300"
        >
          <span class="text-lg font-medium text-white">Why do you offer free website building services?</span>
          <svg 
            class="w-6 h-6 text-white transition-transform duration-300"
            :class="{ 'rotate-180': activeFAQ === 1 }"
            fill="none" 
            stroke="currentColor" 
            viewBox="0 0 24 24"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
          </svg>
        </button>
        <div 
          class="overflow-hidden transition-all duration-500 ease-in-out"
          :class="activeFAQ === 1 ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
        >
          <div class="px-6 pb-6 text-gray-300">
            Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit.
          </div>
        </div>
      </div>

      <!-- FAQ Item 3 -->
      <div class="border border-white/20 rounded-lg overflow-hidden bg-white/5 backdrop-blur-sm">
        <button 
          @click="toggleFAQ(2)"
          class="w-full px-6 py-6 text-left flex items-center justify-between hover:bg-white/10 transition-all duration-300"
        >
          <span class="text-lg font-medium text-white">Can I use your service if I already have web hosting elsewhere?</span>
          <svg 
            class="w-6 h-6 text-white transition-transform duration-300"
            :class="{ 'rotate-180': activeFAQ === 2 }"
            fill="none" 
            stroke="currentColor" 
            viewBox="0 0 24 24"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
          </svg>
        </button>
        <div 
          class="overflow-hidden transition-all duration-500 ease-in-out"
          :class="activeFAQ === 2 ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
        >
          <div class="px-6 pb-6 text-gray-300">
            Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Sed ut perspiciatis unde omnis.
          </div>
        </div>
      </div>

      <!-- FAQ Item 4 -->
      <div class="border border-white/20 rounded-lg overflow-hidden bg-white/5 backdrop-blur-sm">
        <button 
          @click="toggleFAQ(3)"
          class="w-full px-6 py-6 text-left flex items-center justify-between hover:bg-white/10 transition-all duration-300"
        >
          <span class="text-lg font-medium text-white">Do I need a domain name before signing up?</span>
          <svg 
            class="w-6 h-6 text-white transition-transform duration-300"
            :class="{ 'rotate-180': activeFAQ === 3 }"
            fill="none" 
            stroke="currentColor" 
            viewBox="0 0 24 24"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
          </svg>
        </button>
        <div 
          class="overflow-hidden transition-all duration-500 ease-in-out"
          :class="activeFAQ === 3 ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
        >
          <div class="px-6 pb-6 text-gray-300">
            Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit. Neque porro quisquam est qui dolorem ipsum quia dolor sit amet.
          </div>
        </div>
      </div>

      <!-- FAQ Item 5 -->
      <div class="border border-white/20 rounded-lg overflow-hidden bg-white/5 backdrop-blur-sm">
        <button 
          @click="toggleFAQ(4)"
          class="w-full px-6 py-6 text-left flex items-center justify-between hover:bg-white/10 transition-all duration-300"
        >
          <span class="text-lg font-medium text-white">Will my website be optimised for search engines?</span>
          <svg 
            class="w-6 h-6 text-white transition-transform duration-300"
            :class="{ 'rotate-180': activeFAQ === 4 }"
            fill="none" 
            stroke="currentColor" 
            viewBox="0 0 24 24"
          >
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/>
          </svg>
        </button>
        <div 
          class="overflow-hidden transition-all duration-500 ease-in-out"
          :class="activeFAQ === 4 ? 'max-h-96 opacity-100' : 'max-h-0 opacity-0'"
        >
          <div class="px-6 pb-6 text-gray-300">
            Consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam quis nostrud exercitation.
          </div>
        </div>
      </div>
    </div>

    <!-- Call-to-Action -->
  <div class="text-center z-10 mt-12 mb-0"> <!-- removed bottom margin -->
    <p class="text-white text-lg mb-6">Got another question? Let's chat!</p>
    <button class="bg-white text-black font-bold py-4 px-8 rounded-full transition-all duration-300 transform hover:scale-105 hover:shadow-[0_0_20px_rgba(255,255,255,0.3)]">
      Start Live Chat
    </button>
  </div>
</div>

<!-- Offer Footer Section -->
<div
  class="relative bg-no-repeat bg-right md:bg-top bg-cover md:bg-contain py-24 -mt-1 h-[300px] md:h-auto"
  style="background-image: url('/Images/ZBannerFaded.png');"
>
  <!-- Content -->
  <div class="relative z-10 max-w-7xl mx-auto px-6 flex flex-col md:flex-row items-center md:items-start md:justify-start space-y-6 md:space-y-0 md:space-x-8">
    <div class="max-w-lg text-left ml-6 md:ml-16">
      <h1 class="text-3xl md:text-4xl font-bold text-white mb-4">Get started for free</h1>
      <p class="text-base md:text-lg text-white mb-6">Build a website and get your business online in minutes</p>
      <button class="bg-white text-black font-bold py-4 px-8 rounded-full hover:scale-105 hover:shadow-[0_0_20px_rgba(255,255,255,0.3)]">
        Generate your site
      </button>
    </div>
  </div>
</div>
  
</section>

  
  
<!-- Footer -->
<footer class="mt-20 border-t border-gray-700 py-8">
  <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center">
    <!-- Left: Z. -->
    <div class="flex items-center text-5xl font-extrabold">
      <span class="text-white">Z</span><span class="text-[#8145E7]">.</span>
    </div>

    <!-- Right: Slogan and Copyright -->
    <div class="mt-6 md:mt-0 text-center md:text-right">
      <p class="text-xl font-medium text-white">Create Slogan Here</p>
      <p class="text-sm text-gray-400 mt-2">© Copyright 2025</p>
    </div>
  </div>
</footer>
  </div>
</template>

<script setup>
// Mobile comparison table state
const currentColumn = ref(0)
// Mobile comparison navigation functions
const nextColumn = () => {
  if (currentColumn.value < 2) {
    currentColumn.value++
  }
}

const previousColumn = () => {
  if (currentColumn.value > 0) {
    currentColumn.value--
  }
}
// Mobile menu state
const isMobileMenuOpen = ref(false)

// Step images
const step1Image = '/Images/step1.png'
const step2Image = '/Images/step2.png' 
const step3Image = '/Images/step3.png'

// Mobile menu functions
const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}

// Image error handler
const handleImageError = (event) => {
  console.log('Image failed to load:', event.target.src)
  event.target.style.display = 'none'
}

// Smooth scrolling for navigation links
onMounted(() => {
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault()
      const target = document.querySelector(this.getAttribute('href'))
      if (target) {
        target.scrollIntoView({
          behavior: 'smooth'
        })
      }
    })
  })
})
// Built websites data
const websiteImages = ref([
  { src: '/Images/builtWeb1.png', alt: 'Built Website Example 1' },
  { src: '/Images/builtWeb2.png', alt: 'Built Website Example 2' },
  { src: '/Images/builtWeb1.png', alt: 'Built Website Example 3' },
  { src: '/Images/builtWeb2.png', alt: 'Built Website Example 4' },
  { src: '/Images/builtWeb1.png', alt: 'Built Website Example 5' },
  { src: '/Images/builtWeb2.png', alt: 'Built Website Example 6' }
])

// Lightbox state
const lightboxOpen = ref(false)
const currentImageIndex = ref(0)

// Lightbox functions
const openLightbox = (index) => {
  currentImageIndex.value = index
  lightboxOpen.value = true
  document.body.style.overflow = 'hidden' // Prevent background scrolling
}

const closeLightbox = () => {
  lightboxOpen.value = false
  document.body.style.overflow = 'auto' // Restore scrolling
}

const nextImage = () => {
  if (currentImageIndex.value < websiteImages.value.length - 1) {
    currentImageIndex.value++
  }
}

const previousImage = () => {
  if (currentImageIndex.value > 0) {
    currentImageIndex.value--
  }
}

// Handle keyboard navigation
onMounted(() => {
  const handleKeyDown = (event) => {
    if (!lightboxOpen.value) return
    
    switch (event.key) {
      case 'ArrowRight':
        nextImage()
        break
      case 'ArrowLeft':
        previousImage()
        break
      case 'Escape':
        closeLightbox()
        break
    }
  }
  
  document.addEventListener('keydown', handleKeyDown)
  
  // Cleanup
  onUnmounted(() => {
    document.removeEventListener('keydown', handleKeyDown)
  })
})
// Video player state
const videoPlayer = ref(null)
const isPlaying = ref(false)
const currentTime = ref(0)
const duration = ref(0)
const videoProgress = ref(0)

// Video poster image (you can replace with actual poster)
const videoPoster = ref('/Images/video-poster.jpg')

// Toggle play/pause
const togglePlay = () => {
  if (!videoPlayer.value) return
  
  if (isPlaying.value) {
    videoPlayer.value.pause()
  } else {
    videoPlayer.value.play()
  }
}

// Format time in MM:SS format
const formatTime = (seconds) => {
  const mins = Math.floor(seconds / 60)
  const secs = Math.floor(seconds % 60)
  return `${mins.toString().padStart(2, '0')}:${secs.toString().padStart(2, '0')}`
}

// Seek to specific time in video
const seekVideo = (event) => {
  if (!videoPlayer.value) return
  
  const progressBar = event.currentTarget
  const rect = progressBar.getBoundingClientRect()
  const clickX = event.clientX - rect.left
  const percentage = clickX / rect.width
  const newTime = percentage * duration.value
  
  videoPlayer.value.currentTime = newTime
}

// Setup video event listeners
onMounted(() => {
  if (videoPlayer.value) {
    const video = videoPlayer.value
    
    // Play event
    video.addEventListener('play', () => {
      isPlaying.value = true
    })
    
    // Pause event
    video.addEventListener('pause', () => {
      isPlaying.value = false
    })
    
    // Time update
    video.addEventListener('timeupdate', () => {
      currentTime.value = video.currentTime
      if (duration.value > 0) {
        videoProgress.value = (video.currentTime / duration.value) * 100
      }
    })
    
    // Duration loaded
    video.addEventListener('loadedmetadata', () => {
      duration.value = video.duration
    })
    
    // Video ended
    video.addEventListener('ended', () => {
      isPlaying.value = false
      videoProgress.value = 0
      currentTime.value = 0
    })
  }
})

// Reviews data
const reviews = ref([
  {
    cards: [
      {
        text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        userName: "User Name"
      },
      {
        text: "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
        userName: "User Name"
      },
      {
        text: "Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.",
        userName: "User Name"
      }
    ]
  },
  {
    cards: [
      {
        text: "Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        userName: "User Name"
      },
      {
        text: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium.",
        userName: "User Name"
      },
      {
        text: "Totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt.",
        userName: "User Name"
      }
    ]
  },
  {
    cards: [
      {
        text: "Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores.",
        userName: "User Name"
      },
      {
        text: "Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet consectetur adipisci velit.",
        userName: "User Name"
      },
      {
        text: "Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam.",
        userName: "User Name"
      }
    ]
  },
  {
    cards: [
      {
        text: "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti.",
        userName: "User Name"
      },
      {
        text: "Et harum quidem rerum facilis est et expedita distinctio nam libero tempore cum soluta nobis est eligendi optio.",
        userName: "User Name"
      },
      {
        text: "Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates.",
        userName: "User Name"
      }
    ]
  }
])

// Current review state
const currentReview = ref(0)

// Navigation functions
const nextReview = () => {
  if (currentReview.value < reviews.value.length - 1) {
    currentReview.value++
  }
}

const previousReview = () => {
  if (currentReview.value > 0) {
    currentReview.value--
  }
}

const goToReview = (index) => {
  currentReview.value = index
}

// Auto-slide functionality (optional)
onMounted(() => {
  const autoSlide = setInterval(() => {
    if (currentReview.value < reviews.value.length - 1) {
      currentReview.value++
    } else {
      currentReview.value = 0
    }
  }, 5000) // Auto slide every 5 seconds

  // Clean up interval on component unmount
  onUnmounted(() => {
    clearInterval(autoSlide)
  })
})

// FAQ state
const activeFAQ = ref(null)

// FAQ toggle function
const toggleFAQ = (index) => {
  activeFAQ.value = activeFAQ.value === index ? null : index
}
</script>