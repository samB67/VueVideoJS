<template>
    <div class="container">
        <h1>Videos View</h1>
        <div class="row justify-content-center">
            <div class="col-md-12">
                <div class="card mb-4 shadow-sm">
                    <div class="card-header">Test Video</div>

                    <div class="card-body">
                            <video-js id="Player" class="vjs-default-skin" controls preload="auto" width="640" height="268">
                                <source src="https://www.w3schools.com/html/mov_bbb.mp4">
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
    // videojs
    import videojs from 'video.js'
    window.videojs = videojs


    // hls plugin for videojs6
    // require('videojs-contrib-hls/dist/videojs-contrib-hls.js')

    export default {
        name: "VideosPage",

        data: () => {
            return {
            }
        },

        mounted() {
            videojs('Player');
        }
    }
</script>
<style scoped>

</style>
