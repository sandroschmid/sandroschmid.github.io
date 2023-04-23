<script lang="ts">
  export let src: string | undefined = undefined;
  export let alt: string = 'Avatar Image';
</script>

<img {src} {alt}>

<style>
  img {
  	max-width: 150px;
  	border-radius: 50%;
  }
</style>
