<script>
const urlParams = new URLSearchParams(window.location.search);
let param = $state(urlParams.get('id'))
</script>
<main>
    <h1>This is about with id {param}</h1>
</main>