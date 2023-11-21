<template>
    <div>
        <div class="container">
            <div class="row">
                <div class="col-sm-12 col-md-6 col-lg-4">
                    <!-- Nội dung của bạn -->
                    <jwplayer></jwplayer>
                </div>
            </div>
        </div>

    </div>
</template>

<script>
import jwplayer from "~/components/jwplayer.op.vue"
export default {
    components: {
        jwplayer,
    }
}
</script>