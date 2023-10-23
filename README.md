# OdooNautica - Ship-Themed Hotel Management with Odoo

## Project Overview

Welcome to the "OdooNautica" project! This project is designed to help you dive into and master the key mechanics of the Odoo platform. By the end of this project, you'll become a true Odoo expert, capable of customizing and expanding the ERP system to meet your business needs.

"Odoonautica" is an Odoo customization project featuring a ship-themed hotel management system. The primary concept revolves around managing hotel rooms and reservations made by guests who seek a unique experience on this ship.

## Task 1: Create Maritime Management Module

### Create a New Odoo Module

Start by creating a new Odoo module named `maritime_management` with essential files and a manifest file.

### Define Odoo Models

1. **Model Name: `maritime.ship`**
   - Fields:
     - `name`: Char field, name of the ship
     - `captain`: Many2one field, the field should be related to the `res.user` model

2. **Model Name: `maritime.cabin`**
   - Fields:
     - `code`: Char field that should be unique
     - `type`: Selection field with options "standard" and "premium"
     - `number_of_beds`: Integer field to represent the number of beds in the cabin

### Access Rights

Set up access rights to allow only system administrators to access the newly created models.

### Views

- Add form and tree view for both created models.
- Create a menu item that triggers an action to open these views.

## Task 2: Connection Between Models

In this stage, you should have a running "Maritime Management" application with basic views and fields. Now we will make some customizations to our module.

### One2many & Many2one Relationships

- Add a new field `cabin_ids` to `maritime.ship` that will contain information about all cabins that this ship has. You also need to define a field `ship_id` in the `maritime.ship` model to connect both fields.
- Add the field `ship_id` to the form view.

### Compute Field

Create a new field `cabin_count` on model `maritime.ship` that will count the number of cabins on the ship.

### Smart Button

In the view of ships, create a new smart button panel where you will add a smart button that will display the number of cabins connected to that ship. When you click this smart button, it should display a list view with all connected cabins of that ship.
