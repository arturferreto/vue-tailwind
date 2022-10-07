<script>
  import { RouterLink, RouterView } from 'vue-router'
  import Dw from '@/components/icons/Dw.vue'
  
  export default {
    data() {
      return {
        current: true
      }
    },
    computed: {
      route() {
        return this.$route
      }
    },
    components: {
      RouterLink,
      RouterView,
      Dw
    }
  }
  </script>
  
  <template>
    <header>
      <nav class="bg-white shadow">
        <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
          <div class="relative flex h-16 justify-between">
            <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
              <div class="flex flex-shrink-0 items-center">
                <Dw class="block h-8 w-auto" src="https://tailwindui.com/img/logos/mark.svg?color=indigo&shade=600" />
              </div>
              <div class="hidden sm:ml-6 sm:flex sm:space-x-8">
                <RouterLink to="/" :class="[route.path === '/' ? 'border-indigo-500 text-gray-900' : 'hover:border-gray-300 text-gray-500 hover:text-gray-700 border-transparent', 'inline-flex items-center border-b-2  px-1 pt-1 text-sm font-medium']">
                  Home
                </RouterLink>

                <RouterLink to="/about" :class="[route.path === '/about' ? 'border-indigo-500 text-gray-900' : 'hover:border-gray-300 text-gray-500 hover:text-gray-700 border-transparent', 'inline-flex items-center border-b-2  px-1 pt-1 text-sm font-medium']">
                  About
                </RouterLink>

                <RouterLink to="/artur" :class="[route.path === '/artur' ? 'border-indigo-500 text-gray-900' : 'hover:border-gray-300 text-gray-500 hover:text-gray-700 border-transparent', 'inline-flex items-center border-b-2  px-1 pt-1 text-sm font-medium']">
                  Artur
                </RouterLink>
              </div>
            </div>
          </div>
        </div>
    
        <div class="sm:hidden" id="mobile-menu">
          <div class="space-y-1 pt-2 pb-4">
            <RouterLink to="/" :class="[ route.path === '/' ? 'bg-indigo-50 border-indigo-500 text-indigo-700' : 'text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700', 'block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium']">
              Home
            </RouterLink>
            
            <RouterLink to="/about" :class="[ route.path === '/about' ? 'bg-indigo-50 border-indigo-500 text-indigo-700' : 'text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700', 'block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium']">
              About
            </RouterLink>

            <RouterLink to="/artur" :class="[ route.path === '/artur' ? 'bg-indigo-50 border-indigo-500 text-indigo-700' : 'text-gray-500 hover:border-gray-300 hover:bg-gray-50 hover:text-gray-700', 'block border-l-4 border-transparent py-2 pl-3 pr-4 text-base font-medium']">
              Artur
            </RouterLink>
          </div>
        </div>
      </nav>
    </header>
  
    <RouterView />
  </template>