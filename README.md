<!DOCTYPE html>
<html xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
<head>
<link href='https://www.blogger.com/static/v1/widgets/2549344219-widget_css_bundle.css' rel='stylesheet' type='text/css'/>
<link href='https://i.imgur.com/01gikK4.png' rel='icon' type='image/x-icon'/>
<meta content='width=device-width, initial-scale=1' name='viewport'/>
<link href='https://cdnjs.cloudflare.com/ajax/libs/normalize/5.0.0/normalize.min.css' rel='stylesheet'/>
<link href='https://fonts.googleapis.com/css?family=Open+Sans' rel='stylesheet'/>
<link href='https://cdnjs.cloudflare.com/ajax/libs/malihu-custom-scrollbar-plugin/3.1.3/jquery.mCustomScrollbar.min.css' rel='stylesheet'/>
<link href='https://index.leanhduc.pro.vn/botchat/style.css' rel='stylesheet'/>
<script type='text/javascript'>
//<![CDATA[
function loadCSS(e, t, n) { "use strict"; var i = window.document.createElement("link"); var o = t || window.document.getElementsByTagName("script")[0]; i.rel = "stylesheet"; i.href = e; i.media = "only x"; o.parentNode.insertBefore(i, o); setTimeout(function () { i.media = n || "all" }) }
loadCSS("https://use.fontawesome.com/releases/v5.1.0/css/all.css");loadCSS("https://fonts.googleapis.com/css?family=Roboto:300,400,500,700|Roboto+Condensed:300,400,700|Roboto+Slab:400,500,700");loadCSS("//cdn.jsdelivr.net/gh/hung1001/blog@c30405f/smart/lib/font-awesome/css/all.css");loadCSS("https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css");loadCSS("https://fonts.googleapis.com/css?family=Open+Sans:300,300i,400,400i,600,600i,700,700i,800,800i&amp;subset=cyrillic,cyrillic-ext,greek,greek-ext,latin-ext,vietnamese");loadCSS("https://fonts.googleapis.com/css?family=Roboto:100,100i,300,300i,400,400i,500,500i,700,700i,900,900i&amp;subset=cyrillic,cyrillic-ext,greek,greek-ext,latin-ext,vietnamese");
//]]>
</script>
  <title>
Lê Anh Đức | Chat Bot
</title>
<!-- Bắt đầu viết Css cho web -->
<style id='page-skin-1' type='text/css'><!--
/* Chèn CSS vào đây */

--></style>

</head>
<!-- Bắt đầu phần hiển thị trên web -->
<body>
<style>
html,body{cursor:url("https://i.imgur.com/5v5M8gh.png"), auto;}
a:hover{cursor:url("https://i.imgur.com/IXULuQ1.png"), auto;}
</style>
<div class='chat'>
<div class='chat-title'>
<h1>Lê Anh Đức</h1>
<h2>leanhduc.pro.vn</h2>
<figure class='avatar'>
<img src='https://i.imgur.com/FvP92uC.png'/></figure>
</div>
<div class='messages'>
<div class='messages-content'></div>
</div>
<div class='message-box'>
<textarea class='message-input' placeholder='Type message...' type='text'></textarea>
<button class='message-submit' type='submit'>Send</button>
</div>
</div>
<div class='bg'></div>
<!-- partial -->
<script src='https://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js'></script>
<script src='https://cdnjs.cloudflare.com/ajax/libs/malihu-custom-scrollbar-plugin/3.1.3/jquery.mCustomScrollbar.concat.min.js'></script>
<script>
var $messages = $('.messages-content'),
    d, h, m,
    i = 0;

$(window).load(function() {
  $messages.mCustomScrollbar();
  setTimeout(function() {
    fakeMessage();
  }, 100);
});

function updateScrollbar() {
  $messages.mCustomScrollbar("update").mCustomScrollbar('scrollTo', 'bottom', {
    scrollInertia: 10,
    timeout: 0
  });
}

function setDate(){
  d = new Date()
  if (m != d.getMinutes()) {
    m = d.getMinutes();
    $('<div class="timestamp">' + d.getHours() + ':' + m + '</div>').appendTo($('.message:last'));
  }
}

function insertMessage() {
  msg = $('.message-input').val();
  if ($.trim(msg) == '') {
    return false;
  }
  $('<div class="message message-personal">' + msg + '</div>').appendTo($('.mCSB_container')).addClass('new');
  setDate();
  $('.message-input').val(null);
  updateScrollbar();
  setTimeout(function() {
    fakeMessage();
  }, 1000 + (Math.random() * 20) * 100);
}

$('.message-submit').click(function() {
  insertMessage();
});

$(window).on('keydown', function(e) {
  if (e.which == 13) {
    insertMessage();
    return false;
  }
})

var Fake = [
  'Hi there, I\'m Fabio and you?',
  'Nice to meet you',
  'How are you?',
  'Not too bad, thanks',
  'What do you do?',
  'That\'s awesome',
  'Codepen is a nice place to stay',
  'I think you\'re a nice person',
  'Why do you think that?',
  'Can you explain?',
  'Anyway I\'ve gotta go now',
  'It was a pleasure chat with you',
  'Time to make a new codepen',
  'Bye',
  ':)'
]

function fakeMessage() {
  if ($('.message-input').val() != '') {
    return false;
  }
  $('<div class="message loading new"><figure class="avatar"><img src="https://i.imgur.com/FvP92uC.png" /></figure><span></span></div>').appendTo($('.mCSB_container'));
  updateScrollbar();

  setTimeout(function() {
    $('.message.loading').remove();
    $('<div class="message new"><figure class="avatar"><img src="https://i.imgur.com/FvP92uC.png" /></figure>' + Fake[i] + '</div>').appendTo($('.mCSB_container')).addClass('new');
    setDate();
    updateScrollbar();
    i++;
  }, 1000 + (Math.random() * 20) * 100);

}  
</script>
<div class='navbar no-items section' id='navbar'></div>
<script src='//javascript.leanhduc.pro.vn/drop_heart.js'></script>
</body>
<!-- Kết thúc phần hiển thị trên web -->
</html>
