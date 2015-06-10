##Introduction:

This is a modified version of Rajesh's `ionic-datepicker` directive that has dropdowns for the month and year. This directive can be used with any Ionic framework's application.


##Prerequisites.

1) node.js, bower and gulp.

##How to use:

For now, you have to check out the source from github and use the files in the src folder

Give the path of  `style.css, templates.js and ionic-datepicker.js` in your `index.html` file.

````html
<link href="lib/ionic-datepicker/dist/style.css" rel="stylesheet"> 
<!-- path to ionic/angularjs js -->
<script src="lib/ionic-datepicker/dist/templates.js"></script>
<script src="lib/ionic-datepicker/dist/ionic-datepicker.js"></script>
````    
    
3) In your application module inject the dependency `ionic-datepicker`, in order to work with the ionic time picker
````javascript
angular.module('mainModuleName', ['ionic', 'ionic-datepicker']){
 //
}
````

4) Use the below format in your template's corresponding controller

````javascript
$scope.currentDate = new Date();
````

5) Then use the below format in your template / html file

````html
<ionic-datepicker idate="currentDate" >
    <button class="button button-block button-positive"> {{ currentDate | date:'dd - MMMM - yyyy' }} </button>
</ionic-datepicker>
````


a) `ionic-datepicker` is the directive, to which we can pass required vales.

b) `idate` takes date object. If we don't pass any value, the default value will be `new Date()`.

Tested with `angular#1.3.13` and `ionic#1.0.0`. 

##Versions:

### 1) v0.1.0
The whole date picker functionality has been implemented, and can be installed with  `bower install ionic-datepicker --save`
### 2) v0.1.1
Bug Fix. This is the latest version of `ionic-datepicker` component.
### 3) v0.1.2
Bug Fix. If we don't pass the date to the time picker it will pick the todays date by default.
### 4) v0.1.3
[Bug Fix](http://forum.ionicframework.com/t/ionic-datepicker-bower-component-for-ionic-framework-applications/21516/14)
### 1) v0.1.4
Added dropdowns for the date and year

##License:
MIT
