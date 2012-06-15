twilio-backend
==============

Twilio backend for [django-social-auth](https://github.com/omab/django-social-auth)

* Register a new application at [Twilio Connect Api](https://www.twilio.com/user/account/connect/apps)

* fill `TWILIO_CONNECT_KEY` and `TWILIO_AUTH_TOKEN` values in the settings:


    `TWILIO_CONNECT_KEY = ''
     TWILIO_AUTH_TOKEN = ''
`
* Add twilio backend in `        '/social_auth/backends/contrib/twilio`

* Add desired authentication backends to Django's `AUTHENTICATION_BACKENDS` setting:

        'social_auth.backends.contrib.twilio.TwilioBackend',

    
Usage example
==============
Authentication process starts with `socialauth_begin` URL.

Template code example:

`<a href="{% url socialauth_begin 'twilio' %}">Enter using Twilio</a>`
