<script>
    import Card from "../card/index.svelte";

    import "./index.sass";

    import iconWallet from "./icons/wallet.svg";
    import iconCard from "./icons/card.svg";
    import iconClose from "./icons/close.svg";

    import carImage from "./icons/boxville.png";
</script>

<div class="rentcar">
    <div class="rentcar__content">
        <div class="rentcar__head">
            <div class="rentcar__head-left">
                <div class="rentcar__label">Аренда</div>
                <div class="rentcar__tag">Post Car</div>
            </div>
            <div class="rentcar__head-right">
                <div class="rentcar__money rentcar__money--active">
                    <img src={iconWallet} alt="icon" />
                    $156 485 213
                </div>
                <div class="rentcar__money">
                    <img src={iconCard} alt="icon" />
                    $156 485 213
                </div>
            </div>
            <button class="rentcar__close">
                <img src={iconClose} alt="close" />
            </button>
        </div>
        <div class="rentcar__main">
            <div class="rentcar__items">
                <Card
                    type={"Автобус"}
                    model={"Boxville long name car for testttt"}
                    img={carImage}
                    cost={1500}
                    trunk={50}
                    fuel={"Premium"}
                />
                <Card
                    type={"Автобус"}
                    model={"Boxville"}
                    img={carImage}
                    cost={900}
                    trunk={50}
                    fuel={"Premium"}
                />
                <Card
                    type={"Автобус"}
                    model={"Boxville"}
                    img={carImage}
                    cost={15000}
                    trunk={50}
                    fuel={"Premium"}
                />
                <Card
                    type={"Автобус"}
                    model={"Boxville"}
                    img={carImage}
                    cost={100}
                    trunk={50}
                    fuel={"Premium"}
                />
            </div>
        </div>
    </div>
</div>
