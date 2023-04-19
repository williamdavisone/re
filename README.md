# re
ssd
r iframeContEl = document.getElementById('tgme_frame_cont') || document.body;
  var iframeEl = document.createElement('iframe');
  iframeContEl.appendChild(iframeEl);
  var pageHidden = false;
  window.addEventListener('pagehide', function () {
    pageHidden = true;
  }, false);
  window.addEventListener('blur', function () {
    pageHidden = true;
  }, false);
  if (iframeEl !== null) {
    iframeEl.src = protoUrl;
  }
  !false && setTimeout(function() {
    if (!pageHidden) {
      window.location = protoUrl;
