# RecipeGenie
RecipeGenie is a software that uses OCR and a custom API to send recipe suggestions based on a receipt image. This project was made as part of the UNIHACK/Atlassian Hackathon 2024. 

**Link to project demo:** https://youtu.be/6diwDfM9Ue8?si=GrofulDr7CTqJUlz&t=52

## How It's Made:  

**Tech used:** HTML, CSS, Javascript, Python (FastAPI), OpenCV, Pytesseract

The front end of the project was built using basic HTML, CSS and JavaScript without any frameworks. Through javascript, API calls were made to our own custom API developed using the python asyncrhonus API framework FastAPI. This API would take the scanned receipt from the front-end, and parse it into a Numpy Array, which would then be processed using OpenCV to undergo resizing, binarization, dilation, normalisation and merging to ensure the text on the receipt could be read effectively. 

This text was then processed using OCR. To ensure that the text scanned was reliable, only text with a >50% confidence was accepted, and it was then removed of symbols, numbers before being passed into OpenAI's api to come up with a list of ingredients based on everything scanned. OpenAI's api would then return the list of recipes, which were emailed to the user on validation of their email address. 

## Lessons Learned:

The key lesson learnt from this application was how to process images, and develop an asynchronus API rapidly. Most of the challenges faces were with OCR's text recognition not working as intended, therefore a large amount of time and research had to be invested into figuring out the steps required to process the image in order to make it readable. 


## Contributors
Dhruv Israni
Suman Plackal 
Adrian Dimar
Jayden Mun Wai Ng



