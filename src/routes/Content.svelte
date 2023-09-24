<script>
   import kyoto_1 from '$lib/images/tianshu-liu-SBK40fdKbAg-unsplash.jpg';
   import kyoto_2 from '$lib/images/redd-f-wPMvPMD9KBI-unsplash.jpg';
   import kyoto_3 from '$lib/images/sorasak-_UIN-pFfJ7c-unsplash.jpg';

   import tokyo_1 from '$lib/images/yoav-aziz-tKCd-IWc4gI-unsplash.jpg';
   import tokyo_2 from '$lib/images/vista-wei-OiERUvVrioU-unsplash.jpg';
   
   import jpn_end from '$lib/images/rap-dela-rea-NgMqApxnf_8-unsplash.jpg';

   import {gsap} from 'gsap'; 
   import {ScrollTrigger} from 'gsap/dist/ScrollTrigger';
   import {onMount} from 'svelte';

   onMount(() => {
    gsap.registerPlugin(ScrollTrigger);

    gsap.from('#img1', {
        x: -700,
        duration: 1,
        scrollTrigger: {
            trigger: "#img1",
            start: "top 100%",
            end: "top 0",
            toggleActions: "restart none none reset",
        },
    })

    gsap.from('#img2', {
        y: 700,
        duration: 1,
        scrollTrigger: {
            trigger: "#img2",
            start: "top 100%",
            end: "top 20%",
            toggleActions: "restart none none reset",
        },
    })

    gsap.from('#img3', {
        x: 700,
        duration: 1,
        scrollTrigger: {
            trigger: "#img3",
            start: "top 100%",
            end: "top 20%",
            toggleActions: "restart none none reset",
        },
    })

    gsap.from('.collage1 div', {
        opacity: 0,
        duration: 3,
        scrollTrigger: {
            trigger: ".collage1 div",
            start: "top 100%",
            end: "top 20%",
            toggleActions: "restart none none reset",
        },
    })
   })
</script>

<div class="content">
    <div class="collage1">
        <img id="img1" src={kyoto_1} alt="kyoto1" />
        <img id="img2"src={kyoto_2} alt="kyoto2" />
        <img id="img3"src={kyoto_3} alt="kyoto3" />
        <div>EXPLORE KYOTO</div>
    </div>

    <div class="collage2">
        <img id="img4" src={tokyo_1} alt="tokyo1" />
        <img id="img5"src={tokyo_2} alt="tokyo2" />
        <div>LOST IN <br/> TOKYO</div>
    </div>

    <a href="/library" class="collage3">
        <img id="imgend" src={jpn_end} alt="ending greet" />
        <div>FIND<br/>YOURS<br/>NOW</div>
    </a>
</div>


<style>
    .content {
        height: 400vh;
        width: 100vw;
    }
    .collage1 {
        position: absolute;
        left: 0;
        top: 100vh;
    }

    .collage1 div {
        --width: 45vw;
        width: var(--width);
        text-align: center;
        position: relative;
        left: calc( (100vw - var(--width)) / 2);
        top: 77vh;

        font-size: 3rem;
        color: var(--color-text-white);
        letter-spacing: .5rem;
    }

    .collage2 {
        width: 100vw;
        height: 160vh;

        position: absolute;
        left: 0;
        top: 250vh;

        background-color: var(--color-theme-2);
    }

    .collage2 div {
        position: relative;
        top: 70vh;
        /* left: 50vw; */
        text-align: center;

        font-size: 3rem;
        color: var(--color-text-white);
        letter-spacing: .5rem;
    }

    .collage3 {
        width: 100vw;
        height: 100vh;

        position: absolute;
        top: 400vh;
        left: 0;
        cursor: pointer;
    }

    .collage3 div {
        position: relative;
        top: 35%;
        font-size: 6rem;
        color: var(--color-text-white);
        text-align: center;
        vertical-align: middle;
        opacity: 0;

        transition: 0.3s;
    }

    .collage3:hover div {
        opacity: 1;
    }

    #img1, 
    #img2, 
    #img3,
    #img4,
    #img5 {
        object-fit: contain;
        position: absolute;

    }

    #img1 {
        width: 50vw;
        left: 0;
        top: 30vh;
    }

    #img2 {
        width: 40vw;
        left: 50vw;
        top: 10vh;   
    }
    
    #img3 {
        width: 50vw;        
        left: 30vw;
        top: 80vh;
    }

    #img4 {
        left: 0;
        top: 20vh;
    }

    #img5 {
        left: 50vw;
        top: 25vh;

        filter:brightness(.8);
    }

    #img4,
    #img5 {
        width: 50vw;

        transition: 0.3s;
    }

    #img4:hover,
    #img5:hover {
        width: 55vw;
    }

    #img4:hover ~ #img5 {
        left: 55vw;
        width: 45vw;
    }

    #img4:has(#img5:hover) {
        width: 45vw;
    }

    #imgend {
        object-fit: cover;
        position: absolute;

        width: 100vw;
        height: 100vh;
        /*height: 100vh;
        top: 390vh;
        left: 0; */

        filter: none;
        transition: 0.3s;
    }

    .collage3:hover #imgend {
        filter: blur(4px);
        transform: scale(1.1, 1.1);
    }
</style>