Internet Retail E-commerce Back End
Internet retail, also known as e-commerce, plays a significant role within the electronics industry, as it empowers businesses and consumers alike to conveniently engage in online buying and selling of electronic products. In the latest available data from 2021, the industry in the United States alone was estimated to have generated the substantial amount of US$2.54 trillion, according to the United Nations Conference on Trade and Development. E-commerce platforms like Shopify and WooCommerce provide a suite of services to businesses of all sizes. Due to the prevalence of these platforms, developers should understand the fundamental architecture of e-commerce sites.

Project Description
Your challenge is to build the back end for an e-commerce site. You’ll take a working Express.js API and configure it to use Sequelize to interact with a PostgreSQL database.

User Story

AS A manager at an internet retail company
I WANT a back end for my e-commerce website that uses the latest technologies
SO THAT my company can compete with other e-commerce companies
Acceptance Criteria

GIVEN a functional Express.js API
WHEN I add my database name, PostgreSQL username, and PostgreSQL password to an environment variable file
THEN I am able to connect to a database using Sequelize
WHEN I enter schema and seed commands
THEN a development database is created and is seeded with test data
WHEN I enter the command to invoke the application
THEN my server is started and the Sequelize models are synced to the PostgreSQL database
WHEN I open API GET routes in Insomnia Core for categories, products, or tags
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia Core
THEN I am able to successfully create, update, and delete data in my database
Mock-Up
Refer to the provided animations and examples for testing API routes in Insomnia Core.

Getting Started
Clone the starter code repository.
Use the pg and Sequelize packages to connect your Express.js API to a PostgreSQL database.
Use the dotenv package to use environment variables to store sensitive data, like your PostgreSQL username, password, and database name.
Use the schema.sql file in the db folder to create your database using PostgreSQL shell commands.
Database Models
Your database should contain the following four models, including the requirements listed for each model:

Category
id (Integer, Primary Key, Auto Increment)
category_name (String)
Product
id (Integer, Primary Key, Auto Increment)
product_name (String)
price (Decimal)
stock (Integer)
category_id (Integer, References Category Model's id)
Tag
id (Integer, Primary Key, Auto Increment)
tag_name (String)
ProductTag
id (Integer, Primary Key, Auto Increment)
product_id (Integer, References Product Model's id)
tag_id (Integer, References Tag Model's id)
Associations
You'll need to execute association methods on your Sequelize models to create the following relationships between them:

Product belongs to Category
Category has many Product models
Product belongs to many Tag models (through ProductTag)
Tag belongs to many Product models (through ProductTag)
Walkthrough Video
Link to Walkthrough Video



