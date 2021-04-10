# Philips Hue API

### Step 1 - Finding the IP
Since the Philips hue bridge supports UPnP discovery we can find it's ip by going to the `Network` 'folder' in windows explorer and looking for `Philips hue (?.?.?.?)`.

![Step 1](step1.png)


### Step 2 - CLIP API Debugger
By going to the following URL you will be shown the CLIP API Debugger provided by Philips.
`https://<bridge ip address>/debug/clip.html`

![Step 2](step2.png)


### Step 3 - First Command
Now we will be preforming our first command using CLIP.

| Method   | Endpoint          |
|----------|-------------------|
| POST     | /api/newdeveloper |

When preforming this command we will get an error telling us we are not authenticated as shown below. This is due to `newdeveloper` not being a valid api key. We will be getting a valid api key in the next step.

![Step 3](step3.png)


### Step 4 - Getting an API key.
To get an api key from the HUE bridge we will have to preform the following command to register our application.

| Method   | Endpoint | Body                                |
|----------|----------|-------------------------------------|
| POST     | /api     | {"devicetype":"hueapiapp#mitchell"} |

When preforming this command we will be shown an error message saying that the link button isn't pressed as seen in the image below.

![Step 4 Bad](step4-1.png)

When however when we preform the command with the link button pressed we get an api key in the format shown below.

![Step 4 Good](step4-2.png)


### Step 5 - First commands
Now that we have the API key we can request the light fixtures connected to our bridge. By making a request to the following endpoint.

| Method   | Endpoint            | Body |
|----------|---------------------|------|
| GET      | /api/\<key\>/lights |      |

When we execute this command we will get a JSON formatted object with multiple light fixtures in it.

![Step 5](step5.png)


### Step 6 - Controlling lights
Now that we have the available lights we can try turning them on or off by modifying it's state using the endpoint below.

| Method   | Endpoint                         | Body        |
|----------|----------------------------------|-------------|
| PUT      | /api/\<key\>/lights/\<id\>/state | {"on":true} |

![Step 6](step6.png)


### Step 7 - Reading sensors & switches
Ok cool now that we can control a light we can also look into other features of the HUE api like reading the state of an Philips dimmer switch.

| Method   | Endpoint                    | Body |
|----------|-----------------------------|------|
| GET      | /api/\<key\>/sensors/\<id\> |      |

By polling this endpoint once per second we can read the button state and keep track of button presses.

![Step 7](step7.png)