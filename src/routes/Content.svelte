<script>
   import kyoto_1 from '$lib/images/tianshu-liu-SBK40fdKbAg-unsplash.jpg';
   import kyoto_2 from '$lib/images/redd-f-wPMvPMD9KBI-unsplash.jpg';
   import kyoto_3 from '$lib/images/sorasak-_UIN-pFfJ7c-unsplash.jpg';

   import tokyo_1 from '$lib/images/yoav-aziz-tKCd-IWc4gI-unsplash.jpg';
   import tokyo_2 from '$lib/images/vista-wei-OiERUvVrioU-unsplash.jpg';
   
</script>

<div>
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
</div>


<style>
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
        left: calc( (100vw - var(--width)) / 2 + 5vw);
        top: 77vh;

        font-size: 3rem;
        color: var(--color-text-white);
        letter-spacing: .5rem;
    }

    .collage2 {
        width: 100vw;
        height: 140vh;

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
        width: 55vw;
        left: 0;
        top: 20vh;
    }

    #img5 {
        width: 45vw;
        left: 55vw;
        top: 25vh;
    }
</style>