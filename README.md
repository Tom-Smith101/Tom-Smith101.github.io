<div id="text">
You are a using a <div id="platform"></div>
device
</div>

<script>
  function getOsFromUserAgent() {


    var userAgent = navigator.userAgent
    var platform;


    if (userAgent.includes('Android')) {
      platform = 'Android'
      // redirect link for Android. Add Play Store link below
      window.location.href = 'https://www.google.com'
    } else if (userAgent.includes('iPhone') || userAgent.includes('iPad')) {
      platform = 'iOS'
      // Redirect link for iOS
      window.location.href = 'https://www.apple.com'
    } else {
      platform = 'non-Android or iOS'
      // Fallback redirect for other platforms
      window.location.href = 'http://play.google.com/store/apps/details?id=com.google.android.apps.maps'
    }

    document.getElementById('platform').textContent = platform
  }
  getOsFromUserAgent()
</script>
