<template>
    <div class="container">
        <h1>Videos View</h1>
        <div class="row justify-content-center">
            <div class="col-md-12">
                <div class="card mb-4 shadow-sm">
                    <div class="card-header">Test Video</div>

                    <div class="card-body">
                            <video-js ref="Player" class="vjs-default-skin" controls preload="auto" width="640" height="268">
                                <source src="https://d2zihajmogu5jn.cloudfront.net/bipbop-advanced/bipbop_16x9_variant.m3u8" type="application/x-mpegURL">
                            </video-js>
                        <br>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    // custom skin css
    import 'vue-video-player/src/custom-theme.css'
    // Import videojs..
    import videojs from 'video.js'
    window.videojs = videojs
    
    // Require http-streaming plugin..
    require('@videojs/http-streaming/src/videojs-http-streaming.js');

    export default {
        name: "VideosPage",

        data: () => {
            return {
            }
        },

        mounted() {
            videojs(this.$refs.Player);
        }
    }
</script>
<style scoped>

</style>
