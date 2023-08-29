This is some opinionated takes on Django.

## Project vs App
Labzero project want to move away from this unnecessary [confusion]. There's only an app, which is the top level Python namespace that you will refer throughout your application.

[confusion]:https://dev.to/k4ml/django-moving-away-from-project-vs-app-dichotomy-3e7

## CBV vs FBV
Labzero would prefer FBV most of the time. Views in Django is like a controller in the MVC pattern and controller in 80% of the cases are not reusable. Each controller is handling a very specific case of your application. You might gain some benefits in term of reduced code when using CBV but that at the expenses of code readability. CBV big selling point is reusablity, which mostly none if you're writing a controller. The only exception is when you're writing Django reusable app.

Luke Plant's [Django Views The Right Way][plant] has more extensive write up on this topic. Other takes is "[Composition over inheritance: The case for function-based views][406ch]".

[plant]:https://spookylukey.github.io/django-views-the-right-way/
[406ch]:http://web.archive.org/web/20230819023839/https://406.ch/writing/composition-over-inheritance-the-case-for-function-based-views/
