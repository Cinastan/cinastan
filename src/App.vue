<!-- The exported code uses Tailwind CSS. Install Tailwind CSS in your dev environment to ensure all styles work. -->
<template>
    <div class="min-h-screen bg-gradient-to-b from-[#1B3B5A] to-[#0F2235] text-white">
        <!-- 顶部导航栏 -->
        <header class="fixed w-full top-0 z-50 bg-[#1B3B5A]/90 backdrop-blur-sm border-b border-[#DAA520]/20">
            <div class="container mx-auto flex justify-between items-center py-4 px-6">
                <div class="flex items-center">
                    <div class="text-[#DAA520] font-bold text-2xl mr-2">Cinastan</div>
                    <div class="text-white/80 text-sm">秦尼斯坦</div>
                </div>
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="#"
                        class="text-white hover:text-[#DAA520] transition-colors cursor-pointer whitespace-nowrap">首页</a>
                    <a href="#business"
                        class="text-white/80 hover:text-[#DAA520] transition-colors cursor-pointer whitespace-nowrap">业务版块</a>
                    <a href="#culture"
                        class="text-white/80 hover:text-[#DAA520] transition-colors cursor-pointer whitespace-nowrap">文化驱动</a>
                    <a href="#partners"
                        class="text-white/80 hover:text-[#DAA520] transition-colors cursor-pointer whitespace-nowrap">合作与投资</a>
                    <a href="#join"
                        class="text-white/80 hover:text-[#DAA520] transition-colors cursor-pointer whitespace-nowrap">人才招聘</a>
                    <a href="#tech"
                        class="text-white/80 hover:text-[#DAA520] transition-colors cursor-pointer whitespace-nowrap">技术与可持续</a>
                </nav>
                <div class="flex items-center space-x-4">
                    <div class="relative group">
                        <button
                            class="flex items-center text-white/80 hover:text-[#DAA520] cursor-pointer !rounded-button whitespace-nowrap">
                            <span>中文</span>
                            <el-icon class="ml-1">
                                <ArrowDown />
                            </el-icon>
                        </button>
                        <div
                            class="absolute right-0 mt-2 w-40 bg-[#1B3B5A] border border-[#DAA520]/30 rounded-md shadow-lg hidden group-hover:block">
                            <a href="#"
                                class="block px-4 py-2 text-sm text-white hover:bg-[#DAA520]/20 cursor-pointer">English</a>
                            <a href="#"
                                class="block px-4 py-2 text-sm text-white hover:bg-[#DAA520]/20 cursor-pointer">Русский</a>
                            <a href="#"
                                class="block px-4 py-2 text-sm text-white hover:bg-[#DAA520]/20 cursor-pointer">فارسی</a>
                            <a href="#"
                                class="block px-4 py-2 text-sm text-white hover:bg-[#DAA520]/20 cursor-pointer">العربية</a>
                        </div>
                    </div>
                    <button
                        class="bg-[#DAA520] text-[#1B3B5A] px-4 py-2 rounded-md font-medium hover:bg-[#DAA520]/90 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                        联系我们
                    </button>
                </div>
                <button class="md:hidden text-white" @click="toggleMobileMenu">
                    <el-icon size="24">
                        <Menu />
                    </el-icon>
                </button>
            </div>
            <!-- 移动端菜单 -->
            <div v-if="mobileMenuOpen" class="md:hidden bg-[#1B3B5A] border-t border-[#DAA520]/20 py-4">
                <div class="container mx-auto px-6 flex flex-col space-y-4">
                    <a href="#" class="text-white hover:text-[#DAA520] transition-colors py-2 cursor-pointer">首页</a>
                    <a href="#business"
                        class="text-white/80 hover:text-[#DAA520] transition-colors py-2 cursor-pointer">业务版块</a>
                    <a href="#culture"
                        class="text-white/80 hover:text-[#DAA520] transition-colors py-2 cursor-pointer">文化驱动</a>
                    <a href="#partners"
                        class="text-white/80 hover:text-[#DAA520] transition-colors py-2 cursor-pointer">合作与投资</a>
                    <a href="#join"
                        class="text-white/80 hover:text-[#DAA520] transition-colors py-2 cursor-pointer">人才招聘</a>
                    <a href="#tech"
                        class="text-white/80 hover:text-[#DAA520] transition-colors py-2 cursor-pointer">技术与可持续</a>
                </div>
            </div>
        </header>
        <!-- Hero 区域 -->
        <section class="relative pt-24 min-h-[800px] flex items-center"
            style="background-image: url(&quot;/img_9.jpg&quot;)">
            <div class="absolute inset-0 bg-gradient-to-r from-[#1B3B5A]/95 to-transparent"></div>
            <div class="container mx-auto px-6 relative z-10 flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight">
                        <span class="text-[#DAA520]">丝路</span>新纪元
                        <br />连接古今，贯通未来
                    </h1>
                    <p class="text-xl md:text-2xl mb-8 text-white/90 leading-relaxed">
                        从长安到巴格达，从泉州到亚历山大，从轨道到火星前哨——我们编织丝路的每一段光年。
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <button
                            class="bg-[#DAA520] text-[#1B3B5A] px-6 py-3 rounded-md font-medium hover:bg-[#DAA520]/90 transition-colors text-lg cursor-pointer !rounded-button whitespace-nowrap">
                            探索我们的业务
                        </button>
                        <button
                            class="border border-[#DAA520] text-[#DAA520] px-6 py-3 rounded-md font-medium hover:bg-[#DAA520]/10 transition-colors text-lg cursor-pointer !rounded-button whitespace-nowrap">
                            观看企业纪录片
                        </button>
                    </div>
                </div>
            </div>
        </section>
        <!-- 最新贸易动态 -->
        <section class="py-16 bg-[#0F2235]">
            <div class="container mx-auto px-6">
                <div class="flex justify-between items-center mb-8">
                    <h2 class="text-3xl font-bold text-white">
                        <span class="text-[#DAA520]">最新</span>贸易动态
                    </h2>
                    <div class="flex space-x-2">
                        <button
                            class="prev-button p-2 rounded-full border border-[#DAA520]/30 text-[#DAA520] hover:bg-[#DAA520]/10 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                            <el-icon>
                                <ArrowLeft />
                            </el-icon>
                        </button>
                        <button
                            class="next-button p-2 rounded-full border border-[#DAA520]/30 text-[#DAA520] hover:bg-[#DAA520]/10 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                            <el-icon>
                                <ArrowRight />
                            </el-icon>
                        </button>
                    </div>
                </div>
                <swiper :modules="swiperModules" :slides-per-view="1" :breakpoints="swiperBreakpoints"
                    :space-between="30" :pagination="{ clickable: true }"
                    :autoplay="{ delay: 5000, disableOnInteraction: false }" class="news-swiper" @swiper="onSwiperInit">
                    <swiper-slide v-for="(news, index) in newsItems" :key="index">
                        <div
                            class="bg-[#1B3B5A]/50 border border-[#DAA520]/10 rounded-xl overflow-hidden hover:border-[#DAA520]/30 transition-colors">
                            <div class="flex flex-col md:flex-row">
                                <div class="md:w-1/3 h-64 md:h-auto overflow-hidden">
                                    <img :src="news.image" alt="新闻图片" class="w-full h-full object-cover object-top" />
                                </div>
                                <div class="md:w-2/3 p-6 md:p-8">
                                    <div class="flex items-center mb-4">
                                        <span class="bg-[#DAA520]/20 text-[#DAA520] px-3 py-1 rounded-full text-sm">{{
                                            news.category }}</span>
                                        <span class="ml-4 text-white/60 text-sm">{{
                                            news.date
                                            }}</span>
                                    </div>
                                    <h3 class="text-xl md:text-2xl font-bold mb-4">
                                        {{ news.title }}
                                    </h3>
                                    <p class="text-white/80 mb-6 line-clamp-3">
                                        {{ news.content }}
                                    </p>
                                    <button
                                        class="text-[#DAA520] hover:text-[#DAA520]/80 flex items-center cursor-pointer !rounded-button whitespace-nowrap">
                                        阅读更多
                                        <el-icon class="ml-1">
                                            <ArrowRight />
                                        </el-icon>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </swiper-slide>
                </swiper>
            </div>
        </section>
        <!-- 核心业务 -->
        <section id="business" class="py-16 bg-[#1B3B5A] relative overflow-hidden">
            <div class="absolute inset-0 opacity-10" style="
          background-image: url(&quot;/img_12.jpg&quot;);
          background-size: cover;
        "></div>
            <div class="container mx-auto px-6 relative z-10">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="text-[#DAA520]">核心</span>业务版块
                    </h2>
                    <p class="text-white/80 max-w-3xl mx-auto">
                        Cinastan 秦尼斯坦
                        立志成为连接过去与未来的全球丝路贸易核心节点企业，在"陆海空（太空）三线融合"的大格局中重塑丝路精神。
                    </p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div
                        class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-xl p-6 hover:border-[#DAA520]/30 transition-all hover:translate-y-[-5px] cursor-pointer">
                        <div class="h-48 mb-6 overflow-hidden rounded-lg">
                            <img src="/img_1.jpg" alt="陆上丝绸之路" class="w-full h-full object-cover object-top" />
                        </div>
                        <h3 class="text-xl font-bold mb-3 flex items-center">
                            <el-icon class="mr-2 text-[#DAA520]">
                                <Location />
                            </el-icon>
                            陆上丝绸之路
                        </h3>
                        <p class="text-white/70 mb-4">
                            连接中国、中亚、波斯及欧洲的陆上贸易网络，专注于能源、矿产物流与特色商品集采。
                        </p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">中亚能源</span>
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">矿产物流</span>
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">特色商品</span>
                        </div>
                        <button
                            class="flex items-center text-[#DAA520] hover:text-[#DAA520]/80 cursor-pointer !rounded-button whitespace-nowrap">
                            了解更多
                            <el-icon class="ml-1">
                                <ArrowRight />
                            </el-icon>
                        </button>
                    </div>
                    <div
                        class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-xl p-6 hover:border-[#DAA520]/30 transition-all hover:translate-y-[-5px] cursor-pointer">
                        <div class="h-48 mb-6 overflow-hidden rounded-lg">
                            <img src="/img_7.jpg" alt="海上丝绸之路" class="w-full h-full object-cover object-top" />
                        </div>
                        <h3 class="text-xl font-bold mb-3 flex items-center">
                            <el-icon class="mr-2 text-[#DAA520]">
                                <Ship />
                            </el-icon>
                            海上丝绸之路
                        </h3>
                        <p class="text-white/70 mb-4">
                            贯通广州、马六甲、科伦坡、阿拉伯港口及威尼斯的海上贸易航线，提供港口运营与航线优化服务。
                        </p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">港口运营</span>
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">航线优化</span>
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">水产贸易</span>
                        </div>
                        <button
                            class="flex items-center text-[#DAA520] hover:text-[#DAA520]/80 cursor-pointer !rounded-button whitespace-nowrap">
                            了解更多
                            <el-icon class="ml-1">
                                <ArrowRight />
                            </el-icon>
                        </button>
                    </div>
                    <div
                        class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-xl p-6 hover:border-[#DAA520]/30 transition-all hover:translate-y-[-5px] cursor-pointer">
                        <div class="h-48 mb-6 overflow-hidden rounded-lg">
                            <img src="/img_13.jpg" alt="太空丝绸之路" class="w-full h-full object-cover object-top" />
                        </div>
                        <h3 class="text-xl font-bold mb-3 flex items-center">
                            <el-icon class="mr-2 text-[#DAA520]">
                                <Star />
                            </el-icon>
                            太空丝绸之路
                        </h3>
                        <p class="text-white/70 mb-4">
                            面向未来的太空贸易愿景，包括轨道物资运输、月球稀土贸易模型及"太空驿站"物流概念。
                        </p>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">轨道运输</span>
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">月球资源</span>
                            <span class="bg-[#DAA520]/10 text-[#DAA520]/90 px-3 py-1 rounded-full text-sm">太空驿站</span>
                        </div>
                        <button
                            class="flex items-center text-[#DAA520] hover:text-[#DAA520]/80 cursor-pointer !rounded-button whitespace-nowrap">
                            了解更多
                            <el-icon class="ml-1">
                                <ArrowRight />
                            </el-icon>
                        </button>
                    </div>
                </div>
                <div class="mt-16 text-center">
                    <button
                        class="bg-transparent border border-[#DAA520] text-[#DAA520] px-6 py-3 rounded-md font-medium hover:bg-[#DAA520]/10 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                        查看所有业务
                    </button>
                </div>
            </div>
        </section>
        <!-- 文化驱动 -->
        <section id="culture" class="py-16 bg-[#0F2235]">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="text-[#DAA520]">文化</span>驱动
                    </h2>
                    <p class="text-white/80 max-w-3xl mx-auto">
                        Cinastan
                        文脉，传承古代丝绸之路的文化精髓，融合现代科技与古老智慧，创造跨越时空的文化价值。
                    </p>
                </div>
                <div class="flex flex-col md:flex-row gap-8">
                    <div class="md:w-1/2">
                        <div class="bg-[#1B3B5A]/50 border border-[#DAA520]/10 rounded-xl overflow-hidden h-full">
                            <div class="h-72 overflow-hidden">
                                <img src="/img_4.jpg" alt="文化展览" class="w-full h-full object-cover object-top" />
                            </div>
                            <div class="p-6">
                                <h3 class="text-xl font-bold mb-4">数字文化藏品</h3>
                                <p class="text-white/70 mb-6">
                                    探索我们精心策划的古代丝绸之路文物数字藏品，通过3D技术重现历史瑰宝，让文化遗产焕发新生。
                                </p>
                                <div class="flex flex-wrap gap-3 mb-4">
                                    <div
                                        class="bg-[#1B3B5A] border border-[#DAA520]/20 rounded-lg p-4 flex-1 min-w-[120px]">
                                        <div class="text-[#DAA520] text-2xl font-bold mb-1">
                                            50+
                                        </div>
                                        <div class="text-white/70 text-sm">3D文物模型</div>
                                    </div>
                                    <div
                                        class="bg-[#1B3B5A] border border-[#DAA520]/20 rounded-lg p-4 flex-1 min-w-[120px]">
                                        <div class="text-[#DAA520] text-2xl font-bold mb-1">12</div>
                                        <div class="text-white/70 text-sm">合作博物馆</div>
                                    </div>
                                    <div
                                        class="bg-[#1B3B5A] border border-[#DAA520]/20 rounded-lg p-4 flex-1 min-w-[120px]">
                                        <div class="text-[#DAA520] text-2xl font-bold mb-1">5</div>
                                        <div class="text-white/70 text-sm">巡展国家</div>
                                    </div>
                                </div>
                                <button
                                    class="text-[#DAA520] hover:text-[#DAA520]/80 flex items-center cursor-pointer !rounded-button whitespace-nowrap">
                                    探索数字藏品
                                    <el-icon class="ml-1">
                                        <ArrowRight />
                                    </el-icon>
                                </button>
                            </div>
                        </div>
                    </div>
                    <div class="md:w-1/2">
                        <div class="bg-[#1B3B5A]/50 border border-[#DAA520]/10 rounded-xl p-6 mb-8">
                            <h3 class="text-xl font-bold mb-4">丝路时间轴</h3>
                            <div class="relative">
                                <div class="absolute left-4 top-0 bottom-0 w-0.5 bg-[#DAA520]/30"></div>
                                <div class="space-y-6">
                                    <div class="flex">
                                        <div class="relative z-10">
                                            <div
                                                class="w-8 h-8 rounded-full bg-[#DAA520] flex items-center justify-center text-[#1B3B5A] font-bold">
                                                秦汉
                                            </div>
                                        </div>
                                        <div class="ml-6">
                                            <h4 class="font-bold">秦汉时代</h4>
                                            <p class="text-white/70">
                                                丝绸之路的起源，张骞出使西域，开辟东西方贸易初期路线。
                                            </p>
                                        </div>
                                    </div>
                                    <div class="flex">
                                        <div class="relative z-10">
                                            <div
                                                class="w-8 h-8 rounded-full bg-[#DAA520] flex items-center justify-center text-[#1B3B5A] font-bold">
                                                隋唐
                                            </div>
                                        </div>
                                        <div class="ml-6">
                                            <h4 class="font-bold">隋唐时代</h4>
                                            <p class="text-white/70">
                                                丝绸之路的黄金时代，长安成为世界最大的国际化都市之一。
                                            </p>
                                        </div>
                                    </div>
                                    <div class="flex">
                                        <div class="relative z-10">
                                            <div
                                                class="w-8 h-8 rounded-full bg-[#DAA520] flex items-center justify-center text-[#1B3B5A] font-bold">
                                                宋元
                                            </div>
                                        </div>
                                        <div class="ml-6">
                                            <h4 class="font-bold">宋元时代</h4>
                                            <p class="text-white/70">
                                                蒙古帝国时期，丝绸之路全线贯通，马可·波罗东游中国。
                                            </p>
                                        </div>
                                    </div>
                                    <div class="flex">
                                        <div class="relative z-10">
                                            <div
                                                class="w-8 h-8 rounded-full bg-[#DAA520] flex items-center justify-center text-[#1B3B5A] font-bold">
                                                今
                                            </div>
                                        </div>
                                        <div class="ml-6">
                                            <h4 class="font-bold">现代 (21世纪)</h4>
                                            <p class="text-white/70">
                                                一带一路倡议，重启丝绸之路经济带，推动全球互联互通。
                                            </p>
                                        </div>
                                    </div>
                                    <div class="flex">
                                        <div class="relative z-10">
                                            <div
                                                class="w-8 h-8 rounded-full bg-[#1B3B5A] border-2 border-[#DAA520] flex items-center justify-center text-[#DAA520] font-bold">
                                                未
                                            </div>
                                        </div>
                                        <div class="ml-6">
                                            <h4 class="font-bold">未来 (2030+)</h4>
                                            <p class="text-white/70">
                                                太空丝路构想，拓展人类文明的贸易边界至太空。
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="bg-[#1B3B5A]/50 border border-[#DAA520]/10 rounded-xl p-6">
                            <div class="flex items-center mb-4">
                                <el-icon class="text-[#DAA520] mr-2" size="20">
                                    <Connection />
                                </el-icon>
                                <h3 class="text-xl font-bold">"文化加贸易"项目</h3>
                            </div>
                            <p class="text-white/70 mb-4">
                                将文化价值与商业贸易相结合，通过现代科技赋能传统文化产品。
                            </p>
                            <div class="space-y-4">
                                <div class="flex items-center p-3 bg-[#1B3B5A] rounded-lg">
                                    <el-icon class="text-[#DAA520] mr-3" size="24">
                                        <Picture />
                                    </el-icon>
                                    <div>
                                        <div class="font-medium">波斯手工地毯 + AR签名芯片溯源</div>
                                        <div class="text-sm text-white/60">
                                            通过AR技术了解地毯制作工艺与历史
                                        </div>
                                    </div>
                                </div>
                                <div class="flex items-center p-3 bg-[#1B3B5A] rounded-lg">
                                    <el-icon class="text-[#DAA520] mr-3" size="24">
                                        <Goods />
                                    </el-icon>
                                    <div>
                                        <div class="font-medium">海上陶瓷 + 区块链防伪证明系统</div>
                                        <div class="text-sm text-white/60">
                                            确保每件陶瓷艺术品的真实性与唯一性
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- 合作与投资 -->
        <section id="partners" class="py-16 bg-[#1B3B5A] relative overflow-hidden">
            <div class="absolute inset-0 opacity-5" style="
          background-image: url(&quot;/img_2.jpg&quot;);
          background-size: cover;
        "></div>
            <div class="container mx-auto px-6 relative z-10">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="text-[#DAA520]">合作</span>与投资
                    </h2>
                    <p class="text-white/80 max-w-3xl mx-auto">
                        与全球领先企业共同构建新丝路生态系统，创造跨越文化与地域的商业价值。
                    </p>
                </div>
                <div class="mb-16">
                    <h3 class="text-xl font-bold mb-6 flex items-center">
                        <el-icon class="text-[#DAA520] mr-2">
                            <Coordinate />
                        </el-icon>
                        全球战略合作伙伴
                    </h3>
                    <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6">
                        <div v-for="(partner, index) in partners" :key="index"
                            class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-lg p-4 flex flex-col items-center justify-center hover:border-[#DAA520]/30 transition-colors">
                            <el-icon :class="partner.iconClass" size="36">
                                <component :is="partner.icon" />
                            </el-icon>
                            <div class="mt-3 text-center">
                                <div class="font-medium">{{ partner.name }}</div>
                                <div class="text-xs text-white/60">{{ partner.location }}</div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-xl p-6">
                        <el-icon class="text-[#DAA520] mb-4" size="32">
                            <Document />
                        </el-icon>
                        <h3 class="text-xl font-bold mb-3">投资者通道</h3>
                        <p class="text-white/70 mb-6">
                            获取最新财务报告、发展规划与投资机会。
                        </p>
                        <div class="space-y-3">
                            <a href="#"
                                class="flex items-center p-3 bg-[#1B3B5A] rounded-lg hover:bg-[#1B3B5A]/80 transition-colors cursor-pointer">
                                <el-icon class="text-[#DAA520] mr-3">
                                    <Document />
                                </el-icon>
                                <span>2025年第二季度财务报告</span>
                            </a>
                            <a href="#"
                                class="flex items-center p-3 bg-[#1B3B5A] rounded-lg hover:bg-[#1B3B5A]/80 transition-colors cursor-pointer">
                                <el-icon class="text-[#DAA520] mr-3">
                                    <Document />
                                </el-icon>
                                <span>五年发展战略规划</span>
                            </a>
                            <a href="#"
                                class="flex items-center p-3 bg-[#1B3B5A] rounded-lg hover:bg-[#1B3B5A]/80 transition-colors cursor-pointer">
                                <el-icon class="text-[#DAA520] mr-3">
                                    <Document />
                                </el-icon>
                                <span>海外市场拓展计划</span>
                            </a>
                        </div>
                    </div>
                    <div class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-xl p-6">
                        <el-icon class="text-[#DAA520] mb-4" size="32">
                            <TrendCharts />
                        </el-icon>
                        <h3 class="text-xl font-bold mb-3">业务增长数据</h3>
                        <p class="text-white/70 mb-6">
                            Cinastan 三大业务板块近年增长趋势。
                        </p>
                        <div ref="growthChart" class="h-60"></div>
                    </div>
                    <div class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-xl p-6">
                        <el-icon class="text-[#DAA520] mb-4" size="32">
                            <Opportunity />
                        </el-icon>
                        <h3 class="text-xl font-bold mb-3">创新贸易技术</h3>
                        <p class="text-white/70 mb-6">引领行业的前沿技术应用。</p>
                        <div class="space-y-4">
                            <div class="flex items-start">
                                <div class="bg-[#DAA520]/20 p-2 rounded-lg mr-3">
                                    <el-icon class="text-[#DAA520]" size="20">
                                        <DataAnalysis />
                                    </el-icon>
                                </div>
                                <div>
                                    <div class="font-medium mb-1">AI预测供应链</div>
                                    <div class="text-sm text-white/60">
                                        利用人工智能预测市场需求与供应变化，优化库存管理。
                                    </div>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="bg-[#DAA520]/20 p-2 rounded-lg mr-3">
                                    <el-icon class="text-[#DAA520]" size="20">
                                        <Histogram />
                                    </el-icon>
                                </div>
                                <div>
                                    <div class="font-medium mb-1">区块链溯源系统</div>
                                    <div class="text-sm text-white/60">
                                        为高价值商品提供全链路溯源，确保真实性与质量。
                                    </div>
                                </div>
                            </div>
                            <div class="flex items-start">
                                <div class="bg-[#DAA520]/20 p-2 rounded-lg mr-3">
                                    <el-icon class="text-[#DAA520]" size="20">
                                        <Sunny />
                                    </el-icon>
                                </div>
                                <div>
                                    <div class="font-medium mb-1">碳中和物流路线</div>
                                    <div class="text-sm text-white/60">
                                        优化运输路线与方式，减少碳排放，实现绿色丝路。
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- 企业纪录片预告 -->
        <section class="py-16 bg-[#0F2235]">
            <div class="container mx-auto px-6">
                <div class="text-center mb-10">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="text-[#DAA520]">企业</span>纪录片预告
                    </h2>
                    <p class="text-white/80 max-w-3xl mx-auto">
                        《Cinastan：丝路的重启》——探索我们如何连接古今，重塑丝路精神。
                    </p>
                </div>
                <div class="relative rounded-xl overflow-hidden cursor-pointer group" @click="playVideo">
                    <div
                        class="absolute inset-0 bg-black/40 group-hover:bg-black/20 transition-colors z-10 flex items-center justify-center">
                        <div
                            class="w-20 h-20 rounded-full bg-[#DAA520]/90 flex items-center justify-center group-hover:scale-110 transition-transform">
                            <el-icon class="text-[#1B3B5A]" size="32">
                                <VideoPlay />
                            </el-icon>
                        </div>
                    </div>
                    <img src="/img_8.jpg" alt="企业纪录片预告" class="w-full h-[500px] object-cover object-top" />
                </div>
            </div>
        </section>
        <!-- 人才招聘 -->
        <section id="join" class="py-16 bg-[#1B3B5A] relative overflow-hidden">
            <div class="absolute inset-0 opacity-5" style="
          background-image: url(&quot;/img_14.jpg&quot;);
          background-size: cover;
        "></div>
            <div class="container mx-auto px-6 relative z-10">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="text-[#DAA520]">加入</span>Cinastan
                    </h2>
                    <p class="text-white/80 max-w-3xl mx-auto">
                        "我们招募的不只是员工，而是历史的合作者。"成为丝路新纪元的缔造者。
                    </p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <div v-for="(job, index) in jobs" :key="index"
                        class="bg-[#0F2235]/80 border border-[#DAA520]/10 rounded-xl p-6 hover:border-[#DAA520]/30 transition-colors">
                        <div class="flex justify-between items-start mb-4">
                            <div>
                                <h3 class="text-xl font-bold mb-1">{{ job.title }}</h3>
                                <div class="text-white/60 text-sm">{{ job.location }}</div>
                            </div>
                            <span
                                :class="`bg-${job.tagColor}/20 text-${job.tagColor} px-3 py-1 rounded-full text-sm`">{{
                                job.tag }}</span>
                        </div>
                        <p class="text-white/70 mb-4">{{ job.description }}</p>
                        <div class="flex flex-wrap gap-2 mb-6">
                            <span v-for="(skill, skillIndex) in job.skills" :key="skillIndex"
                                class="bg-[#1B3B5A] text-white/80 px-3 py-1 rounded-full text-sm">{{ skill }}</span>
                        </div>
                        <div class="flex justify-between items-center">
                            <div class="text-[#DAA520] font-medium">{{ job.salary }}</div>
                            <button
                                class="bg-[#DAA520] text-[#1B3B5A] px-4 py-2 rounded-md font-medium hover:bg-[#DAA520]/90 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                                申请职位
                            </button>
                        </div>
                    </div>
                </div>
                <div class="mt-16 text-center">
                    <button
                        class="bg-transparent border border-[#DAA520] text-[#DAA520] px-6 py-3 rounded-md font-medium hover:bg-[#DAA520]/10 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                        查看所有职位
                    </button>
                </div>
            </div>
        </section>
        <!-- 技术与可持续 -->
        <section id="tech" class="py-16 bg-[#0F2235]">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">
                        <span class="text-[#DAA520]">技术</span>与可持续
                    </h2>
                    <p class="text-white/80 max-w-3xl mx-auto">
                        通过前沿技术推动贸易可持续发展，打造绿色丝路。
                    </p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-16">
                    <div class="bg-[#1B3B5A]/50 border border-[#DAA520]/10 rounded-xl overflow-hidden">
                        <div class="h-64 overflow-hidden">
                            <img src="/img_3.jpg" alt="智能调度系统" class="w-full h-full object-cover object-top" />
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-3">智能调度系统</h3>
                            <p class="text-white/70 mb-6">
                                利用人工智能技术优化陆海空三线物流调度，实现资源最优配置与效率最大化。
                            </p>
                            <div class="grid grid-cols-2 gap-4 mb-6">
                                <div class="bg-[#0F2235] p-4 rounded-lg">
                                    <div class="text-[#DAA520] font-bold text-lg mb-1">32%</div>
                                    <div class="text-sm text-white/70">运输时间缩短</div>
                                </div>
                                <div class="bg-[#0F2235] p-4 rounded-lg">
                                    <div class="text-[#DAA520] font-bold text-lg mb-1">45%</div>
                                    <div class="text-sm text-white/70">成本节约</div>
                                </div>
                                <div class="bg-[#0F2235] p-4 rounded-lg">
                                    <div class="text-[#DAA520] font-bold text-lg mb-1">99.8%</div>
                                    <div class="text-sm text-white/70">准时交付率</div>
                                </div>
                                <div class="bg-[#0F2235] p-4 rounded-lg">
                                    <div class="text-[#DAA520] font-bold text-lg mb-1">28%</div>
                                    <div class="text-sm text-white/70">碳排放减少</div>
                                </div>
                            </div>
                            <button
                                class="text-[#DAA520] hover:text-[#DAA520]/80 flex items-center cursor-pointer !rounded-button whitespace-nowrap">
                                了解技术细节
                                <el-icon class="ml-1">
                                    <ArrowRight />
                                </el-icon>
                            </button>
                        </div>
                    </div>
                    <div class="bg-[#1B3B5A]/50 border border-[#DAA520]/10 rounded-xl overflow-hidden">
                        <div class="h-64 overflow-hidden">
                            <img src="/img_10.jpg" alt="绿色丝路倡议" class="w-full h-full object-cover object-top" />
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold mb-3">绿色丝路倡议</h3>
                            <p class="text-white/70 mb-6">
                                打造碳中和物流路线，推动可持续贸易发展，保护沿线生态环境。
                            </p>
                            <div class="space-y-4 mb-6">
                                <div class="flex items-center bg-[#0F2235] p-3 rounded-lg">
                                    <el-icon class="text-[#DAA520] mr-3" size="24">
                                        <Sunny />
                                    </el-icon>
                                    <div>
                                        <div class="font-medium">可再生能源驱动</div>
                                        <div class="text-sm text-white/60">
                                            物流中心100%使用太阳能与风能
                                        </div>
                                    </div>
                                </div>
                                <div class="flex items-center bg-[#0F2235] p-3 rounded-lg">
                                    <el-icon class="text-[#DAA520] mr-3" size="24">
                                        <Van />
                                    </el-icon>
                                    <div>
                                        <div class="font-medium">电动运输车队</div>
                                        <div class="text-sm text-white/60">
                                            陆路运输全面电气化转型
                                        </div>
                                    </div>
                                </div>
                                <div class="flex items-center bg-[#0F2235] p-3 rounded-lg">
                                    <el-icon class="text-[#DAA520] mr-3" size="24">
                                        <Refresh />
                                    </el-icon>
                                    <div>
                                        <div class="font-medium">循环包装系统</div>
                                        <div class="text-sm text-white/60">
                                            可重复使用的环保包装解决方案
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <button
                                class="text-[#DAA520] hover:text-[#DAA520]/80 flex items-center cursor-pointer !rounded-button whitespace-nowrap">
                                了解可持续计划
                                <el-icon class="ml-1">
                                    <ArrowRight />
                                </el-icon>
                            </button>
                        </div>
                    </div>
                </div>
                <div class="bg-[#1B3B5A]/50 border border-[#DAA520]/10 rounded-xl p-6">
                    <h3 class="text-xl font-bold mb-6 flex items-center">
                        <el-icon class="text-[#DAA520] mr-2">
                            <GoodsFilled />
                        </el-icon>
                        ESG 责任
                    </h3>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                        <div class="bg-[#0F2235] p-4 rounded-lg">
                            <el-icon class="text-[#DAA520] mb-3" :size="28">
                                <School />
                            </el-icon>
                            <h4 class="font-bold mb-2">教育支持</h4>
                            <p class="text-white/70 text-sm">
                                在丝路沿线国家建立12所职业学校，培养当地物流与贸易人才。
                            </p>
                        </div>
                        <div class="bg-[#0F2235] p-4 rounded-lg">
                            <el-icon class="text-[#DAA520] mb-3" size="28">
                                <OfficeBuilding />
                            </el-icon>
                            <h4 class="font-bold mb-2">文化保护</h4>
                            <p class="text-white/70 text-sm">
                                资助8个古代丝路遗址的保护与修复工作，传承历史文化遗产。
                            </p>
                        </div>
                        <div class="bg-[#0F2235] p-4 rounded-lg">
                            <el-icon class="text-[#DAA520] mb-3" size="28">
                                <Coin />
                            </el-icon>
                            <h4 class="font-bold mb-2">经济赋能</h4>
                            <p class="text-white/70 text-sm">
                                扶持沿线小型生产商与手工艺人，帮助其产品进入国际市场。
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- 页脚 -->
        <footer class="bg-[#0A1825] pt-16 pb-8">
            <div class="container mx-auto px-6">
                <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
                    <div>
                        <div class="flex items-center mb-6">
                            <div class="text-[#DAA520] font-bold text-2xl mr-2">Cinastan</div>
                            <div class="text-white/80 text-sm">秦尼斯坦</div>
                        </div>
                        <p class="text-white/60 mb-6">
                            连接过去与未来的全球丝路贸易核心节点企业，在"陆海空（太空）三线融合"的大格局中重塑丝路精神。
                        </p>
                        <div class="flex space-x-4">

                            <a href="#" class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">
                                <el-icon size="20">
                                    <ChatDotRound />
                                </el-icon>
                            </a>
                            <a href="#" class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">
                                <el-icon size="20">
                                    <Connection />
                                </el-icon>
                            </a>
                            <a href="#" class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">
                                <el-icon size="20">
                                    <Message />
                                </el-icon>
                            </a>
                        </div>
                    </div>
                    <div>
                        <h4 class="text-white font-bold mb-6">业务版块</h4>
                        <ul class="space-y-3">
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">陆上丝绸之路</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">海上丝绸之路</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">太空丝绸之路</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">跨境保税仓网络</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">特色商品集采</a>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h4 class="text-white font-bold mb-6">关于我们</h4>
                        <ul class="space-y-3">
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">公司简介</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">品牌理念</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">管理团队</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">企业责任</a>
                            </li>
                            <li>
                                <a href="#"
                                    class="text-white/60 hover:text-[#DAA520] transition-colors cursor-pointer">新闻中心</a>
                            </li>
                        </ul>
                    </div>
                    <div>
                        <h4 class="text-white font-bold mb-6">联系我们</h4>
                        <ul class="space-y-3">
                            <li class="flex items-start">
                                <el-icon class="text-[#DAA520] mr-2 mt-1">
                                    <Location />
                                </el-icon>
                                <span class="text-white/60">长安市大汉新区贸易大厦</span>
                            </li>
                            <li class="flex items-center">
                                <el-icon class="text-[#DAA520] mr-2">
                                    <Phone />
                                </el-icon>
                                <span class="text-white/60">+86 10 8888 7777</span>
                            </li>
                            <li class="flex items-center">
                                <el-icon class="text-[#DAA520] mr-2">
                                    <Message />
                                </el-icon>
                                <span class="text-white/60">contact@cinastan.com</span>
                            </li>
                        </ul>
                        <div class="mt-6">
                            <button
                                class="bg-[#DAA520] text-[#1B3B5A] px-4 py-2 rounded-md font-medium hover:bg-[#DAA520]/90 transition-colors cursor-pointer !rounded-button whitespace-nowrap">
                                订阅通讯
                            </button>
                        </div>
                    </div>
                </div>
                <div class="border-t border-white/10 pt-8 flex flex-col md:flex-row justify-between items-center">
                    <div class="text-white/50 text-sm mb-4 md:mb-0">
                        © 2025 Cinastan 秦尼斯坦. 保留所有权利。
                    </div>
                    <div class="flex space-x-6">
                        <a href="#"
                            class="text-white/50 text-sm hover:text-[#DAA520] transition-colors cursor-pointer">隐私政策</a>
                        <a href="#"
                            class="text-white/50 text-sm hover:text-[#DAA520] transition-colors cursor-pointer">服务条款</a>
                        <a href="#"
                            class="text-white/50 text-sm hover:text-[#DAA520] transition-colors cursor-pointer">Cookie
                            政策</a>
                        <a href="#"
                            class="text-white/50 text-sm hover:text-[#DAA520] transition-colors cursor-pointer">网站地图</a>
                    </div>
                </div>
            </div>
        </footer>
        <!-- 视频播放弹窗 -->
    </div>
</template>
<script lang="ts" setup>
import { ref, onMounted, nextTick } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Pagination, Autoplay } from "swiper/modules";
// @ts-ignore
import "swiper/css";
// @ts-ignore
import "swiper/css/navigation";
// @ts-ignore
import "swiper/css/pagination";
// @ts-ignore
import * as echarts from "echarts";
import {
    ArrowDown,
    ArrowLeft,
    ArrowRight,
    Menu,
    Location,
    Ship,
    Star,
    Connection,
    Picture,
    Goods,
    Coordinate,
    Document,
    TrendCharts,
    Opportunity,
    DataAnalysis,
    Histogram,
    Sunny,
    VideoPlay,
    GoodsFilled,
    School,
    OfficeBuilding,
    Coin,
    ChatDotRound,
    Message,
    Phone,
    Refresh,
    Van
} from "@element-plus/icons-vue";
const swiperModules = [Pagination, Autoplay];
const swiperBreakpoints = {
    640: {
        slidesPerView: 1,
        spaceBetween: 20
    },
    768: {
        slidesPerView: 1,
        spaceBetween: 30
    },
    1024: {
        slidesPerView: 1,
        spaceBetween: 30
    }
};
const mobileMenuOpen = ref(false);
const videoDialogVisible = ref(false);
const growthChart = ref<HTMLElement | null>(null);
const swiperInstance = ref(null);
const toggleMobileMenu = () => {
    mobileMenuOpen.value = !mobileMenuOpen.value;
};
const playVideo = () => {
    videoDialogVisible.value = true;
};
const onSwiperInit = (swiper: any) => {
    swiperInstance.value = swiper;
};
const newsItems = [
    {
        title: "Cinastan 集团与哈萨克斯坦签署能源物流合作协议",
        content:
            "近日，Cinastan 秦尼斯坦 与哈萨克斯坦能源部签署了为期十年的能源物流合作协议。根据协议，双方将共同建设连接中亚油气资源与中国市场的智能物流通道，预计年处理能力将达到 5000 万吨。",
        category: "陆上丝路",
        date: "2025-06-01",
        image: "/img_11.jpg"
    },
    {
        title: "马六甲智能港口项目正式投入运营，效率提升40%",
        content:
            "由 Cinastan 秦尼斯坦 投资建设的马六甲智能港口项目于上周正式投入运营。该项目采用全球领先的 AI 调度系统与自动化装卸设备，使港口作业效率提升40%，成为海上丝绸之路的重要枢纽。",
        category: "海上丝路",
        date: "2025-05-25",
        image: "/img_5.jpg"
    },
    {
        title: "太空物资运输试验成功，月球资源开发迈出关键一步",
        content:
            "Cinastan 太空部门与中国航天科技集团合作的首次太空物资运输试验取得成功。此次试验验证了轨道间物资转运技术，为未来月球资源开发奠定了技术基础。",
        category: "太空丝路",
        date: "2025-05-18",
        image: "/img_0.jpg"
    }
];
const partners = [
    {
        name: "中国石油",
        location: "中国",
        icon: "OfficeBuilding",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "哈萨克能源",
        location: "哈萨克斯坦",
        icon: "Sunny",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "马士基航运",
        location: "丹麦",
        icon: "Ship",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "迪拜港口",
        location: "阿联酋",
        icon: "Ship",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "太空探索技术",
        location: "美国",
        icon: "Star",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "伊朗贸易",
        location: "伊朗",
        icon: "Goods",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "土耳其物流",
        location: "土耳其",
        icon: "Van",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "意大利商会",
        location: "意大利",
        icon: "OfficeBuilding",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "俄罗斯铁路",
        location: "俄罗斯",
        icon: "Van",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "新加坡航运",
        location: "新加坡",
        icon: "Ship",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "中亚矿业",
        location: "乌兹别克斯坦",
        icon: "Coin",
        iconClass: "text-[#DAA520]"
    },
    {
        name: "德国科技",
        location: "德国",
        icon: "DataAnalysis",
        iconClass: "text-[#DAA520]"
    }
];
const jobs = [
    {
        title: "国际贸易官员",
        location: "北京 / 迪拜",
        tag: "全职",
        tagColor: "[#DAA520]",
        description:
            "负责中东和中亚地区的贸易关系发展，协调跨国贸易项目，分析市场趋势。",
        skills: ["国际贸易", "阿拉伯语/波斯语", "谈判技巧", "市场分析"],
        salary: "¥30K-45K/月"
    },
    {
        title: "中亚事务专员",
        location: "乌鲁木齐 / 阿拉木图",
        tag: "全职",
        tagColor: "[#DAA520]",
        description:
            "负责中亚五国的业务拓展，维护与当地政府和企业的关系，推动能源与矿产贸易。",
        skills: ["俄语/哈萨克语", "能源行业", "政府关系", "项目管理"],
        salary: "¥25K-40K/月"
    },
    {
        title: "宇航工程商业顾问",
        location: "北京 / 远程",
        tag: "兼职",
        tagColor: "[#DAA520]",
        description:
            "为公司太空丝路项目提供技术咨询，评估商业可行性，制定太空资源开发战略。",
        skills: ["航天工程", "商业分析", "资源评估", "战略规划"],
        salary: "项目制"
    }
];
onMounted(() => {
    nextTick(() => {
        if (growthChart.value) {
            const chart = echarts.init(growthChart.value);
            const option = {
                animation: false,
                color: ["#DAA520", "#1E90FF", "#9370DB"],
                tooltip: {
                    trigger: "axis",
                    backgroundColor: "#1B3B5A",
                    borderColor: "#DAA520",
                    textStyle: {
                        color: "#fff"
                    }
                },
                legend: {
                    data: ["陆上丝路", "海上丝路", "太空丝路"],
                    textStyle: {
                        color: "#fff"
                    },
                    right: 0
                },
                grid: {
                    left: "3%",
                    right: "4%",
                    bottom: "3%",
                    containLabel: true
                },
                xAxis: {
                    type: "category",
                    boundaryGap: false,
                    data: ["2021", "2022", "2023", "2024", "2025"],
                    axisLine: {
                        lineStyle: {
                            color: "#ffffff30"
                        }
                    },
                    axisLabel: {
                        color: "#ffffff80"
                    }
                },
                yAxis: {
                    type: "value",
                    axisLine: {
                        lineStyle: {
                            color: "#ffffff30"
                        }
                    },
                    splitLine: {
                        lineStyle: {
                            color: "#ffffff10"
                        }
                    },
                    axisLabel: {
                        color: "#ffffff80"
                    }
                },
                series: [
                    {
                        name: "陆上丝路",
                        type: "line",
                        smooth: true,
                        data: [120, 132, 145, 160, 178]
                    },
                    {
                        name: "海上丝路",
                        type: "line",
                        smooth: true,
                        data: [150, 170, 195, 210, 250]
                    },
                    {
                        name: "太空丝路",
                        type: "line",
                        smooth: true,
                        data: [10, 15, 25, 40, 65]
                    }
                ]
            };
            chart.setOption(option);
            window.addEventListener("resize", () => {
                chart.resize();
            });
        }
    });
});
</script>
<style scoped>
@import url("/img_6.jpg");

:root {
    --primary-color: #1b3b5a;
    --accent-color: #daa520;
    --dark-color: #0f2235;
    --darker-color: #0a1825;
}

body {
    font-family:
        "Noto Serif SC",
        serif,
        -apple-system,
        BlinkMacSystemFont,
        "Segoe UI",
        Roboto,
        Helvetica,
        Arial,
        sans-serif;
    min-height: 1024px;
}

.news-swiper {
    width: 100%;
    height: 100%;
    margin-left: auto;
    margin-right: auto;
}

.news-swiper :deep(.swiper-pagination-bullet) {
    background: rgba(218, 165, 32, 0.5);
}

.news-swiper :deep(.swiper-pagination-bullet-active) {
    background: #daa520;
}

.video-dialog :deep(.el-dialog__header) {
    display: none;
}

.video-dialog :deep(.el-dialog__body) {
    padding: 0;
}

.aspect-w-16 {
    position: relative;
    padding-bottom: 56.25%;
}

.aspect-w-16>* {
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
    -webkit-appearance: none;
    margin: 0;
}
</style>
