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
3. Generate code, save on backend (FIREBASE)
4. Text user a code (TWILIO)
5. User sends us corect code
6. Compare codes on the server
7. Send user a JWT to identify them (FIREBASE)

* This solves the problem of time gap - token is saved in server
* This solved identification

### 44. Tech Stack with Google Cloud Functions 8:26

* When we generate code we'll save to FIREBASE
* When we text a coe we'll use TWILIO
* Send user a JWT to identify - FIREBASE
* We'll use GOOGLE CLOUD FUNCTIONS (similar to AWS Lambda) for some code needed on external server. Can access firebase
* REACT NATVE for the View

### 45. Traditional Servers vs Google Cloud Functions 8:21

* Comparison screenshots

### 46. Layout of Google Cloud Functions 9:49

### New User Workflow

#### Cloud Function 1
1. User enters email and phone number -
2. verify phone is not in use (hasn;t been used to log in)
3. Create a new user record(FIREBASE)
4. Respond that User was created

#### Cloud Function 2
5. User requests to login with phone number
6. Generate a code
7. Save the code to the user's record
8. Text code to the user

#### Cloud Function 3
9. User enter code
10. Compare codes
11. Mark code as no longer valid
12. Send user a JWT to identify them (FIREBASE)

### 47. Firebase Project Setup 7:21


### 48. Deploying a Firebase Project 4:35
### 49. Testing Deployed Functions 7:42
### 50. Project File Structure 5:48
### 51. The Request and Response Objects 10:49
### 52. Generating a Service Account 5:48
### 53. Sanitizing User Inputs 8:54
### 54. Creating New Users 6:22
### 55. Testing New User Creation 5:23
