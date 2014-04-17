#Angular JS Scroll Section Loader
Auto template loader with scroll event for Angular JS.

##Install
Bower: ```bower install angular-scroll-section-loader```

##Usage
- Include module in your html.
> ```<script src="/angular-scroll-section-loader/scroll-section-loader.min.js"></script>```

- Add 'scrollSectionLoader' as a dependency in your Angular app.
> var app = angular.module('myApp',[scrollSectionLoader']);

- In controller:
> ```$scope.sections = ['about','services','contact']; //html files to load (about.html, etc)```
> ```$scope.loadedSections = [$scope.sections[0]]; //loaded html files```

- In html:
```html
	<section ng-repeat="section in loadedSections"  
           ng-include="section+'.html'"  
           scroll-section  
           sections="sections"  
           loaded-sections="loadedSections">  
```