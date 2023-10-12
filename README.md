# Skills lab 6
# Group Members: Thomas Noto, Fae Mahmoud
Our program takes a user inputted name and age. Then it displays them with some printed out messages.
Here's how to do so:
  When you open the program and run it, you will see the message: "Input your name:" followed by a text box.
  This is done by the code:
  ```python
        name = str(input("Input your name:"))
  ```
  You then type in your name to the text box, and hit enter.
  Then you will see the message, "Your name is: (your name)" 
  This is done by the code:
  ``` python
      print("Your Name is: " + name);
  ```
  Then, you will see the message: "Input your age :" followed be another text box.
  This is done by the code:
  ``` python
      age = str(input('Input your age: '))
  ```
  You will then type in your age.
  Then you will see the message, "You are (age) years old".
  This is done by the code: 
  ``` python
      print('You are ' + age + ' years old')
  ```
Here is a gif illustrating how the code works:

[Upl<!DOCTYPE html>
<!-- saved from url=(0050)https://gyazo.com/7b986672423e6bf7e3c9aedde698ecbf -->
<html><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8"><script type="text/javascript" async="" src="./cmp_files/js"></script><script type="text/javascript" async="" src="./cmp_files/analytics.js"></script><script async="" src="./cmp_files/js(1)"></script><script>window.dataLayer = window.dataLayer || [];
function gtag() { dataLayer.push(arguments); }
gtag('js', new Date());
gtag('set', 'linker', {
  'accept_incoming': true,
  'domains': ['gyazo.com', 'i.gyazo.com']
});
gtag('config', 'UA-2827501-10', {
  'linker': {
    'domains': ['gyazo.com', 'i.gyazo.com']
  }
});
gtag('config', 'G-G84Y44WHKY', {
  'linker': {
    'domains': ['gyazo.com', 'i.gyazo.com']
  }
})</script><meta content="width=device-width, height=device-height" name="viewport"><title>7b986672423e6bf7e3c9aedde698ecbf.gif</title><style type="text/css">body {
  background-color: #0e0e0e;
  color: #eee;
  margin: 0;
  font-family: sans-serif;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 10px;
}

header a {
  color: #eee;
  text-decoration: none;
  line-height: 60px;
  height: 60px;
}

header .logo {
  flex-grow: 1;
}

header .download {
  line-height: 36px;
  height: 36px;
  border: 1px solid #ccc;
  border-radius: 4px;
  color: #ccc;
  padding: 0 10px;
}

header a:hover {
  opacity: 0.9;
}

svg {
  height: 30px;
  padding-top: 12px;
}

img {
  image-orientation: from-image;
  text-align: center;
  position: absolute;
  margin: auto;
  top: 80px;
  right: 0;
  bottom: 80px;
  left: 0;
  max-width: 100vw;
  max-height: calc(100vh - 160px);
}

img.with-alert {
  top: 200px;
}

img.shrinkToFit {
  cursor: zoom-in;
}

img.overflowing {
  cursor: zoom-out;
  margin-top: 0;
  top: 0;
  bottom: 0;
  max-width: inherit;
  max-height: inherit;
}

#legacy-alert {
  display: none;
  padding: 13px 50px 13px 20px;
  border-radius: 3px;
  vertical-align: middle;
  line-height: 1.5em;
  background-color: #fff9cf;
  border-color: #f1ce44;
  color: #4a4a4a;
}
#legacy-alert a {
  color: #396bdd;
  text-decoration: none;
}
#legacy-alert.show {
  display: block;
}
</style><script type="text/javascript">document.addEventListener('DOMContentLoaded', main, false);

var zomStatus = '';

window.gyazoTrk = function (action, labelName) {
  window.gtag('event', action, {'event_category': 'i.gyazo.com', 'event_label': labelName})
}

function main () {
  updateZoomStatus()

  window.addEventListener('resize', function (event) {
    updateZoomStatus()
  })

  var image = document.getElementById('image')
  image.addEventListener('click', onClickImage)
  image.addEventListener('load', function (event) {
    updateZoomStatus()
  })

  showLegacyAlert();
}

