<script>
    export let message = '하이하이';
    export let showModal = false;
    export let isPromo = true;
</script>
{#if showModal}
    <div class="backdrop" class:promo={isPromo} >
        <div class="modal">
            <p>Sign up for offers!</p>
            <p>{message}</p>
        </div>
        <button type="button" on:click>닫기</button>
    </div>
{/if}
<style>
    .backdrop {
        width: 100%;
        height: 100%;
        position: fixed;
        top: 0;
        left: 0;
        background: rgba(0, 0, 0, 0.8);
    }
    .modal {
        padding: 10px;
        border-radius: 10px;
        max-width: 400px;
        margin: 10% auto;
        text-align: center;
        background: white;
    }
    .promo .modal {
        background: crimson;
        color: white;
    }
</style>

    