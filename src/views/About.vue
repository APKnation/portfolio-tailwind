<template>
  <section id="about" class="py-16 sm:py-20 px-4 bg-gray-900 text-white">
    <div class="max-w-7xl mx-auto">
      <transition appear name="fade">
        <h2 class="text-3xl sm:text-4xl font-bold text-center mb-12 sm:mb-16 text-white">
          About Me
        </h2>
      </transition>
      
      <div class="flex flex-col lg:flex-row items-center gap-8 sm:gap-12">
        <!-- Profile Image with Advanced Card -->
        <transition appear name="slide-in-left">
          <div class="lg:w-1/3 flex justify-center">
            <div class="relative group">
              <!-- Advanced Card Background -->
              <div class="absolute inset-0 bg-gradient-to-br from-gray-800 to-gray-900 rounded-2xl 
                           transform rotate-3 group-hover:rotate-6 transition-all duration-500 
                           shadow-2xl border border-gray-700/50"></div>
              
              <!-- Card Content -->
              <div class="relative bg-gray-800/90 backdrop-blur-sm rounded-2xl p-6 
                         border border-gray-700/50 shadow-xl transform hover:scale-105 
                         transition-all duration-500 hover:shadow-2xl">
                
                <!-- Profile Image -->
                <div class="relative mb-6">
                  <img 
                    src="/src/assets/images/profile.jpg" 
                    alt="About Atanas" 
                    class="w-48 h-48 sm:w-56 sm:h-56 object-cover rounded-xl 
                           border-4 border-gray-700 shadow-lg"
                  >
                  <!-- Decorative Elements -->
                  <div class="absolute -top-2 -right-2 w-6 h-6 bg-gray-600 rounded-full 
                               animate-pulse"></div>
                  <div class="absolute -bottom-2 -left-2 w-4 h-4 bg-gray-600 rounded-full 
                               animate-pulse delay-75"></div>
                </div>
                
                <!-- Name and Title -->
                <div class="text-center">
                  <h3 class="text-xl font-bold text-white mb-2">Atanas Patrick</h3>
                  <p class="text-gray-400 text-sm">Software Engineer</p>
                </div>
              </div>
            </div>
          </div>
        </transition>

        <!-- Content with Advanced Card -->
        <transition appear name="slide-in-right">
          <div class="lg:w-2/3">
            <div class="bg-gray-800/90 backdrop-blur-sm rounded-2xl p-6 sm:p-8 
                       border border-gray-700/50 shadow-xl hover:shadow-2xl 
                       transition-all duration-500 hover:border-gray-600/50">
              
              <!-- Bio Section -->
              <div class="mb-8">
                <h3 class="text-xl font-semibold text-white mb-4 flex items-center">
                  <div class="w-2 h-2 bg-gray-600 rounded-full mr-3"></div>
                  Introduction
                </h3>
                <div class="space-y-4 text-gray-300 leading-relaxed">
                  <p class="text-base">
                    I'm Atanas Patrick, a passionate software engineer with 1 year of experience building 
                    scalable web applications and solving complex problems with elegant code solutions.
                  </p>
                  <p class="text-base">
                    My approach combines technical expertise with a keen eye for user experience, ensuring that the 
                    solutions I build are not only functional but also intuitive and enjoyable to use. 
                    I specialize in modern web technologies and frameworks that deliver exceptional results.
                  </p>
                </div>
              </div>

              <!-- Skills & Expertise -->
              <div class="mb-8">
                <h3 class="text-xl font-semibold text-white mb-4 flex items-center">
                  <div class="w-2 h-2 bg-gray-600 rounded-full mr-3"></div>
                  Expertise
                </h3>
                <div class="grid grid-cols-2 sm:grid-cols-3 gap-3">
                  <div class="bg-gray-700/50 rounded-lg p-3 text-center hover:bg-gray-700 
                               transition-colors duration-300">
                    <span class="text-gray-300 text-sm">JavaScript</span>
                  </div>
                  <div class="bg-gray-700/50 rounded-lg p-3 text-center hover:bg-gray-700 
                               transition-colors duration-300">
                    <span class="text-gray-300 text-sm">Vue.js</span>
                  </div>
                  <div class="bg-gray-700/50 rounded-lg p-3 text-center hover:bg-gray-700 
                               transition-colors duration-300">
                    <span class="text-gray-300 text-sm">Laravel</span>
                  </div>
                  <div class="bg-gray-700/50 rounded-lg p-3 text-center hover:bg-gray-700 
                               transition-colors duration-300">
                    <span class="text-gray-300 text-sm">React</span>
                  </div>
                  <div class="bg-gray-700/50 rounded-lg p-3 text-center hover:bg-gray-700 
                               transition-colors duration-300">
                    <span class="text-gray-300 text-sm">Node.js</span>
                  </div>
                  <div class="bg-gray-700/50 rounded-lg p-3 text-center hover:bg-gray-700 
                               transition-colors duration-300">
                    <span class="text-gray-300 text-sm">Tailwind CSS</span>
                  </div>
                </div>
              </div>

              <!-- Contact Information Grid -->
              <div>
                <h3 class="text-xl font-semibold text-white mb-4 flex items-center">
                  <div class="w-2 h-2 bg-gray-600 rounded-full mr-3"></div>
                  Get In Touch
                </h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                  <div class="flex items-center space-x-3 p-4 bg-gray-700/30 rounded-lg 
                               hover:bg-gray-700/50 transition-all duration-300 group">
                    <div class="bg-gray-600/30 p-2 rounded-lg group-hover:bg-gray-600/50 
                                transition-colors duration-300">
                      <MapPin class="w-5 h-5 text-gray-400" />
                    </div>
                    <div>
                      <p class="text-xs text-gray-500">Location</p>
                      <p class="text-sm text-gray-300">Dodoma-Tanzania</p>
                    </div>
                  </div>
                  
                  <div class="flex items-center space-x-3 p-4 bg-gray-700/30 rounded-lg 
                               hover:bg-gray-700/50 transition-all duration-300 group">
                    <div class="bg-gray-600/30 p-2 rounded-lg group-hover:bg-gray-600/50 
                                transition-colors duration-300">
                      <Mail class="w-5 h-5 text-gray-400" />
                    </div>
                    <div>
                      <p class="text-xs text-gray-500">Email</p>
                      <p class="text-sm text-gray-300">atanasikafuka@gmail.com</p>
                    </div>
                  </div>
                  
                  <div class="flex items-center space-x-3 p-4 bg-gray-700/30 rounded-lg 
                               hover:bg-gray-700/50 transition-all duration-300 group">
                    <div class="bg-gray-600/30 p-2 rounded-lg group-hover:bg-gray-600/50 
                                transition-colors duration-300">
                      <Phone class="w-5 h-5 text-gray-400" />
                    </div>
                    <div>
                      <p class="text-xs text-gray-500">Phone</p>
                      <p class="text-sm text-gray-300">+255749288072</p>
                    </div>
                  </div>
                  
                  <!-- Download Resume Button -->
                  <div class="flex items-center justify-center">
                    <a 
                      href="/src/assets/images/resume.pdf" 
                      download
                      class="inline-flex items-center space-x-2 bg-gray-700 hover:bg-gray-600 
                             text-white px-4 py-2 rounded-lg transition-all duration-300 
                             transform hover:scale-105 text-sm"
                    >
                      <Download class="w-4 h-4" />
                      <span>Download Resume</span>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </transition>
      </div>
    </div>
  </section>
</template>

<script setup>
import { MapPin, Mail, Phone, Download } from 'lucide-vue-next'
</script>
