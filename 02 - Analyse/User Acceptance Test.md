# User Acceptance Test
Dit is een user acceptance test voor de Fridge Push service omdat dit in interne service is gaan we er van uit dat de persoon die de test uitvoerd technisch onderlegd is.

## FPs01b - login test bad flow
### Instructions
Connect to the MQTT endpoint using the following credentials:
![[Pasted image 20210619012201.png]]

### Expected
You get disconnected
![[Pasted image 20210619012302.png]]

## FPs01g - login test good flow
### Instructions
Connect to the MQTT endpoint using the following credentials:
![[Pasted image 20210619012658.png]]

### Expected
You don't get disconnected and the icon turns green
![[Pasted image 20210619012821.png]]

## FPs02g- message test good flow
### Instructions
Send the following message.
![[Pasted image 20210619131017.png]]

### Expected
You don't get disconnected and the icon is still green
![[Pasted image 20210619012821.png]]

## FPs02b- message test bad flow
### Instructions
Now try sending the same message to the wrong channel.
![[Pasted image 20210619131058.png]]

### Expected
You get disconnected
![[Pasted image 20210619012302.png]]

## FPs03- dashboard
### Instructions
Check if the dashboard has the correct values.

### Expected
![[Pasted image 20210619131916.png]]

## Results
| code      	| passed? | notes |
|---------------|---------|-------|
| FPs01b    	|         |       |
| FPs01g    	|         |       |
| FPs02g 		|  		  |		  |
| FPs02b 		|  		  |		  |
| FPs03 		|  		  |		  |