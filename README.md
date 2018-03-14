# angular-toasts

Angular directive for Bootstap "toast" notifications.

## Usage

Some where in your HTML, use the directive:
```
<div toast="{ timeout: 2500, position: 'top' }"></div>
```

Then, when you want to display a notification, do so with an Angular $broadcast:
```javascript
$rootScope.$broadcast("toast", {
	type: "alert-success",
	text: "This is a successful message!"
});
$rootScope.$broadcast("toast", {
	type: "alert-error",
	text: "Oh no! Something bad has happened"
});
```
