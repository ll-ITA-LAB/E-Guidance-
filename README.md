MAJOR-PROJECT-E-GUIDANCE-HUB
mern-ecommerce
Frontend-> React JS Backend-> Node JS & Express JS Database-> MongoDB

Installation process
clone the repo using this command
git clone https://github.com/ashraf-kabir/mern-ecommerce.git
install npm packages
install backend packages
cd mern-ecommerce
npm install
install frontend packages
cd client
npm install
go to the parent folder of mern-ecommerce & create .env for connection, JWT_SECRET, BRAINTREE_MERCHANT_ID, BRAINTREE_PUBLIC_KEY and BRAINTREE_PRIVATE_KEY.
cd mern-ecommerce
sudo nano .env
(ctrl+x to save & nano follow instruction there)

sample code for backend .env
MONGODB_URI=YOUR_MONGODB_URI
JWT_SECRET=YOUR_JWT_SECRET
BRAINTREE_MERCHANT_ID=YOUR_BRAINTREE_MERCHANT_ID
BRAINTREE_PUBLIC_KEY=YOUR_BRAINTREE_PUBLIC_KEY
BRAINTREE_PRIVATE_KEY=YOUR_BRAINTREE_PRIVATE_KEY
create another .env file inside client directory for REACT_APP_API_URL.
cd mern-ecommerce/client
sudo nano .env
sample code for frontend .env
REACT_APP_API_URL=YOUR_API_URL
Instructions:
for mongodb atlas database creation follow this tutorial-
https://www.youtube.com/watch?v=KKyag6t98g8

you can use any random string as JWTSECRET
for localhost REACT_APP_API_URL is http://localhost:5000/api but for heroku (server deployment) it will be different
note: add .env on .gitignore
for server deployment use secrets directly
deploy this project on your local server by using this command
cd mern-ecommerce
npm run dev
note: both backend & frontend server will start at once with the
above command. 6. #### Database Structure: (Table: columns)

categories: _id, name, createdAt, updatedAt;
orders: _id, status, products (Array), transaction_id, amount, address, user (Object), createdAt, updatedAt
products: _id, photo (Object), sold, name, description, price, category, shipping, quantity, createdAt, updatedAt
users: _id, role, history (Array), name, email, salt, hashed_password, createdAt, updatedAt
App Description:
user can view all products
user can view single product
user can search products and view products by category and price range
user can add to cart checkout products using credit card info
user can register & sign in
admin can create, edit, update & delete products
admin can create categories
admin can view ordered products
admin can change the status of a product (processing, shipped, delivered, etc.)
Deployed on
https://ecommerce-ak.herokuapp.com/
