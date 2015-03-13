## World Crises Project ##

---

For this project, we were required to create a website that runs off the Google App Engine. In phase one, 12 static pages needed to be developed representing four crises, four organizations, and four people. The following list contains our choices for our 12 static pages:

Crises:
  * Tohoku Earthquake
  * East African drought
  * Syraian Uprising
  * Human Trafficking

People:
  * Lady Gaga
  * Scarlett Johansson
  * Ricky Martin
  * Bashar al-Assad

Organizations:
  * MTV
  * Oxfam
  * Ricky Martin Foundation
  * United Nations

## Schema ##

---

One of the key aspects to this project was designing an XML schema to validate against. The schema has been written to satisfy all required project fields, as well as providing additional optional fields for each site endpoint.

### All types have the following required fields: ###
  * name - the name of the crisis, organization, or person
  * kind - the kind of crisis, organization, or person
  * location - the location of the crisis, organization, or person
  * description - a textual description and link of for further reading
  * social - links to related social networks
  * external links - links to external websites with a name
  * images - links to images that will be displayed in the webpage
  * video - links to the videos that will be displayed in the webpage

### Crisis specific types: ###
  * date - every crisis requires a date which is broken up into year, month, day tags.
  * human impact - the human impact provides many optional tags to display deaths, affected, missing, and displaced. Additionally, a required comments tag is provided for additional information on the human impact.
  * economic impact - this tag also provides many optional tags including cost, donations, unemployed, and a list of economic sectors. Similarly to human impact a required comments tag is present.
  * resources needed - a list of resources that are lacking in the areas where the crisis hit.
  * helping out - a tag that requires a list of ways to help, where each way is a title and url.
  * orgs list - a list of organizations associated with it
  * people list - a list of people associated with it

### Organization specific types: ###
  * contact info - contact info provides relevant optional tags like address, email, and phone number but does require name and a url
  * history - history requires a comment and url string on the history of the organization
  * people list - a list of people associated with this organization
  * crisis list - a list of crises associated with this organization

### Person specific types: ###
  * crisis list - a list of crises associated with this organization
  * people list - a list of people associated with it

## Data Models ##

---

The data models directly reflect that of the XML schema for easy exporting/importing of data. Every hierarchy in the XML schema represents a separate model in the database. A similar hierarchy in the models was established with db key references.

## HTML Pages/CSS ##

---

The static HTML pages were written with basic html/css, with added javascript for functionality.