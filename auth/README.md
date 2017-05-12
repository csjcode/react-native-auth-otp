# react-native-auth-fb
React Native Authorization/Login with Firebase

## One Time Password Authentication

### 42. Review of Common Auth Flows 8:20

* Login screenshot
* We're going to haev one page with the Signup and Signin
* This is going to be a very detailed and complex Authorization app
* For Signup - We're going to get a phone number and email
* For Signin - Phone number and Code

### 43. The Details of One Time Passwords 10:04

* Simple Flow screenshot

1. User enter phone number.
2. We text the user a token
3. User enters token in our app
4. We verify token is correct
5. if token correct then it's authenticated

* A ton of time can be beteween steps 2 and 4
* Also, hwat does it mean to eb authenticated?
* Don't send the expected code the user has to enter (token) via HTTP!!!! ie. don't send the valid token
* DONT cmopare the the entered and expected tokens on the mobile device itself.
* INSTEAD, do on a external server

### Ideal OTP Authentication Workflow

1. User request OTP
2. Confirm request
3. Generate code, save on backend
4. Text user a code
5. User sends us corect code
6. Compare codes on the server
7. Send user a JWT to identify them

* This solves the problem of time gap - token is saved in server
* This solved identification

### 44. Tech Stack with Google Cloud Functions 8:26





### 45. Traditional Servers vs Google Cloud Functions 8:21
### 46. Layout of Google Cloud Functions 9:49
### 47. Firebase Project Setup 7:21
### 48. Deploying a Firebase Project 4:35
### 49. Testing Deployed Functions 7:42
### 50. Project File Structure 5:48
### 51. The Request and Response Objects 10:49
### 52. Generating a Service Account 5:48
### 53. Sanitizing User Inputs 8:54
### 54. Creating New Users 6:22
### 55. Testing New User Creation 5:23
