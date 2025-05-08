<template>
    <div class="p8">
        <div class="footer">
            <div class="info-groups">
                <div class="info-column">
                    <div class="logo">Buster</div>
                    <div class="info-text">
                        대표 | 한병기 <br>
                        사업자번호 | 878-87-02950 <br>
                        이메일| ceo@cargolab.io <br>
                        주소| 충청남도 아산시 배방읍 호서로79번길 20, 호서벤처밸리 303호
                    </div>
                </div>
                <div class="footer-nav">
                    <div class="title">Buster</div>
                    <div class="link-item" @click="moveSection(0)">About</div>
                    <div class="link-item" @click="moveSection(1)">Vision</div>
                    <div class="link-item" @click="moveSection(2)">Features</div>
                    <div class="link-item" @click="moveSection(3)">Values</div>
                    <div class="link-item" @click="moveSection(4)">FAQ</div>
                </div>

            </div>
            <div class="divider"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
    props: {
        moveSection: {
            type: Function,
            required: true
        }
    }
};

</script>