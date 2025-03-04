<template class="bg-black">
    <title>I am what i am // invitación</title>
    <div class="flex flex-col text-center p-5 sofia bg-[#24032B]">
        <div class="md:w-[50%] pt-20 w-[90%] mx-auto  gap-[2rem] flex flex-col">
            <h1 ref="neonText" class="neon-pink slab whitespace-nowrap">I AM WHAT I AM</h1>
            <div class="flex flex-col gap-[1.1rem] text-white">
                <p class="text-[#EA52EA] uppercase">
                    Sabado 5 de Abril en
                    Sissy Bag <br> C. de Pelayo, 42, Centro, 28004 Madrid
                    <br> 21:00
                </p>
                    <iframe class="mt-8" width="100%" height="315" src="https://www.youtube.com/embed/jdlvWIJlI50?si=RmhX8Fr1M8oOPHn2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
                <div class="flex mx-auto mt-20 mb-14">
                    <PhArrowFatDown ref="neonArr" class="arrow-pink" :size="128" />
                </div>

   
                <p class="mt-8">
                    Estás invitade a la fiesta de la expresión y la purísima identidad
                    Ven con tu look más único y personal, no quiero que seas extra si no es lo
                    tuyo, quiero que seas TÚ.<br>
                    Todo lo excéntrico, extravagante, raro, maniático, estrafalario, curioso,
                    atípico y extraordinario es bienvenido. <br>
                    Tienes toda la libertad de expresarte como quieras, en una performance, una
                    canción, un cuadro, una escultura... házmelo saber para poder organizar el
                    orden. <br>
                    Por ende, habrá todo tipo de shows del resto de artistas y música vibrante
                    que te hará querer darlo todo. <br>
                    Es una fiesta de libertad, NO ES UNA COMPETICIÓN ¡¡¡Se exige disfrute,
                    respeto y amor al resto de artistas y mucho coño!!!
                </p>
                <h2 ref="neonText2" class="neon-pink mt-6 mb-8 slab">
                    A DARLO TODO P00TAS
                </h2>
            </div>
        </div>
    </div>
</template>


<script setup>
import { ref, onMounted } from 'vue'
import { gsap } from 'gsap'
import { PhArrowFatDown } from "@phosphor-icons/vue";

const neonText = ref(null)
const neonText2 = ref(null)
const neonArr = ref(null)

onMounted(() => {
    gsap.to(neonText.value, {
        duration: 1.5,
        textShadow: "0 0 10px #E046E0, 0 0 20px #E046E0",
        ease: "sine.inOut",
        yoyo: true,
        repeat: -1
    })
    gsap.to(neonText2.value, {
        duration: 1,
        textShadow: "0 0 10px #E046E0, 0 0 20px #E046E0",
        ease: "sine.inOut",
        yoyo: true,
        repeat: -1
    })
    gsap.to(neonArr.value, {
        duration: 1,
        filter: "drop-shadow(0 0 10px #00aa00), drop-shadow(0 0 20px #E046E0)",
        ease: "sine.inOut",
        yoyo: true,
        repeat: -1
    })
})
</script>

<style lang="sass" scoped>

    .neon-pink
      color: #F0D9F0
      text-shadow: 0 0 5px #ff77ff, 0 0 10px #ff77ff, 0 0 20px #ff77ff, 0 0 40px #ff77ff
    .arrow-pink
      color: #F0D9F0
      filter: drop-shadow(0 0 2px #ff77ff) drop-shadow(0 0 7px #ff77ff) drop-shadow(0 0 15px #ff77ff) drop-shadow(0 0 30px #ff77ff)
    p
        font-size: 20px
        font-weight: 200


h2
    font-size: 40px

h1
    font-size: 55px
    line-height: 40px
    font-weight: 400

@media (max-width: 500px) 
    *
        font-size: 10px

    h1 
        font-size: 45px
    
    h2
        font-size: 30px
    
    p
        font-size: 17px
        font-weight: 300
    

</style>
