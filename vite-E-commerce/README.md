The code is divided into  4 parts.
Entities (It holds all the object models for the data that is used in the project. The entities act as the core of the architecture and are totally independent of the code logic.

UseCases (This component holds all the business logic of our project. It is added to the project either in the services, stores or utility functions. The business logic is isolated from the TS component for reusability and maintenance purposes. The business logic is dependent upon the entities only and is independent of the framework being used)

Interface <Controllers> (These are the TS components of the project. It acts as a controller and passes the control from the user through UI to the Business Logic functions and back to user)

UI_Framework (This folder holds the APP.js component as this is where we integrate our tools and packages that are used. The configuration of these tools and packages are added to this folder)

1.Entities.
The entities/ directory contains TypeScript files defining domain entities such as Product, User, and Order. These entities represent core data structures within the application.


Order.ts
Defines the Order entity, representing an order placed by a user in the e-commerce store.
Properties: id, user, products, totalPrice, status, createdAt, updatedAt, etc.


Product.ts
Defines the Product entity, representing a product in the e-commerce store.
Properties: id, name, description, price, category, image, stock, createdAt, updatedAt, etc.


User.ts
Defines the User entity, representing a user of the e-commerce platform.
Properties: id, username, email, password, firstName, lastName, address, createdAt, updatedAt, etc.

2. Interface.
This directory contains React components that make up the user interface of your e-commerce application.
components/
Products/


Product.tsx:
          Renders a single product.

          
ProductList.tsx:
          Renders a list of products.

          
Content/
UI/


ImageContainer.tsx:
                Contains product images.

                
LinkContainer.tsx:
                Contains product links.

                
TextBox.tsx:
                Contains text content.

                
VideoContainer.tsx:
                Contains product videos.
MainLayout/

Container.tsx:
                Contains the main layout structure.
Header.tsx:
                Renders the header section.
Footer.tsx:
                Renders the footer section.

3. Use Cases.
The useCases/ directory contains modules related to managing business logic, particularly focused on products in this structure.

Products/


ProductsAPI.tsx:
               Provides an API client for fetching product data.

               
ProductsActions.tsx:
               Defines actions for managing product-related state.

               
ProductsReducers.tsx:
               Reducers for handling product-related state changes.

               
ProductsUtils.tsx:
               Utility functions for working with product data.

4. UI Framework
This directory contains files related to UI framework setup, including routing.

router/


Router.tsx:
            Main router configuration component.

            
RoutesList.tsx:
            Contains route configurations.
