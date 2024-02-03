<script>
  import { Canvas } from '@threlte/core'
  import Scene from './Scene.svelte'
  import HUD from './HUD.svelte';
</script>

  <HUD />
  <Canvas>
    <!-- This is the #D space not for components -->
    <Scene />
  </Canvas>