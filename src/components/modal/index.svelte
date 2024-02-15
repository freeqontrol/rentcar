<script>
    import "./index.sass";

    import iconClose from "./icons/close.svg";
    import iconWallet from "./icons/wallet.svg";
    import iconCard from "./icons/card.svg";

    export let showModal;

    let modal;

    export let modalProps;
</script>

<!-- svelte-ignore a11y-click-events-have-key-events a11y-no-noninteractive-element-interactions -->
<div
    role="dialog"
    bind:this={modal}
    on:close={() => (showModal = false)}
    on:click|self={() => (showModal = false)}
    class="modal"
>
    <div class="modal__body">
        <button on:click={() => (showModal = false)} class="modal__close">
            <img src={iconClose} alt="close" />
        </button>
        <h1 class="modal__title">Аренда транспорта</h1>
        <div class="modal__details">
            <div class="modal__details-item">
                <div class="modal__details-prop">Название транспорта:</div>
                <div class="modal__details-value">{modalProps.model}</div>
            </div>
            <div class="modal__details-item">
                <div class="modal__details-prop">Стоимость аренды:</div>
                <div class="modal__details-value">
                    <span class="mark">$</span>
                    {modalProps.cost.toLocaleString()}
                    <span class="dark">/ час</span>
                </div>
            </div>
        </div>
        <div class="modal__box">
            <div class="modal__box-sub">Количество часов аренды:</div>
            <div class="modal__box-time">
                <label class="modal__time">
                    <input type="radio" name="time" value="1" checked />
                    <span>1 час</span>
                </label>
                <label class="modal__time">
                    <input type="radio" name="time" value="2" />
                    <span>1 час</span>
                </label>
                <label class="modal__time">
                    <input type="radio" name="time" value="3" />
                    <span>1 час</span>
                </label>
                <label class="modal__time">
                    <input type="radio" name="time" value="4" />
                    <span>1 час</span>
                </label>
                <label class="modal__time">
                    <input type="radio" name="time" value="5" />
                    <span>1 час</span>
                </label>
                <label class="modal__time">
                    <input type="radio" name="time" value="6" />
                    <span>1 час</span>
                </label>
                <label class="modal__time">
                    <input type="radio" name="time" value="7" />
                    <span>1 час</span>
                </label>
                <label class="modal__time">
                    <input type="radio" name="time" value="1" />
                    <span>1 час</span>
                </label>
            </div>
        </div>
        <div class="modal__box">
            <div class="modal__box-sub">Цвет автомобиля:</div>
            <div class="modal__box-color">
                <label class="modal__color">
                    <input type="radio" name="color" value="color1" />
                    <span style="background-color: #211218;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color1" />
                    <span style="background-color: #EEDCDD;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color1" checked />
                    <span style="background-color: #98898D;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color2" />
                    <span style="background-color: #CF1919;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color3" />
                    <span style="background-color: #E77618;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color4" />
                    <span style="background-color: #EEB320;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color5" />
                    <span style="background-color: #28522B;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color6" />
                    <span style="background-color: #4E64C4;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color7" />
                    <span style="background-color: #691369;"></span>
                </label>
                <label class="modal__color">
                    <input type="radio" name="color" value="color1" />
                    <span style="background-color: #7B523A;"></span>
                </label>
            </div>
        </div>
        <div class="modal__box">
            <div class="modal__box-head">
                <div class="modal__box-sub">Итоговая стоимость:</div>
                <div class="modal__box-cost"><span>$</span> 1 500</div>
            </div>
            <div class="modal__btns">
                <button class="modal__btn">
                    <img src={iconWallet} alt="icon" />
                    Наличными
                </button>
                <button class="modal__btn">
                    <img src={iconCard} alt="icon" />
                    По карте
                </button>
            </div>
        </div>
    </div>
</div>
