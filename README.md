Angular shopping site
===================
This is angular site for shopping build using angular material. Have different components.
shopping cart.

The application sends an actual HTTP requests while getting the list of items, item description, verifying voucher code and also buying. But since we don't have a real back-end all these HTTP requests' responses are not used. Instead mock data is used. The code is written such a way that, this HTTP URL can be easily replaced with an actual back-end URL in future. We just need to change one configuration file and no need to touch the actual logic.

Setup
-----

1)  Run the following command to install the dependencies

  `npm install`

Directory Structure
-------------------
 - **src/app** - Contains the main application and all the logic
 - **src/assets** - Contains static assets like images and theme files
 - **src/environments** - Contains the environment file. We can configure the main API URL in this file.

App Directory Structure
-------------------
 - **components** - Contains the dumb components of the application. These dumb components just receive properties and render them. They have no idea about HTTP calls and other services
 - **containers** - Contains smart components. These components work with services and get the data and pass it down to dumb components
 - **mock** - Contains the mock data for the application. Can be removed safely once we have the real back-end
 - **models** - Contains the model which is used to maintain the state and structure while passing around data
 - **modules** - Contains external modules that the application depends upon. Currently we use material design and hence this folder includes the material module
 -  **providers** - Contains the services that raises the actual HTTP requests. This is a place to add business logic
 - **utils** - Contains small utility function / files that are used throughout the application
 