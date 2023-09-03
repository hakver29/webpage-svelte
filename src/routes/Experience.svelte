<script lang="ts">
    export let jobTitle: string;
    export let company: string;
    export let startDate: string;
    export let endDate: string;
    export let description: string;
</script>

<div class="experience">
    <h3>{jobTitle}</h3>
    <p>{company}</p>
    <p>{startDate} - {endDate}</p>
</div>

<style>
    .experience {
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
