#Goolge cloud functions course
##Starting a project
To start a new projetc go to 
{Firebase console}(https://console.firebase.google.com/)
or
{Google cloud function}(https://console.cloud.google.com/)
##Create a virtual environment
First we have to install 'python3-venv' with following command
```
sudo dnf install python-virtualenv
python3 -m venv venv
   and add venv into gitignore aby se to neobjevilo v gitu
source venv/bin/activate
```
In order to add new packages to our venv we created new file requirements.txt
and executed it with with this commands nad also upgraded pip
```
pip install -r requirements.txt
pip install --upgrade pip
  maybe 'pip install wheel' would be needed
```
Pak jsem jeste pridal intrepreter pro prislusny venv v settings/Python interpreter
##Deploing the cloud function hello_world
First set our project ID 
```
gcloud init
gloud projects list
gcloud config set project medigital-1595594762122
```
Then deploy the function hello_world by this command
```
cloud functions deploy hello_world --runtime python37 --trigger-http
```
The function is accessible by anybody (this can be missused)
```
https://us-central1-medigital-1595594762122.cloudfunctions.net/hello_world/?name=Petre&lastname=Simecko

``` 