<!-- The exported code uses Tailwind CSS. Install Tailwind CSS in your dev environment to ensure all styles work. -->

<template>
  <div class="min-h-screen bg-gray-50">
    <!-- 导航栏 -->
    <nav class="fixed w-full z-50 bg-white/80 backdrop-blur-md shadow-sm">
      <div class="max-w-7xl mx-auto px-4 h-16 flex items-center justify-between">
        <div class="flex items-center space-x-2">
          <img :src="logoUrl" alt="Cinastan" class="h-8">
          <span class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-amber-500 bg-clip-text text-transparent">Cinastan</span>
        </div>
        <div class="flex items-center space-x-8">
          <a v-for="item in navItems" :key="item" href="#" class="text-gray-600 hover:text-blue-600 transition-colors">{{ item }}</a>
          <button class="!rounded-button bg-blue-600 text-white px-4 py-2 hover:bg-blue-700 transition-colors whitespace-nowrap">联系我们</button>
        </div>
      </div>
    </nav>

    <!-- Hero区域 -->
    <div
  class="relative h-screen"
  :style="{
    backgroundImage: `url(${heroBackgroundUrl})`,
    backgroundSize: 'cover',
    backgroundRepeat: 'no-repeat',
    backgroundPosition: 'center'
  }"
>
      <div class="absolute inset-0 bg-gradient-to-r from-gray-900/90 to-transparent">
        <div class="max-w-7xl mx-auto px-4 h-full flex items-center">
          <div class="max-w-2xl text-white space-y-6">
            <h1 class="text-5xl font-bold leading-tight">连接古今，驱动未来</h1>
            <p class="text-xl text-gray-200">Digital Silk Road Pioneer</p>
            <p class="text-gray-300">作为数字丝绸之路的先驱者，我们致力于将传统贸易与现代科技完美融合，开创全新的商业模式。</p>
            <button class="!rounded-button bg-amber-500 text-white px-6 py-3 text-lg hover:bg-amber-600 transition-colors whitespace-nowrap">了解更多</button>
          </div>
        </div>
      </div>
    </div>

    <!-- 业务领域 -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">业务领域</h2>
        <div class="grid grid-cols-3 gap-8">
          <div v-for="(service, index) in services" :key="index" class="group relative overflow-hidden rounded-xl shadow-lg">
            <img :src="service.image" :alt="service.title" class="w-full h-64 object-cover object-top transition-transform group-hover:scale-105">
            <div class="absolute inset-0 bg-gradient-to-t from-gray-900/90 to-transparent flex flex-col justify-end p-6">
              <h3 class="text-xl font-bold text-white mb-2">{{ service.title }}</h3>
              <p class="text-gray-200 text-sm">{{ service.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 合作伙伴 -->
    <section class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">合作伙伴</h2>
        <swiper
          :modules="swiperModules"
          :slides-per-view="5"
          :space-between="30"
          :autoplay="{ delay: 3000 }"
          :loop="true"
          class="partner-swiper"
        >
          <swiper-slide v-for="(partner, index) in partners" :key="index">
            <div class="bg-white rounded-lg shadow-md p-6 h-32 flex items-center justify-center">
              <img :src="partner.logo" :alt="partner.name" class="max-h-16">
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </section>

    <!-- 新闻动态 -->
    <section class="py-20 bg-white">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">新闻动态</h2>
        <div class="grid grid-cols-3 gap-8">
          <div v-for="(news, index) in newsItems" :key="index" class="group">
            <div class="overflow-hidden rounded-xl mb-4">
              <img :src="news.image" :alt="news.title" class="w-full h-48 object-cover object-top transition-transform group-hover:scale-105">
            </div>
            <div class="space-y-2">
              <div class="text-sm text-gray-500">{{ news.date }}</div>
              <h3 class="text-lg font-semibold group-hover:text-blue-600 transition-colors">{{ news.title }}</h3>
              <p class="text-gray-600 line-clamp-2">{{ news.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 客户反馈 -->
    <section class="py-20 bg-gray-50">
      <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-16">客户反馈</h2>
        <swiper
          :modules="swiperModules"
          :slides-per-view="3"
          :space-between="30"
          :autoplay="{ delay: 5000 }"
          :loop="true"
          class="testimonial-swiper"
        >
          <swiper-slide v-for="(testimonial, index) in testimonials" :key="index">
            <div class="bg-white rounded-xl shadow-lg p-6 space-y-4">
              <div class="flex items-center space-x-4">
                <img :src="testimonial.avatar" :alt="testimonial.name" class="w-12 h-12 rounded-full">
                <div>
                  <div class="font-semibold">{{ testimonial.name }}</div>
                  <div class="text-sm text-gray-500">{{ testimonial.company }}</div>
                </div>
              </div>
              <p class="text-gray-600">{{ testimonial.content }}</p>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </section>

    <!-- 页脚 -->
    <footer class="bg-gray-900 text-gray-300 py-12">
      <div class="max-w-7xl mx-auto px-4 grid grid-cols-4 gap-8">
        <div>
          <img :src="logoUrl" alt="Cinastan" class="h-8 mb-4">
          <p class="text-sm">数字丝绸之路的开拓者，致力于连接全球贸易，创新商业未来。</p>
        </div>
        <div>
          <h3 class="text-white font-semibold mb-4">联系方式</h3>
          <div class="space-y-2 text-sm">
            <p>电话：400-888-8888</p>
            <p>邮箱：contact@cinastan.com</p>
            <p>地址：长安市大汉新区数字贸易大厦</p>
          </div>
        </div>
        <div>
          <h3 class="text-white font-semibold mb-4">快速链接</h3>
          <div class="space-y-2 text-sm">
            <a v-for="item in navItems" :key="item" href="#" class="block hover:text-white transition-colors">{{ item }}</a>
          </div>
        </div>
        <div>
          <h3 class="text-white font-semibold mb-4">关注我们</h3>
          <div class="flex space-x-4">
            <el-icon class="text-2xl cursor-pointer hover:text-white transition-colors"><Position /></el-icon>
            <el-icon class="text-2xl cursor-pointer hover:text-white transition-colors"><ChatDotRound /></el-icon>
            <el-icon class="text-2xl cursor-pointer hover:text-white transition-colors"><Share /></el-icon>
          </div>
        </div>
      </div>
      <div class="max-w-7xl mx-auto px-4 mt-8 pt-8 border-t border-gray-800 text-center text-sm">
        <p>© 2025 Cinastan. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination, Autoplay } from 'swiper/modules';
// @ts-ignore
import "swiper/css";
// @ts-ignore
import "swiper/css/navigation";
// @ts-ignore
import "swiper/css/pagination";
// @ts-ignore
import { Position, ChatDotRound, Share } from '@element-plus/icons-vue';

const swiperModules = [Pagination, Autoplay];

const logoUrl = '/28474f09a368cdbeeac5d5a2bc80465e.jpg';

const heroBackgroundUrl = '/6afe1247d82c40c36103f02d8fdc9223.jpg';

const navItems = ['首页', '关于我们', '业务领域', '合作伙伴', '新闻中心', '联系我们'];

const services = [
  {
    title: '陆上贸易',
    description: '通过智能物流系统，打造高效、安全、可追溯的陆路运输网络。',
    image: '/df882868b446d7e8c254fffe53666137.jpg'
  },
  {
    title: '海上贸易',
    description: '依托智能航运系统，构建全球化海运贸易生态。',
    image: '/39284c97d5178335d961db33615d7bf9.jpg'
  },
  {
    title: '太空贸易',
    description: '利用卫星通信技术，开创太空数字贸易新纪元。',
    image: '/8b6a402633a017dc9bfa3c340bc44ed2.jpg'
  }
];

const partners = [
  { name: '全球物流', logo: '/82776bcc0e69cfb96d02bd316d0832b3.jpg' },
  { name: '智慧港口', logo: '/bed2111509c4792e94a274ec8af45ab0.jpg' },
  { name: '数字科技', logo: '/3384becbe39d356f6bd47dff777a07ae.jpg' },
  { name: '航天通信', logo: '/cadd255b9b20594dbfde085c2e944626.jpg' },
  { name: '金融服务', logo: '/7a9a8f2797656b8dccff337f01ff5636.jpg' },
  { name: '智能制造', logo: '/e759a4038337f09ba81eb5ff014000da.jpg' }
];

const newsItems = [
  {
    title: '数字丝绸之路建设取得重大突破',
    date: '2025-03-01',
    description: '我司成功完成首个跨洲际智能物流网络部署，实现全程可视化追踪。',
    image: '/bb1f33092eeebd05a27098857671773d.jpg'
  },
  {
    title: '智慧港口项目落地东南亚',
    date: '2025-02-28',
    description: '新一代智慧港口管理系统在新加坡正式投入使用，效率提升50%。',
    image: '/16ed6517145b13b106ffc3bd985be742.jpg'
  },
  {
    title: '太空数据中心启动建设',
    date: '2025-02-25',
    description: '公司投资百亿建设低轨道数据中心，打造太空云服务平台。',
    image: '/e29b9dd981df0219a761baadfd9aeccd.jpg'
  }
];

const testimonials = [
  {
    name: '张明远',
    company: '远洋航运集团',
    content: '与 Cinastan 合作让我们的航运效率提升了30%，智能调度系统非常出色。',
    avatar: '/cafe00fe72c6aaab7cab2348864a503b.jpg'
  },
  {
    name: '李晓华',
    company: '数字科技有限公司',
    content: '太空数据服务为我们提供了前所未有的全球视野，合作非常愉快。',
    avatar: '/b78bfe48fcc46ab59435a2283241daa8.jpg'
  },
  {
    name: '王志强',
    company: '智慧物流科技',
    content: '数字化转型过程中，Cinastan 提供的解决方案让我们受益匪浅。',
    avatar: '/276fe750ee165c02845c2dcc93d79b74.jpg'
  },
  {
    name: '陈思琪',
    company: '全球贸易集团',
    content: '他们的创新理念和专业服务态度，为我们带来了显著的业务增长。',
    avatar: '/b3929c43c2cc110cff0c701d0bfe8663.jpg'
  }
];
</script>

<style scoped>
.partner-swiper {
  padding: 20px 0;
}

.testimonial-swiper {
  padding: 20px 0;
}
</style>

