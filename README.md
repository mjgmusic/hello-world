# hello-world

This is the first thing I am typing

/*
* Simple jQuery Scroller
* Uses jQuery to animate scrolling on click
* Simply use the ID that you want to scroll to
* as the href attribute of an <a> tag
* 
* Example HTML: <a href="#main" class="scroll-to">Scroll to #main</a>
*
*/
$(document).ready(function () {
  // add event listener
  $('.scroll-to').on('click', function (e) {
    e.preventDefault();
    var id = $(e.currentTarget).attr('href')
    var target = $(id);
    $('html,body').animate({
      scrollTop: (target.offset().top)
    }, 1000);
  });
});
