# Seconds-Counter-Through-Jquery
Seconds Counter Through Jquery



function timer(seconds, cb) {
  var remaningTime = seconds;
  window.setTimeout(function() {
    cb();
    console.log(remaningTime);
    if (remaningTime > 0) {
      timer(remaningTime - 1, cb); 
    }
  }, 1000);
}

var callback = function() {
  console.log('callback');
};

timer(90, callback);
