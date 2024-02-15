<script>
    import Modal from "../modal/index.svelte";

    import "./index.sass";
    export let type;
    export let model;
    export let img;
    export let cost;
    export let trunk;
    export let fuel;

    let showModal = false;
    let modalProps;

    const handleModal = (props) => {
        showModal = true;
        modalProps = props;
    };
</script>

<div class="card">
    <div class="card__head">
        <div class="card__sub">{type}</div>
        <div class="card__label">{model}</div>
    </div>
    <div class="card__image">
        <img src={img} alt={model} />
    </div>
    <div class="card__body">
        <div class="card__details">
            <div class="card__details-item">
                <div class="card__details-prop">Стоимость аренды</div>
                <div class="card__details-value">
                    <span class="mark">$</span>
                    {cost.toLocaleString()}
                    <span class="dark">/ час</span>
                </div>
            </div>
            <div class="card__details-item">
                <div class="card__details-prop">Багажник</div>
                <div class="card__details-value">
                    <span class="mark">{trunk}</span> кг
                </div>
            </div>
            <div class="card__details-item">
                <div class="card__details-prop">Тип топлива</div>
                <div class="card__details-value">
                    <span class="mark">{fuel}</span>
                </div>
            </div>
        </div>
        <button
            class="card__btn"
            on:click={() =>
                handleModal({
                    cost,
                    model,
                })}>Подробнее</button
        >
    </div>
</div>

{#if showModal}
    <Modal bind:showModal {modalProps} />
{/if}
