<template>
    <main class="flex justify-center py-16 px-6 md:px-12 lg:px-16 rounded-[40px]">
        <div class="max-w-[95rem] w-full flex flex-col lg:flex-row items-center gap-16 text-white">
            <!-- Left: Image Section -->
            <div class="lg:w-[50%]">
                <img src="../../assets/images/valueUserImg.png" alt="Value Image" class="rounded-xl xl:max-w-[566px]">
            </div>

            <!-- Right: Values List -->
            <div class="w-full lg:w-[50%]">
                <!-- Title -->
                <div class="inline-flex mb-8 items-center px-4 py-2 bg-white text-[#1E3A5F] rounded-full text-xs font-medium">
                    OUR VALUES
                </div>

                <!-- Value Items -->
                <div v-for="(value, index) in values" :key="index" 
                    class="flex items-start gap-4 cursor-pointer"
                >
                    
                    <div class="w-[60px] flex items-center justify-center">
                        <img :src="value.image" alt="">
                    </div>

                    <!-- Text Content -->
                    <div class="z-10">
                        <h3 class="text-lg text-[#DFF4FD]">{{ value.title }}</h3>
                        <p class="text-sm text-[#DFF4FDCC] leading-relaxed">{{ value.description }}</p>
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script setup>
import { ref } from 'vue';
import excellenceIcon from '../../assets/images/excellenceIcon.png';
import integrityIcon from '../../assets/images/integrityIcon.png';
import innovationIcon from '../../assets/images/innovationIcon.png';
import collaborationIcon from '../../assets/images/collaborationIcon.png';
import sustainabilityIcon from '../../assets/images/sustainabilityIcon.png';


const values = ref([
    {
        title: "Excellence",
        description: "We are committed to delivering the highest standards of quality in every product we manufacture and every service we provide.",
        image: excellenceIcon
    },
    {
        title: "Integrity",
        description: "We operate with honesty, transparency, and accountability, building trust with our partners and stakeholders.",
        image: integrityIcon
    },
    {
        title: "Innovation",
        description: "We embrace cutting-edge technologies and processes to improve efficiency, quality, and accessibility in healthcare.",
        image: innovationIcon
    },
    {
        title: "Collaboration",
        description: "We work closely with wholesalers, distributors, and healthcare providers to ensure seamless delivery of medications to patients.",
        image: collaborationIcon
    },
    {
        title: "Sustainability",
        description: "We are dedicated to creating a positive impact on society by promoting affordable healthcare and supporting local communities.",
        image: sustainabilityIcon
    }
]);

const currentIndex = ref(0);
</script>

<style scoped>
main {
    position: relative;
    background-image: url("../../assets/images/sectionBgImg.png");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

main::before {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(180deg, rgba(0, 38, 63, 0) 0%, #00263F 100%);
    z-index: 1;
    pointer-events: none;
    border-bottom-left-radius: 40px;
    border-bottom-right-radius: 40px;
}
</style>