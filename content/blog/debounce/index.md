---
title: Debouncing 
date: "2020-03-10"
description: "Debouncing inputs"
---

Debouncing input is a way to wait before acting on input from the user. This prevents unnecessary calls
to your api or processing of inputs until the user is finished interacting with the interface. This is useful
when you only care what the final state of the input is. Any user interactions that trigger expensive api calls
can be wrapped in a debounce function.

Example code taken for Underscore.js
`
// Returns a function, that, as long as it continues to be invoked, will not
// be triggered. The function will be called after it stops being called for
// N milliseconds. If `immediate` is passed, trigger the function on the
// leading edge, instead of the trailing.
function debounce(func, wait, immediate) {
	var timeout;
	return function() {
		var context = this, args = arguments;
		var later = function() {
			timeout = null;
			if (!immediate) func.apply(context, args);
		};
		var callNow = immediate && !timeout;
		clearTimeout(timeout);
		timeout = setTimeout(later, wait);
		if (callNow) func.apply(context, args);
	};
};
`

