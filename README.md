## Intelligent Selection project - Python Flask Skeleton for Google App Engine

Original site: https://github.com/GoogleCloudPlatform

## Set up environment

1. Brew installing on mac
(on terminal) >> ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go/install)"
http://stackoverflow.com/questions/20381128/how-to-install-homebrew-on-mac-osx

2. Python and PIP install
(on terminal) >> brew install python
http://stackoverflow.com/questions/17271319/installing-pip-on-mac-os-x

3. ContextIO
	>> git clone https://github.com/ContextIO/Python-ContextIO
	>> cd Python-ContextIO
	>> pip install rauth
	>> sudo python setup.py install



## Run Locally
1. Install the [App Engine Python SDK](https://developers.google.com/appengine/downloads).
See the README file for directions. You'll need python 2.7 and [pip 1.4 or later](http://www.pip-installer.org/en/latest/installing.html) installed too.

2. Clone this repo with

   ```
   git clone https://github.com/shuaiharry/IntelligentSelection.git
   ```
3. Install dependencies in the project's lib directory.
   Note: App Engine can only import libraries from inside your project directory.

   ```
   cd IntelligentSelection
   pip install -r requirements.txt -t lib
   ```
4. Run this project locally from the command line:

   ```
   dev_appserver.py .
   ```

Visit the application [http://localhost:8080](http://localhost:8080)

See [the development server documentation](https://developers.google.com/appengine/docs/python/tools/devserver)
for options when running dev_appserver.

## Deploy
To deploy the application:

1. Use the [Admin Console](https://appengine.google.com) to create a
   project/app id. (App id and project id are identical)
1. [Deploy the
   application](https://developers.google.com/appengine/docs/python/tools/uploadinganapp) with

   ```
   appcfg.py -A <your-project-id> --oauth2 update .
   ```
1. Congratulations!  Your application is now live at your-app-id.appspot.com

## Next Steps
This skeleton includes `TODO` markers to help you find basic areas you will want
to customize.

### Relational Databases and Datastore
To add persistence to your models, use
[NDB](https://developers.google.com/appengine/docs/python/ndb/) for
scale.  Consider
[CloudSQL](https://developers.google.com/appengine/docs/python/cloud-sql)
if you need a relational database.

### Installing Libraries
See the [Third party
libraries](https://developers.google.com/appengine/docs/python/tools/libraries27)
page for libraries that are already included in the SDK.  To include SDK
libraries, add them in your app.yaml file. Other than libraries included in
the SDK, only pure python libraries may be added to an App Engine project.

### Feedback
Star this repo if you found it useful. Use the github issue tracker to give
feedback on this repo.

## Contributing changes
See [CONTRIB.md](CONTRIB.md)

## Licensing
See [LICENSE](LICENSE)

## Author
Logan Henriquez and Johan Euphrosine
