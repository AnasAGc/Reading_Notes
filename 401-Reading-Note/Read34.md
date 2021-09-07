# Readings: API Deployment Summary:
## Configuring Django Settings: Best Practices:
#### Managing Django Settings: Issues:
1. **Different environments** Each environment can have its own specific settings.we need an approach that allows us to keep all env Django setting configurations.
2. **Sensitive data** we have SECRET_KEY in each Django project.. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This data cannot be stored in VCS.
3. **Sharing settings between team members** You need a general approach to eliminate human error when working with the settings. 
4. **Django settings are a Python code** This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of key-value pairs, settings.py can have a very tricky logic.

#### Setting Configuration: Different Approaches :
1. First approach >> extend all environment-specific settings in settings_local.py file, which is ignored by VCS. 
   - Pros: Secrets not in VCS.
   - Cons: 
         * settings_local.py is not in VCS, so you can lose some of your Django environment settings.
         * The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.
         * You need to have settings_local.example (in VCS) to share the default configurations for developers.


2. Second approach >> Separate settings file for each environment : This is an extension of the previous approach. It allows you to keep all configurations in VCS and to share default settings between developers.
 - To run a project with a specific configuration, you need to set an additional parameter:
```
python manage.py runserver --settings=settings.local
```
   - Pros:
         * All environments are in VCS.
         * It’s easy to share settings between developers.

  - Cons:
         * You need to find a way to handle secret passwords and tokens.
         * “Inheritance” of settings can be hard to trace and maintain.
3. Third approach >> Environment variables "perfect place to store settings" : by using environment variables.
   - Pros:
         * Configuration is separated from code.
         * Environment parity – you have the same code for all environments.
         * No inheritance in settings, and cleaner and more consistent code.
         * There is a theoretical grounding for using environment variables – 12 Factors.

   - Cons:You need to handle sharing default config between developers.
* **12 Factors** : is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created by Heroku, a well-known Cloud hosting provider.Its main rule is to store configuration in the environment. Following this recommendation will give us strict separation of config from code.
* Instead of splitting settings by environments, you can split them by the source: Django, third- party apps (Celery, DRF, etc.), and your custom settings.
* Give meaningful names to your settings ,always use the prefix with the project name for your custom (project) settings and write descriptions for your settings in comments.

## How Does SSH Work :
* **SSH, or Secure Shell** is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and relaying the output back to the client.
* The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client. 
* There are three different encryption technologies used by SSH:
  1. Symmetrical encryption
  2. Asymmetrical encryption
  3. Hashing.