(function($){

$(document).ready(function(){
													 
// ---------------------------------------------------------
// Tabs
// ---------------------------------------------------------
$(".tabs").each(function(){

		$(this).find(".tab").hide();
		$(this).find(".tab-menu li:first a").addClass("active").show();
		$(this).find(".tab:first").show();

});

$(".tabs").each(function(){

		$(this).find(".tab-menu a").click(function() {

				$(this).parent().parent().find("a").removeClass("active");
				$(this).addClass("active");
				$(this).parent().parent().parent().parent().find(".tab").hide();
				var activeTab = $(this).attr("href");
				$(activeTab).fadeIn();
				return false;

		});

});


// ---------------------------------------------------------
// Toggle
// ---------------------------------------------------------

$(".toggle").each(function(){

		$(this).find(".box").hide();

});

$(".toggle").each(function(){

		$(this).find(".trigger").click(function() {

				$(this).toggleClass("active").next().stop(true, true).slideToggle("normal");

				return false;

		});

});



$(".recent-posts.team li:nth-child(3n)").addClass("nomargin");



// prettyphoto init
$("a[rel^='prettyPhoto']").prettyPhoto({
	animation_speed:'normal',
	slideshow:5000,
	autoplay_slideshow: false,
	overlay_gallery: true
});


/***************** IZOTOPE PORTFOLIO *******/

var container = $('.isotope'),
    filterLinks = $('#filter-by a');

	filterLinks.click(function(e){
	    var selector = $(this).attr('data-filter');
	    container.isotope({
	        filter : '.' + selector,
	        itemSelector : '.isotope-item',
	        layoutMode : 'fitRows',
	        animationEngine : 'best-available'
    });

    filterLinks.removeClass('active');
    $('#filter-by li').removeClass('current-cat');
    $(this).addClass('active');
    e.preventDefault();
});



// ---------------------------------------------------------
// Back to Top
// ---------------------------------------------------------

// fade in #back-top
$(function () {
	$(window).scroll(function () {
		if ($(this).scrollTop() > 100) {
			$('#back-top').fadeIn();
		} else {
			$('#back-top').fadeOut();
		}
	});

	// scroll body to 0px on click
	$('#back-top a').click(function () {
		$('body,html').stop(false, false).animate({
			scrollTop: 0
		}, 800);
		return false;
	});
});


/* ----------------------- ------------- USFULL ADDONS ------ ------------------ */

$('.breadcrumb li a').each(function(){
	var th = $(this);
	if (th.text()=='Uncategorized') {
		th.parent().parent().remove();
	}
});



$('#content article:first, #content article:first').addClass('first');
$('.single-post #content article').addClass('clearfix');
$('#topnav > li:last').addClass('last');

$('#topnav .sub-menu li').each(function(){
	var temp1 = $(this).find('ul');
	if (temp1.length > 0) $(this).addClass('hasChildren');
});

$('#home-content div[id*="advanced-recent-posts"]').addClass('clearfix');
$('#searchform input[type="text"]').attr('placeholder', 'Search');

$('.single-portfolio').each(function(){
	var temp1 = $(this).find('.grid_gallery');
	var temp2 = $(this).find('.two_third');
	if (temp1.length > 0) temp2.addClass('has_grid_gallery');
});

$('.search-results #content article.post-holder, .blog #content article.post-holder, .archive #content article.post-holder, .author #content article.post-holder').each(function(){
	var tempImage = $(this).find('.featured-thumbnail');
	if (tempImage.length == 0) $(this).find('.post-content').css({paddingLeft: '0'});
});

if ($('.pagination').length < 2) { $('.pagination').css({display: 'none'}); }
if ($('.pagenavi').length>0) {  $('.pagenavi').fadeIn(1000); }

/*******/

$('ul.star').each(function(){
	var tt = $(this).find('li');
	for (var i = tt.length - 1; i >= 0; i--) {
		var tx = '<span class="count">'+(i+1)+'</span>'; 	
		$(tt[i]).append(tx);
	};
});

/******/


$('.recent-post-item').addClass('clearfix');

$("body").on('mouseover', '.wpcf7-not-valid-tip',function(){ $(this).remove(); });

$.fn.equalHeights = function() {
    var heights = []; 
    this.each(function(){  heights.push($(this).height());  });

    var maxHeight = Math.max.apply(0, heights);
    this.height(maxHeight);
}

window.onload = function(){

	$('#carouselArea > div').css({opacity: '1'});
	$('#carouselArea').css({background: '#1C1C1D'});
	$('#gallery .portfolio li h6 a').equalHeights();
	$('#main .palaroidBox h5 a').equalHeights();
	$('.palaroidBox li .excerpt').equalHeights();
	$('.teamBoxs li').equalHeights();
	$('.list_carousel li .excerpt').equalHeights();

	$('.breadcrumb').animate({opacity:'1'}, 400);
}

/* ----------------------- ------------- END OF USFULL ADDONS ------ ------------------ */

/* ----------------------- -------------------------------- ------------------ */
/* ----------------------- -------------- CURRENT TEMPLATE ------------ ------------------ */
/* ----------------------- -------------------------------- ------------------ */




/**************************/

window.onresize = res;
function res(){

	//$(".list_carousel li").css({height: 'auto'});
	$("#gallery .portfolio li h6 a").css({height: 'auto'});
	$(".folio-desc p").css({height: 'auto'});
	$("#main .palaroidBox h5 a").css({height: 'auto'});
	$(".palaroidBox li .excerpt").css({height: 'auto'});
	$(".teamBoxs li").css({height: 'auto'});
	$(".list_carousel li .excerpt").css({height: 'auto'});

	//$(".list_carousel li").equalHeights();
	$('#gallery .portfolio li h6 a').equalHeights();
	$('.folio-desc p').equalHeights();
	$('#main .palaroidBox h5 a').equalHeights();
	$('.palaroidBox li .excerpt').equalHeights();
	$('.teamBoxs li').equalHeights();
	$('.list_carousel li .excerpt').equalHeights();


	/*var tHLi = $('.list_carousel li').outerHeight(true);
	$('.caroufredsel_wrapper, .list_carousel').css({height: tHLi+'px' });
	var gf = tHLi+80;
	$('#caroWrap').css({height: gf+'px'});*/

}

/*  ******************* END OF FILE***************************/
});


})(jQuery);