function showLegacyAlert () {
  if (location.hash !== '#unsupported-browser') return;
  if ('replaceState' in history) {
    history.replaceState({}, document.title, "/7b986672423e6bf7e3c9aedde698ecbf");
  }
  var alert = document.getElementById('legacy-alert');
  if (!alert) return;
  alert.classList.add('show');
  alert.innerHTML = navigator.language === 'ja-JP'
    ? "<p>お使いのブラウザのバージョンは現在Gyazoではサポートしておりません。Gyazoでは快適な利用のため、最新のブラウザの利用をオススメしています。サポートブラウザについては<a href='https://helpfeel.com/GyazoJP/--5d3807bed8b95000171654f5' target='_blank'>こちら</a>をご覧ください。</p>"
    : "<p>Your browser is old and not supported. Gyazo may not work correctly. We recommend using a modern browser. <a href='https://helpfeel.com/Gyazo/--5de75e1e040e1d0017df4364' target='_blank'>Learn more</a>.</p>";
  var image = document.getElementById('image');
  if (!image) return;
  image.classList.add('with-alert');
}

function onClickImage (event) {
  if (zomStatus === '' || zomStatus === 'shrinkToFit') {
    if (imageIsShrinked()) {
      zoomIn(event)
    }
  } else {
    zoomOut()
  }
}

function updateZoomStatus () {
  var image = document.getElementById('image')

  if (zomStatus === '' || zomStatus === 'shrinkToFit') {
    if (imageIsShrinked()) {
      zoomOut()
    } else {
      zoomDefault()
    }
  } else {
    if (!imageIsShrinked()) {
      zoomDefault()
    }
  }
}

function imageIsShrinked() {
  var image = document.getElementById('image')
  return (image.width !== image.naturalWidth)
}

function zoomIn (event) {
  var image = document.getElementById('image')

  var imageX = event.pageX - image.offsetLeft
  var imageY = event.pageY - image.offsetTop

  var naturalX = imageX / image.width * image.naturalWidth
  var naturalY = imageY / image.height * image.naturalHeight

  var scrollX = naturalX - (window.innerWidth / 2)
  var scrollY = naturalY - (window.innerHeight / 2)

  zomStatus = 'overflowing'
  image.classList.remove('shrinkToFit');
  image.classList.add('overflowing');
  showHeader(false)

  window.scroll(scrollX, scrollY)
}

function zoomOut () {
  var image = document.getElementById('image')
  zomStatus = 'shrinkToFit'
  image.classList.remove('overflowing');
  image.classList.add('shrinkToFit');
  showHeader(true)
}

function zoomDefault () {
  var image = document.getElementById('image')
  zomStatus = ''
  image.classList.remove('overflowing');
  image.classList.remove('shrinkToFit');
  showHeader(true)
}

