# pim1
Personal Inventory Management

React / React Native App 

An inventory management web/mobile application. Users can take pictures of items they want to add to the system and a vision api will classify and add the (after user confirms to add them). Items can be added manually by user. 

Main Page
  + to add items or take picture
  List of areas and preview of items last added to container within the area

### Create Container
*On app:* Take picture of items, 
  vision model api suggests name for container,
  suggests individual items to add, can +add and enter ?description

  sends api request to google gemini vision api to list all items present and provide attributes

  current prompt:   (needs updating to standardize attributes)
      You are an self storage classification system. List all of the objects present in the image with description and all attributes. Return as json. Return individual objects, like hat (color blue, etc)

  attributes


### Storage Hierarchy
Areas
  |  Containers
      |  Folders
          |  Items
              { _id,
                name,
                desc,
                images: {images, descriptions, aiDescriptions},
                
