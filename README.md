Example of Facebook login flow with Spring MVC
==============================================

- First you need register facebook app and get App ID and App Secret keys.
- Specify Site URL: (http://{host}/signin/facebook)

- It required simple Spring MVC config 
+ `<mvc:annotation-driven/> <context:component-scan base-package="gameru" />` for using annotation
+ On page add *facebook login button* like that `<a href="/auth/facebook" class="fb_login">Log in with Facebook</a>`
+ Add something like fb.properties file with facebook keys
`#FACEBOOK
fb.client_id=
fb.secret=
fb.redirect_uri=http://{host}/signin/facebook
`
+ In spring xml config specify `<context:property-placeholder location="classpath:fb.properties"/>`

*** 
Controller handle REST steps of facebook authentication process
