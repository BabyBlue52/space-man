<script>
    import Year from "./models/2024.svelte";
    import Typewriter from "./Typewriter.svelte";
    import ControllerUI from "./ControllerUI.svelte";
</script>
<div class="hud">
    <div style="transform:scale(0.9);margin-left: -10px">
        <h1>Man in Space</h1>
        <div class="kennedy">
            <p>We choose to go to the moon. We choose to go to the moon in this decade and do the other things, not because they are easy, but because they are hard.</p>
        </div>
    </div>
    <section class="year-link">
        <Year/>
    </section>
    <section>
        <ControllerUI/>
    </section>
    <section>
        <Typewriter/>
    </section>
</div>
<style lang="scss">
    @import '../variables.scss';
    .hud {
        position: absolute;
        top: 0;
        left:0;
        border: salmon 1px solid;
        height: calc(99vh - 2%);
        width: calc(99vw - 2%);
        margin: 20px;   
        .kennedy {
            position: relative;
            bottom: 30px;
            left: 2px;
        }
        .year-link {
                position:absolute;
                bottom: 65px;
                right: 5px;
                height: 20px;
                width: 20px;
            
            }    
     
    }
    @media screen and (max-width: 600px){
        .hud {
            border: salmon 1px solid;
            height: calc(95vh - 1%);
            width: calc(95vw - 5%);
           
            .year-link {
                position:absolute;
                bottom: 65px;
                right: 5px;
                height: 20px;
                width: 20px;
            
            }    
        }
    }
</style>