function showHeader (visible) {
  var header = document.getElementsByTagName('header')[0]
  header.style.display = visible ? '' : 'none'
}
</script><meta http-equiv="origin-trial" content="AymqwRC7u88Y4JPvfIF2F37QKylC04248hLCdJAsh8xgOfe/dVJPV3XS3wLFca1ZMVOtnBfVjaCMTVudWM//5g4AAAB7eyJvcmlnaW4iOiJodHRwczovL3d3dy5nb29nbGV0YWdtYW5hZ2VyLmNvbTo0NDMiLCJmZWF0dXJlIjoiUHJpdmFjeVNhbmRib3hBZHNBUElzIiwiZXhwaXJ5IjoxNjk1MTY3OTk5LCJpc1RoaXJkUGFydHkiOnRydWV9"></head><body><header><a class="logo" href="https://gyazo.com/" onclick="window.gyazoTrk(&#39;open&#39;, &#39;top_page&#39;);"><svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 100 33.1906">
<g>
  <g>
    <path fill="#EEEEEE" d="M12.81376,26.13836c-1.75255,0-3.40193-0.32069-4.90224-0.95314
      c-1.50005-0.63258-2.89466-1.59531-4.14512-2.86138c-1.2504-1.27254-2.20088-2.69067-2.82524-4.21513
      C0.31668,16.58321,0,14.90708,0,13.12695c0-1.81873,0.32218-3.52245,0.95755-5.06375
      c0.63569-1.54169,1.60269-2.96512,2.8742-4.2308c1.2719-1.2719,2.70096-2.23903,4.24744-2.87446
      C9.62645,0.32238,11.3358,0,13.15978,0c1.95784,0,3.81199,0.40398,5.51092,1.20066
      c1.53048,0.75213,3.06168,1.96781,4.55208,3.61376l0.18191,0.20063l-2.53596,2.42916l-0.1902-0.23754
      c-0.97892-1.22216-2.06754-2.16559-3.23576-2.804c-1.28465-0.70174-2.70355-1.05767-4.21727-1.05767
      c-2.71379,0-5.02269,0.94965-6.86254,2.82252c-1.83907,1.83933-2.77136,4.17511-2.77136,6.94284
      c0,2.8584,1.03973,5.24611,3.09024,7.09684c1.91516,1.71628,4.02266,2.58653,6.26376,2.58653
      c1.91141,0,3.65204-0.65162,5.17352-1.9366c1.52414-1.29832,2.38746-2.87536,2.56574-4.68697l0.01405-0.14377h-6.35417v-3.34501
      h10.2453v0.70913c0,1.88803-0.22524,3.58177-0.66943,5.03422c-0.43156,1.33717-1.17048,2.60609-2.19661,3.77256
      c-1.162,1.30803-2.50001,2.30249-3.97713,2.95592C16.26958,25.80691,14.60983,26.13836,12.81376,26.13836z"></path>
    <polygon fill="#EEEEEE" points="28.07189,33.1906 33.63187,22.79416 26.24624,9.73259 30.17257,9.73777 35.32783,19.42503
      40.13668,9.73777 43.96395,9.73777 31.94637,33.1906    "></polygon>
    <polygon fill="#EEEEEE" points="64.38857,25.8403 75.1158,12.6156 66.42464,12.6156 66.42464,9.61407 81.54702,9.61407
      70.91614,22.78151 81.0592,22.78151 81.0592,25.8403    "></polygon>
  </g>
  <path fill="#EEEEEE" d="M91.26947,26.54037c-4.81373,0-8.73002-3.91629-8.73002-8.73009s3.91629-8.73021,8.73002-8.73021
    c4.81404,0,8.73053,3.91642,8.73053,8.73021S96.08351,26.54037,91.26947,26.54037z M91.26947,12.30423
    c-3.0359,0-5.50581,2.46997-5.50581,5.50606c0,3.03597,2.46991,5.50594,5.50581,5.50594c3.03591,0,5.50582-2.46997,5.50582-5.50594
    C96.77529,14.7742,94.30538,12.30423,91.26947,12.30423z"></path>
  <path fill="#EEEEEE" d="M52.83164,26.24327c-4.65958,0-8.45046-3.79082-8.45046-8.45033s3.79088-8.45033,8.45046-8.45033
    c1.94178,0,3.76783,0.64087,5.28076,1.85318l0.3251,0.26086V9.52471h3.14144v16.53645H58.4375v-1.93193l-0.32497,0.26085
    C56.59947,25.60253,54.77336,26.24327,52.83164,26.24327z M52.83165,12.41523c-2.96505,0-5.37726,2.41247-5.37726,5.3777
    s2.41221,5.37758,5.37726,5.37758c2.9653,0,5.3777-2.41234,5.3777-5.37758S55.79695,12.41523,52.83165,12.41523z"></path>
</g>
</svg>
</a><a class="download" href="https://gyazo.com/signup" onclick="window.gyazoTrk(&#39;open&#39;, &#39;signup&#39;);" target="_blank">Get Gyazo for Free</a></header><div id="legacy-alert" class="show"><p>Your browser is old and not supported. Gyazo may not work correctly. We recommend using a modern browser. <a href="https://helpfeel.com/Gyazo/--5de75e1e040e1d0017df4364" target="_blank">Learn more</a>.</p></div><a href="https://gyazo.com/7b986672423e6bf7e3c9aedde698ecbf"><img id="image" src="./cmp_files/7b986672423e6bf7e3c9aedde698ecbf.gif" class="with-alert"></a></body></html>oading cmp.html…]()
