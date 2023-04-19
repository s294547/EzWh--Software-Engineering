# EZWH - Easy Warehouse Management

|||
|:--:|:--:|
| **AuthorS** | Giulia Bianchi, Edoardo Colella, Manuel Colotti, Giovanna Di Benedetto|

</div>

EZWH (EaSy WareHouse) is a software application designed to support the management of a warehouse. It provides a simple and intuitive interface for managing relationships with suppliers and the inventory of physical items stocked in a physical warehouse.

The application is designed for use by a warehouse manager, who supervises the availability of items in the warehouse. When a certain item is in short supply, the manager can issue an order to a supplier. In general, the same item can be purchased from many suppliers. The warehouse keeps a list of possible suppliers per item.

After items are ordered from a supplier, they are received at the warehouse and must be quality checked and stored in specific positions. The quality check is performed by specific roles (quality office), who apply specific tests for each item. Possibly the tests are not made at all, or made randomly on some of the items received. If an item does not pass a quality test, it may be rejected and sent back to the supplier.

Storage of items in the warehouse takes into account the availability of physical space in the warehouse. The position of items is traced to guide later retrieval.

The warehouse is part of a company. Other organizational units (OU) of the company may ask for items in the warehouse. This is implemented via internal orders, received by the warehouse. Upon receipt of an internal order, the warehouse must collect the requested item(s), prepare them, and deliver them to a pickup area. When the item is collected by the other OU, the internal order is completed.

## Backend
The backend of EZWH is implemented using the Express.js framework, which is a popular and lightweight web framework for Node.js. It includes several components to manage the application's data and business logic, such as:

Database: EZWH uses a SQLite database to store information about the warehouse, items, suppliers, internal orders, and more. The database schema is defined using the Sequelize ORM (Object-Relational Mapping) library for Node.js.
APIs: EZWH provides a set of RESTful APIs for interacting with the application, such as adding new items to the warehouse, issuing orders to suppliers, and fulfilling internal orders from other organizational units. The APIs are defined in the routes directory, which includes separate files for each resource.
Services: EZWH includes several backend services to handle tasks such as quality checks, item storage, and order fulfillment. These services are implemented as separate modules in the services directory.

## Frontend
The frontend of EZWH is implemented using React, which is a popular and widely used JavaScript library for building user interfaces. It includes several components to manage the application's user interface, such as:

UI components: EZWH includes several UI components to display information and interact with the user, such as forms for adding new items, tables for displaying warehouse inventory, and buttons for issuing orders. These components are defined in the src/components directory.
State management: EZWH uses Redux for managing the application's state, which includes information about the current inventory, suppliers, internal orders, and more. The state is defined using actions and reducers in the src/store directory.
API calls: EZWH makes API calls to the backend using Axios, which is a popular and lightweight HTTP client for the browser and Node.js. The API calls are defined in the src/services directory.

