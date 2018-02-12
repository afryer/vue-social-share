<template>
  <div class="js-share-page share-page__icons">
    <a 
        class="share share--twitter" 
        href="https://twitter.com/intent/tweet?source=webclient&text=http://www.urlofpagegoeshere.com" 
        target="_blank" 
        data-title="twitter-share"
        data-hashtags="twitter,another,hashtag"
        data-text="share this on twitter">
        Share this page on twitter</a>

    <a 
        class="share share--facebook" 
        href="http://www.facebook.com/sharer.php?&p[url]=http://www.urlofpagegoeshere.com" 
        target="_blank" 
        data-title="facebook-share">
        Share this page on facebook</a>


    <a 
      class="share share--linkedin" 
      href="http://www.linkedin.com/shareArticle?mini=true&url=http://www.urlofpagegoeshere.com" 
      target="_blank"
      data-title="linkedin-share"
      data-text="share on linkedin">
      Share this page on LinkedIn</a>

    <a 
      class="share share--googlePlus-share" 
      target="_blank" 
      data-title="googlePlus-share"
      data-text="share on googleplus"
      href="https://plus.google.com/share?url=http://www.urlofpagegoeshere.com">
      Share this page on google plus</a>
    
    <a 
      class="share--email" 
      data-title="email-share" 
      href="mailto:?Subject=Social Share&amp;Body=I%20saw%20this%20and%20thought%20of%20you!%20https://bbc.com">
      Share this page via email</a>

  </div><!-- /.share-page__icons -->
</template>

<script>

export default {
  name: 'SocialShare', 

  data () {
    return {
      shareOptions: ['Twitter', 'Facebook','LinkedIn',],
 
      popup: {
        height: 350,
        width: 520,
        menubar: false,
        toolbar: false,
        resizable: true,
        scrollbars: false,
        top: 0,
        left: 0,
        window: undefined
      },
      networks: {
        email: {
          sharer: 'mailto:?subject=@title&body=@url%0D%0A%0D%0A@description',
        },
        twitter: {
          sharer: 'https://twitter.com/intent/tweet?text=@title&url=@url&hashtags=@hashtags@twitteruser',
        },
        facebook: {
          sharer: 'https://www.facebook.com/sharer/sharer.php?u=@url&title=@title&description=@description&quote=@quote',
        },
        linkedin: {
          sharer: 'https://www.linkedin.com/shareArticle?mini=true&url=@url&title=@title&summary=@description',
        },
        googleplus: {
          sharer: 'https://plus.google.com/share?url=@url',
        },
        pinterest: {
          sharer: 'https://pinterest.com/pin/create/button/?url=@url&media=@media&description=@title',
        },
        reddit: {
          sharer: 'https://www.reddit.com/submit?url=@url&title=@title',
        },
        whatsapp: {
          sharer: 'whatsapp://send?text=@description%0D%0A@url',
        },
        sms: {
          sharer: 'sms:?body=@url%20@description',
        },


      }

    }
  }, 

  mounted () {
    this.popupDefaults.top = (screen.height / 2) - (this.popupDefaults.height / 2);
    this.popupDefaults.left = (screen.width / 2) - (this.popupDefaults.width / 2);
  }, 

  methods: {
    openSharer (network,url) {
      this.popup.window = window.open(
        url,
      )
    }
  }



}

</script>

<style scoped>

</style>


