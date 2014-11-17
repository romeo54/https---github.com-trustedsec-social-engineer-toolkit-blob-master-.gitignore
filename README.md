<htlm>
<head>
  <title>Google+ JavaScript Quickstart</title>
  <script src="https://apis.google.com/js/client:platform.js" async defer></script>
  <span id="signinButton">
  <span
    class="g-signin"
    data-callback="signinCallback"
    data-clientid="CLIENT_ID"
    data-cookiepolicy="single_host_origin"
    data-requestvisibleactions="http://schema.org/AddAction"
    data-scope="https://www.googleapis.com/auth/plus.login">
  </span>
</span>
function signinCallback(authResult) {
  if (authResult['status']['signed_in']) {
    // Update the app to reflect a signed in user
    // Hide the sign-in button now that the user is authorized, for example:
    document.getElementById('signinButton').setAttribute('style', 'display: none');
  } else {
    // Update the app to reflect a signed out user
    // Possible error values:
    //   "user_signed_out" - User is signed-out
    //   "access_denied" - User denied access to your app
    //   "immediate_failed" - Could not automatically log in the user
    console.log('Sign-in state: ' + authResult['error']);
  }
}
<meta name="google-signin-attribute_name" content="your value" />
<meta name="google-signin-clientid" content="xxxxxxxxxxxxxx.apps.googleusercontent.com" />
<meta name="google-signin-cookiepolicy" content="single_host_origin" />
<meta name="google-signin-callback" content="signinCallback" />
<meta name="google-signin-requestvisibleactions" content="https://schema.org/AddAction" />
<meta name="google-signin-scope" content="https://www.googleapis.com/auth/plus.login" />
<div class="g-signin"
<script type="text/javascript">
  (function() {
   var po = document.createElement('script'); po.type = 'text/javascript'; po.async = true;
   po.src = 'https://apis.google.com/js/client:plusone.js';
   var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(po, s);
 })();
</script>
<!-- Coloca la etiqueta donde quieras que se muestre el botón -->
<button
  class="g-interactivepost"
  data-contenturl="https://plus.google.com/pages/"
  data-contentdeeplinkid="/pages"
  data-clientid="xxxxx.apps.googleusercontent.com"
  data-cookiepolicy="single_host_origin"
  data-prefilltext="Engage your users today, create a Google+ page for your business."
  data-calltoactionlabel="CREATE"
  data-calltoactionurl="http://plus.google.com/pages/create"
  data-calltoactiondeeplinkid="/pages/create">
  Tell your friends
</button>
