<script>
  import { onMount } from "svelte";
  import { fade } from 'svelte/transition';

let phrase = 'throw new ArgumentException("Number of lines must be greater than zero."); string junkCode = "";for (int i = 0; i < numLines; i++){junkCode += GenerateRandomLineOfCode() + Environment.NewLine;}'
let typedChars = phrase[0];
let index = 0;

  /**
   * @type {number | undefined}
   */
let typeWriter;

const typeOut = () => {
    
        if (index < phrase.length) {
            typedChars += phrase[index];
            index += 1;
        } else {
            clearInterval(typeWriter)
        }
    
}

const typing = () => {
    setInterval(typeOut,10);    
} 


onMount(() =>{    
    typing();
});


</script>

<section>
    <h3 out:fade>{typedChars} </h3>
</section>

<style>
    section {
        overflow: hidden;
        min-height: max-content;
        height: max-content;
        width: max-content;
        
        position: absolute;
        bottom: 20px;
        left: 20px;
        max-width: 200px;
    }
    h3 {
        
    }
</style>