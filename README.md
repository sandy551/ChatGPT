> [!TIP]
> To stay updated on the latest news and insights on mule-related topics, follow us on:
> [^1]:
> [Subscribe for latest updates(✨🌟FREE✨🌟)](https://mule.org.in/m/create-account)
> [^1]:
> [Our website](https://mule.org.in/)
> [^1]:
> [Our WhatsApp channel](https://www.whatsapp.com/channel/0029VaIq2XrKbYMPKdl3YE3X)
> [^1]:
> [WhatsApp community](https://chat.whatsapp.com/F6cPb1xEsGdEJ7rrfEHN0H)
> [^1]:
> [Our LinkedIn page](https://www.linkedin.com/company/mule-trains/)

# ChatGPT Integration

The name ChatGPT stands for Chat Generative Pre-trained Transformer. This latest GPT technology is based on a deep learning model that evaluates the importance of the words or phrases in each input.

ChatGPT can write silly poems and songs or quickly explain just about anything found on the internet.

This project enables you to quickly start creating interact with OpenAI-chatGPT by:

* Guiding you through project creation and setup.
* How to get API Key and how to use it.


**Requirements**

  * Java 8 or 11 provided
  * Apache Maven
  * Anypoint Studio for your specific operating system
  * Modern browsers
  * Postman
  
**Generating API key**

  * Go to OpenAI - https://platform.openai.com/
  * Click on profile.
  * Click on view API Key.
  * Click on create new security key.
  * Once click on create new security key it will pop up new window with security key, so keep your secure key safely, if you lost the key generate new one.

**How config in our API**
  * Open anypoint studio
  * Create a new project
  * Drag and drop the listener connector 
    * add host as localhost
    * port as 8081(user choice)
    * path opeanAI(user choice)

**config the request details to integrate with openAI**
  * Request URL: https://api.openai.com/v1/chat/completions
  * Headers need to pass(**$OPENAI_API_KEY indicates your API Key**)
    * Authorization: Bearer $OPENAI_API_KEY
    * Content-Type: application/json
  * Body
    ```json
    {
      "model": "gpt-3.5-turbo",
      "messages": [
          {
              "role": "user",
              "content": "Hello!"
          }
      ]
    }
    ```
**Postman collections**
  in postman collection for every request body have a header section in that you need to replace yourAPIKey with your api key(generated in #[Generating API key section])
  ```
  Authorization: Bearer {yourAPIKey}
  ```
**References**

https://medium.com/@k.sandeep5121/how-to-interact-with-openal-chatgpt-through-mulesoft-180963761761
