<script lang="ts">
    import Lenis from 'lenis';
    import 'lenis/dist/lenis.css';

    $effect(() => {
        const lenis = new Lenis({ autoRaf: true });
        return () => lenis.destroy();
    });
</script>