# DIabatic Retinopathy
Diabetic Retinopathy (DR) is a serious eye condition that affects individuals with diabetes, caused by damage to the blood vessels in the retina due to prolonged high blood sugar levels. It is a leading cause of blindness worldwide, especially among working-age adults. The disease progresses through stages, starting with mild retinal swelling (non-proliferative DR) and potentially advancing to severe vision impairment due to abnormal blood vessel growth (proliferative DR). Early detection through regular eye exams  is crucial for preventing vision loss, as timely treatment with laser therapy, injections, or surgery can help manage the condition effectively.

## Installation :     
*Install requirements.txt
pip3 install -r requirements.txt
* Create a new database and table accordingly.    
* Then, Go to 'blindness.py' file and change some configuration settings according to your database.
```
connection = sk.connect(
    host="localhost",
    user="root",
    password="********",
    database="********"
)
```
* Now, your DB server must be connected.   
* Finally, you also want 'classifier.pt' file which contains model's dictionary required when it is to be loaded and put that file in the same directory and then modify the path accordingly in the 'model.py' file.
```
model = load_model('../Desktop/classifier.pt')

```
* Finally, execute your 'blindness.py' file and your GUI must start (recommended to start this from your terminal and keep all your project files in same directory).   
* Upload the image and get your predictions.

## Optional :   
* If you want to get SMS on mobile for your predictions , then Create an account on [Twilio](http://twilio.com/) by verifying your number. 
* Next, get your credentials from the Dashboard of twilio and use 'send_sms.py' to fetch API request and fill and replace your credentials.
[Note, currently 'send_sms.py' is commented out, so uncomment everything before using it].
* Then, uncomment following lines in 'blindness.py'   
```#from send_sms import *```
```#send(value, classes)```   
* Your messaging service should  start and also you now see Message_Id printed on your terminal.    
