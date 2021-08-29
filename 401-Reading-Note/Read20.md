# What is Django.

Django is a high-level Python web framework that enables rapid development of secure and maintainable websites. Built by experienced developers, Django takes care of much of the hassle of web development, so you can focus on writing your app without needing to reinvent the wheel. It is free and open source, has a thriving and active community, great documentation, and many options for free and paid-for support. 

features

* Object-relational mapper

Deﬁne your data models entirely in Python. You get a rich, dynamic database-access API for free — but you can still write SQL if needed.

* URLs and views

A clean, elegant URL scheme is an important detail in a high-quality Web application. Django encourages beautiful URL design and doesn’t put any cruft in URLs, like .php or .asp.

To design URLs for an application, you create a Python module called a URLconf. Like a table of contents for your app, it contains a simple mapping between URL patterns and your views.

* Templates

Django’s template language is designed to strike a balance between power and ease. It’s designed to feel comfortable and easy-to-learn to those used to working with HTML, like designers and front-end developers. But it is also flexible and highly extensible, allowing developers to augment the template language as needed.

* Forms

Django provides a powerful form library that handles rendering forms as HTML, validating user-submitted data, and converting that data to native Python types. Django also provides a way to generate forms from your existing models and use those forms to create and update data.

* Authentication

Django comes with a full-featured and secure authentication system. It handles user accounts, groups, permissions and cookie-based user sessions. This lets you easily build sites that allow users to create accounts and safely log in/out.

* Admin

One of the most powerful parts of Django is its automatic admin interface. It reads metadata in your models to provide a powerful and production-ready interface that content producers can immediately use to start managing content on your site. It’s easy to set up and provides many hooks for customization.

* Internationalization

Django offers full support for translating text into different languages, plus locale-specific formatting of dates, times, numbers, and time zones. It lets developers and template authors specify which parts of their apps should be translated or formatted for local languages and cultures, and it uses these hooks to localize Web applications for particular users according to their preferences.

## Technical Organization

The DSF handles legal, financial, and administrative matters for Django. But there is a separate organizational structure for the technical team.

Historically, Django followed Python’s model of having a Benevolent Dictator for Life, that is, a project founder who retained final say for disputes/arguments within the community. Adrian Holovaty and Jacob Kaplan-Moss functioned as Django’s dual-BDFLs from 2005 until their retirement in 2014.

Django has a small, core team of trusted volunteers who work alongside the Django Fellows to manage technical side of the Django Project. Django Core members are divided into teams that have authority over the Django Project infrastructure, including the Django Project website itself, the official issue tracker, official mailing lists, IRC channels, and more. There is currently ongoing discussion around potentially dissolving Django core or updating it in a meaningful way.

## Security

Django helps developers avoid many common security mistakes by providing a framework that has been engineered to "do the right things" to protect the website automatically. For example, Django provides a secure way to manage user accounts and passwords, avoiding common mistakes like putting session information in cookies where it is vulnerable (instead cookies just contain a key, and the actual data is stored in the database) or directly storing passwords rather than a password hash.

A password hash is a fixed-length value created by sending the password through a cryptographic hash function. Django can check if an entered password is correct by running it through the hash function and comparing the output to the stored hash value. However due to the "one-way" nature of the function, even if a stored hash value is compromised it is hard for an attacker to work out the original password.

## Maintainable

Django code is written using design principles and patterns that encourage the creation of maintainable and reusable code. In particular, it makes use of the Don't Repeat Yourself (DRY) principle so there is no unnecessary duplication, reducing the amount of code. Django also promotes the grouping of related functionality into reusable "applications" and, at a lower level, groups related code into modules (along the lines of the Model View Controller (MVC) pattern).

## Portable

Django is written in Python, which runs on many platforms. That means that you are not tied to any particular server platform, and can run your applications on many flavours of Linux, Windows, and Mac OS X. Furthermore, Django is well-supported by many web hosting providers, who often provide specific infrastructure and documentation for hosting Django sites.

## Conclusion

So where does this Django behind the scenes tour leave us? Django’s code is open source and available to all. Django’s organization is managed by a non-profit, the DSF, with a miniscule budget. And Django code is lead by a core team of volunteers, two paid Django Fellows, and a larger group of contributors.

