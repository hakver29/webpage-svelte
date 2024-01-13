<script lang="ts">
    export let degree: string;
    export let university: string;
    export let startDate: string;
    export let endDate: string;
    export let description: string;
</script>

<div class="education">
    <h3>{degree} - {university}</h3>
    <p>{description}</p>
    <p>{startDate} - {endDate}</p>
</div>

<style>
    .education {
        margin-bottom: 20px;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
    }

    h3 {
        font-size: 18px;
        margin: 0;
    }

    p {
        margin: 5px 0;
    }
</style>
