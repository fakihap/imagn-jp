<script>
   import kyoto_1 from '$lib/images/tianshu-liu-SBK40fdKbAg-unsplash.jpg';
   import kyoto_2 from '$lib/images/redd-f-wPMvPMD9KBI-unsplash.jpg';
   import kyoto_3 from '$lib/images/sorasak-_UIN-pFfJ7c-unsplash.jpg';
</script>

<div>
    <div class="collage1">
        <img id="img1" src={kyoto_1} alt="kyoto1" />
        <img id="img2"src={kyoto_2} alt="kyoto2" />
        <img id="img3"src={kyoto_3} alt="kyoto3" />
        <div>EXPLORE KYOTO</div>
    </div>
</div>


<style>
    #img1, 
    #img2, 
    #img3 {
        object-fit: contain;
        position: absolute;
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
        left: calc( (100vw - var(--width)) / 2 + 5vw);
        top: 77vh;

        font-size: 3rem;
        color: var(--color-text-white);
        letter-spacing: .5rem;
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
</style>