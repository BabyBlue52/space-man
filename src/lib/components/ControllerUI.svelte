<script>
    
    import Y from './models/y-btn.svelte'
    import B from './models/b-btn.svelte';
    import A from './models/a-btn.svelte';
    import X from './models/x-btn.svelte';

    let isPressedY = false;
    let isPressedX = false;
    let isPressedB = false;
    let isPressedA = false;

    const buttonYPressed = () => {
        isPressedY = true;
        setTimeout(() => {
           isPressedY = false;  
        }, 150)
    }
    const buttonBPressed = () => {
        isPressedB = true;
        setTimeout(() => {
           isPressedB = false;  
        }, 150)
    }
    const buttonXPressed = () => {
        isPressedX = true;
        setTimeout(() => {
           isPressedX = false;  
        }, 150)
    }
    const buttonAPressed = () => {
        isPressedA = true;
        setTimeout(() => {
           isPressedA = false;  
        }, 150)
    }

</script>

<div class="d-pad">
    <div class="d-flex">
        <button id="y" on:click={buttonYPressed} class="{isPressedY ? 'isPressed' : ''}">
            <Y/>
        </button>
    </div>
    <div class="d-flex w-100">
        <button id="x" on:click={buttonXPressed} class="{isPressedX ? 'isPressed' : ''}">
            <X/>
        </button>
        <button id="b" on:click={buttonBPressed} class="{isPressedB ? 'isPressed' : ''}">
            <B/>
        </button>
    </div>
    <div class="d-flex" >
        <button id="a" on:click={buttonAPressed} class="{isPressedA ? 'isPressed' : ''}">
            <A/>
        </button>
    </div>
</div>

<style lang="scss">
    .d-flex {
        display: flex;
        justify-content: center;
    }
    .w-100 {
        position: relative;
        width: 210px;
        justify-content: space-between;
    }
    .d-pad {
        z-index: 999;
        position: absolute;
        bottom: 10%;
        right: 2%;
        width: 200px;
        height: max-content;
        #y {
            position: relative;
            top: 15px;
            left: 5px;
        }
        #a {
            position: relative;
            bottom: 15px;
            left: 5px;
        }
    }
    .isPressed {
        filter: invert(1);
        transform: scale(1.05);
        stroke: none;
    }
</style>