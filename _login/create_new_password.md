---
title: /api/organizations/complete-password/
name: Create New Password
position: 0.3
method: post
description: Provide a new password for your account
right_code: |
  ~~~ json
  {
    "password": "thanosrocks",
    "token": "G7TwCq1Vkds0DLYnfAuP"
  }
  ~~~
  {: title="Request" }


---
This API call requires that you have first requested to reset your password ("Reset Password" API call) and validated that request ("Validate Reset Password" API call). To create a new password, you provide the "reset token" that you received from the "Reset Password" API call and provide the password you'd like to use.

### Request Parameters:

password
: (string) The new password you would like to use for your account

token
: (string) This is the "reset_token" you received from your "Reset Password" API call

| Code | Name                   | Meaning                                                                                  |
|------|------------------------|------------------------------------------------------------------------------------------|
| 204  | No Content             | The API call was received and the password has been updated in our system                |
| 404  | Not Found              | Generally, the call is not sent to the correct URL or email address is not in our system |
| 415  | Unsupported Media Type | Generally, this is a syntax problem                                                      |


~~~ bash
curl -X "POST" "https://stable.projectthanos.com/api/organizations/complete-password/" \
     -H 'Content-Type: application/json; charset=utf-8' \
     -d $'{
  "token": "G7TwCq1Vkds0DLYnfAuP",
  "password": "thanosrocks"
}'

~~~
{: title="Curl" }

~~~ bash
http --json POST 'https://stable.projectthanos.com/api/organizations/complete-password/' \
    'Content-Type':'application/json; charset=utf-8' \
    token="G7TwCq1Vkds0DLYnfAuP" \
    password="thanosrocks"

~~~
{: title="HTTPie" }

~~~ python
# Install the Python Requests library:
# `pip install requests`

import requests
import json


def send_request():
    # Create New Password
    # POST https://stable.projectthanos.com/api/organizations/complete-password/

    try:
        response = requests.post(
            url="https://stable.projectthanos.com/api/organizations/complete-password/",
            headers={
                "Content-Type": "application/json; charset=utf-8",
            },
            data=json.dumps(    token="G7TwCq1Vkds0DLYnfAuP" \
    password="thanosrocks")
        )
        print('Response HTTP Status Code: {status_code}'.format(
            status_code=response.status_code))
        print('Response HTTP Response Body: {content}'.format(
            content=response.content))
    except requests.exceptions.RequestException:
        print('HTTP Request failed')

~~~
{: title="Python (requests)" }

~~~ javascript
// request Create New Password
(function(callback) {
    'use strict';

    const httpTransport = require('https');
    const responseEncoding = 'utf8';
    const httpOptions = {
        hostname: 'stable.projectthanos.com',
        port: '443',
        path: '/api/organizations/complete-password/',
        method: 'POST',
        headers: {"Content-Type":"application/json; charset=utf-8"}
    };
    httpOptions.headers['User-Agent'] = 'node ' + process.version;


    const request = httpTransport.request(httpOptions, (res) => {
        let responseBufs = [];
        let responseStr = '';

        res.on('data', (chunk) => {
            if (Buffer.isBuffer(chunk)) {
                responseBufs.push(chunk);
            }
            else {
                responseStr = responseStr + chunk;
            }
        }).on('end', () => {
            responseStr = responseBufs.length > 0 ?
                Buffer.concat(responseBufs).toString(responseEncoding) : responseStr;

            callback(null, res.statusCode, res.headers, responseStr);
        });

    })
    .setTimeout(0)
    .on('error', (error) => {
        callback(error);
    });
    request.write("{\"password\":\"thanosrocks\",\"token\":\"G7TwCq1Vkds0DLYnfAuP\"}")
    request.end();


})((error, statusCode, headers, body) => {
    console.log('ERROR:', error);
    console.log('STATUS:', statusCode);
    console.log('HEADERS:', JSON.stringify(headers));
    console.log('BODY:', body);
});

~~~
{: title="Node.js" }