# Xero Python Custom Connection Starter

This is a starter app with the code to get you interacting with the Xero API using the xero-python SDK and OAuth 2.0 Client Credentials authorisation method.

You'll be able to connect to a Xero Organisation and make real API calls - we recommend you connect to the Demo company.
Please use your Demo Company organisation for your testing. 
[Here](https://central.xero.com/s/article/Use-the-demo-company) is how to turn it on.

## Getting Started

### Prerequirements
* python3.5+ installed
* git installed
* SSH keys setup for your github profile.

### Download the code
* Clone this repo to your local drive.

### Local installation
* Open terminal window and navigate to your `xero-python-oauth2-starter` local drive directory 
* Create new python virtual environment by running `python3 -m venv venv`
* Activate new virtual environment by running `source venv/bin/activate`
* Install project dependencies by running `pip install -r requirements.txt`

## Create a Xero App
To obtain your API keys, follow these steps and create a Xero app

* Create a [free Xero user account](https://www.xero.com/us/signup/api/) (if you don't have one)
* Login to [Xero developer center](https://developer.xero.com/myapps)
* Click "New App" link
* Select "Custom connection"
* Enter your app details
* Click "Create app"
* Follow the on-screen prompts to select scopes and appoint an authorised user
* The user will have to authorise via the email they received from Xero
* Return to the app details page to obtain your client ID and generate a client secret

## Configure API keys
* Create a `config.py` file in the root directory of this project & add the 2 variables
```python
CLIENT_ID = "...client id string..."
CLIENT_SECRET = "...client secret string..."
```

## Take it for a spin

* Make sure your python virtual environment activated `source venv/bin/activate`
* Start flask application `python3 app.py`
* Launch your browser and navigate to http://localhost:5000/
* Click "Get Token"
* If everything was configured correctly your app will receive a token from Xero API
* Done - try out the different API calls

### This starter app functions include:

* Obtaining a token from Xero API via Client Credentials grant method
* storing Xero token in a permanent flask session (in local drive file)
* read organisation information from /organisation endpoint
* read invoices information from /invoices endpoint

## License

This software is published under the [MIT License](http://en.wikipedia.org/wiki/MIT_License).

	Copyright (c) 2020 Xero Limited

	Permission is hereby granted, free of charge, to any person
	obtaining a copy of this software and associated documentation
	files (the "Software"), to deal in the Software without
	restriction, including without limitation the rights to use,
	copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the
	Software is furnished to do so, subject to the following
	conditions:

	The above copyright notice and this permission notice shall be
	included in all copies or substantial portions of the Software.

	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
	EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES
	OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
	NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
	HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
	WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
	FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
	OTHER DEALINGS IN THE SOFTWARE.
