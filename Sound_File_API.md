# Sound Files Operations
This topic explains how to perform REST operations on sound files, such as uploading or retrieving information about them to or from from a user profile.

## Uploading a sound file
Uploads a sound file.

* **URL**

  https://api.sounddate.com/profile/sound

* **Method**

  `POST`

* **Sample Request**

  ```
  https://api.sounddate.com/profile/sound
  Bearer: {access token}
  Content-Type: audio/mpeg
  Accept: application/json
  {sound file}
  ```
* **Headers**
  **Bearer:** The access token. Required.
  **Content-Type:** The format of the sound file. Optional. Possible values:  `audio/mpeg`, `audio/xwav`.
  **Accept:** The response format. Optional. Possible values: `application/xml`, `application/json`.

* **Success Response**
  Code: `200`
  Response Header:
  ```
  {
     "id":123,
     "length":3.13
  }
  ```
  
* **Response Codes and Errors**
  **200:** OK. Successful operation.
  **401:** Unauthorized. Invalid access token.
  **413:** Payload too large. The sound file is too long.



