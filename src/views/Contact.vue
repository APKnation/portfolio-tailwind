<template>
  <section id="contact" class="py-16 sm:py-20 bg-gray-900 text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="text-4xl font-extrabold text-white sm:text-5xl leading-tight mb-4">
          <span class="gradient-text">Contact Me</span>
        </h2>
        <p class="text-lg text-gray-400 max-w-2xl mx-auto">
          I'm always open to new opportunities, collaborations, and interesting projects.
          Feel free to reach out, and I'll get back to you as soon as possible!
        </p>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">
        <!-- Contact Form -->
        <div class="bg-gray-800 p-8 rounded-lg shadow-xl border border-primary-700/50">
          <h3 class="text-3xl font-bold text-white mb-8">Send Message</h3>
          <form @submit.prevent="submitForm" class="space-y-6">
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div>
                <label for="name" class="block text-sm font-medium text-gray-300 mb-2">Name <span class="text-red-500">*</span></label>
                <input type="text" id="name" v-model="form.name" required
                       class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-md text-white
                              focus:ring-primary-500 focus:border-primary-500 placeholder-gray-400">
              </div>
              <div>
                <label for="email" class="block text-sm font-medium text-gray-300 mb-2">Email <span class="text-red-500">*</span></label>
                <input type="email" id="email" v-model="form.email" required
                       class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-md text-white
                              focus:ring-primary-500 focus:border-primary-500 placeholder-gray-400">
              </div>
            </div>
            <div>
              <label for="subject" class="block text-sm font-medium text-gray-300 mb-2">Subject <span class="text-red-500">*</span></label>
              <input type="text" id="subject" v-model="form.subject" required
                     class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-md text-white
                            focus:ring-primary-500 focus:border-primary-500 placeholder-gray-400">
            </div>
            <div>
              <label for="message" class="block text-sm font-medium text-gray-300 mb-2">Message <span class="text-red-500">*</span></label>
              <textarea id="message" v-model="form.message" rows="4" required
                        class="w-full px-4 py-2 bg-gray-700 border border-gray-600 rounded-md text-white
                               focus:ring-primary-500 focus:border-primary-500 placeholder-gray-400 resize-none"></textarea>
            </div>
            <button type="submit" 
                    :disabled="isSubmitting"
                    class="w-full bg-gradient-to-r from-primary-600 to-secondary-600 text-white py-3 px-6 
                           rounded-md font-medium hover:from-primary-700 hover:to-secondary-700 
                           transition-all duration-300 transform hover:scale-105 disabled:opacity-50 
                           disabled:cursor-not-allowed">
              {{ isSubmitting ? 'Sending...' : 'Send Message' }}
            </button>
          </form>
        </div>

        <!-- Let's Connect Section -->
        <div class="bg-gray-800 p-8 rounded-lg shadow-xl border border-primary-700/50">
          <h3 class="text-3xl font-bold text-white mb-8">Let's Connect</h3>
          <p class="text-gray-300 mb-8 leading-relaxed">
            Whether you have a project in mind, want to discuss potential collaborations, 
            or just want to say hello, I'd love to hear from you. The best way to reach me 
            is through the platforms below.
          </p>
          
          <div class="space-y-6">
            <!-- GitHub -->
            <div class="flex items-center justify-between p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors duration-300">
              <div class="flex items-center space-x-4">
                <div class="w-12 h-12 bg-gray-800 rounded-full flex items-center justify-center">
                  <Github class="w-6 h-6 text-white" />
                </div>
                <div>
                  <h4 class="text-white font-semibold">GitHub</h4>
                  <p class="text-gray-400 text-sm">Check out my projects and contributions</p>
                </div>
              </div>
              <a href="https://github.com/APKnation" target="_blank" rel="noopener noreferrer"
                 class="text-primary-400 hover:text-primary-300 transition-colors duration-300 flex items-center space-x-2">
                <span class="text-sm">Connect with me</span>
                <ExternalLink class="w-4 h-4" />
              </a>
            </div>

            <!-- Instagram -->
            <div class="flex items-center justify-between p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors duration-300">
              <div class="flex items-center space-x-4">
                <div class="w-12 h-12 bg-gradient-to-br from-purple-600 to-pink-600 rounded-full flex items-center justify-center">
                  <Instagram class="w-6 h-6 text-white" />
                </div>
                <div>
                  <h4 class="text-white font-semibold">Instagram</h4>
                  <p class="text-gray-400 text-sm">Follow for updates and insights</p>
                </div>
              </div>
              <a href="https://instagram.com/apk_nation" target="_blank" rel="noopener noreferrer"
                 class="text-primary-400 hover:text-primary-300 transition-colors duration-300 flex items-center space-x-2">
                <span class="text-sm">Connect with me</span>
                <ExternalLink class="w-4 h-4" />
              </a>
            </div>

            <!-- WhatsApp -->
            <div class="flex items-center justify-between p-4 bg-gray-700 rounded-lg hover:bg-gray-600 transition-colors duration-300">
              <div class="flex items-center space-x-4">
                <div class="w-12 h-12 bg-green-600 rounded-full flex items-center justify-center">
                  <MessageCircle class="w-6 h-6 text-white" />
                </div>
                <div>
                  <h4 class="text-white font-semibold">WhatsApp</h4>
                  <p class="text-gray-400 text-sm">+255749288072</p>
                </div>
              </div>
              <a href="https://wa.me/255749288072" target="_blank" rel="noopener noreferrer"
                 class="text-primary-400 hover:text-primary-300 transition-colors duration-300 flex items-center space-x-2">
                <span class="text-sm">Connect with me</span>
                <ExternalLink class="w-4 h-4" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, reactive } from 'vue'
import { Github, Instagram, MessageCircle, ExternalLink } from 'lucide-vue-next'
import { useToast } from 'vue-toastification'

const toast = useToast()
const isSubmitting = ref(false)

const form = reactive({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const submitForm = async () => {
  if (!form.name || !form.email || !form.subject || !form.message) {
    toast.error('Please fill in all required fields')
    return
  }
  
  if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(form.email)) {
    toast.error('Please enter a valid email address')
    return
  }
  
  isSubmitting.value = true
  
  try {
    // Simulate API call
    await new Promise(resolve => setTimeout(resolve, 2000))
    
    toast.success('Message sent successfully! I\'ll get back to you soon.')
    
    // Reset form
    Object.keys(form).forEach(key => form[key] = '')
    
  } catch (error) {
    toast.error('Failed to send message. Please try again.')
  } finally {
    isSubmitting.value = false
  }
}
</script>
