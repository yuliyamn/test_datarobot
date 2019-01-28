<template>
  <div class="footer-wrap">
    <div class="footer">
      <div class="footer-text"><img src="./assets/robot-ico-1.png"/> DataRobot, Inc. © 2012</div>

      <div class="social-buttons">
        <div class="fb-share-button" data-href="https://www.datarobot.com/" data-layout="button" data-size="small" data-mobile-iframe="true">
          <a target="_blank" href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fwww.datarobot.com%2F&amp;src=sdkpreparse" class="fb-xfbml-parse-ignore">Share</a>
        </div>
        <a href="https://twitter.com/intent/tweet?screen_name=DataRobot&ref_src=twsrc%5Etfw" class="twitter-mention-button" data-show-count="false">Tweet</a>
        <div class="g-plus" data-action="share" data-href="https://www.datarobot.com/"></div>
      </div>

      <div class="footer-text">Better predictions. Faster.</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "Footer"
  }
</script>

<style scoped lang="scss">
  .footer-wrap {
    position: relative;

    &:before {
      content: '';
      position: absolute;
      left: -100px;
      right: -100px;
      height: 1px;
      background-color: #e1e8f0;
      top: 0;
    }
  }
  .footer {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 28px 0;
    margin-top: 35px;

    @media screen and (max-width: 940px) {
      flex-direction: column;
      padding-top: 80px;

      p {
        margin-bottom: 14px;
        width: 50%;
      }
    }

    @media screen and (max-width: 768px) {
      margin-top: 0;
      padding-top: 120px;
    }

    @media screen and (max-width: 940px) {
      .footer-text {
        img {
          display: block;
          margin: 0 auto 10px;
        }
      }
    }
  }
  .social-buttons {
    position: absolute;
    top: 28px;
    left: 50%;
    transform: translateX(-50%);
    text-align: center;

    .fb_iframe_widget {
      top: -3px;
    }
  }
</style>
