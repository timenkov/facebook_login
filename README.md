Example of Facebook login flow with Spring MVC
----------------------------------------------
Controller handle RESTful steps of facebook authentication process

#####Facebook settings:
+ First you need register application on facebook and get **App ID** and **App Secret** keys.
[App Dashboard](https://developers.facebook.com/apps/)
+ Specify Site URL, which will be used as `redirect_uri` : http://{host}/signin/facebook

#####Additional configs: 
+ Spring config:
```
<mvc:annotation-driven/>
<context:component-scan base-package="facebook.login"/>
<context:property-placeholder location="classpath:fb.properties"/>
```

+ Add something like `fb.properties` file with facebook keys
```
#FACEBOOK
fb.client_id=
fb.secret=
fb.redirect_uri=http://{host}/signin/facebook
```

+ Add html *facebook login button* like that `<a href="/auth/facebook" class="fb_login">Log in with Facebook</a>`


*** 
Hope it will be helpful.<br/>
Any suggestions, please contact: `timenkov(a)gmail.com`
