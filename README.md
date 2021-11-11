# Grocery Go Getter

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
Grocery Go Getter is a inventory tracking app that allows the user to keep an inventory of all food items in their pantry or refridgerator and also contains a shopping list to allow the user to properly map what items to get when they take a trip to the store!

### App Evaluation
[Evaluation of your app across the following attributes]
- **Category:**
- **Mobile:**
- **Story:**
- **Market:**
- **Habit:**
- **Scope:**

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User should be able to login using their username and password
* User should be able to create a new account if one does not exist
* User should be able to view a list of all of their items in their pantry
* User should be able to add items to their pantry
* User should be able to edit the order of the items
* User should be able to update item information (expiration date and amount)
* User should be able to delete an item
* User should be able to add to-do items in the shopping list
* Upon completing a task in the shopping list, the user should be able to select the task and a checkmark should appear to inform the user the task is completed.

**Optional Nice-to-have Stories**

* If an item is nearing its expiration date or the amount is getting low, the user should receive a system-wide notification regarding the low amount
* Color of the Amount element in the Pantry list should change colors depending on how much of the item is there
* If a user is adding an item, the icon of the item should be rendered by using an API that uploads the corresponding image of the product (i.e. if the user enters Chex Mix, the icon should be a Chex Mix bag)

### 2. Screen Archetypes

* Login/Register Screen - User signs up or logs into their account
   * User should be able to login using their username and password
    * User should be able to create a new account if one does not exist
    * User should stay logged in until logged out, persisting through the device

* Pantry Screen - view of items in a vertical order that contains name of product and amount
    * User should be able to view a list of all of their items in their pantry
    * User should be able to add items to their pantry
    * User should be able to edit the order of the items
    * User should be able to delete an item

* Item Detail Screen - detailed view of a specific product with additional information
    * User should be able to add/update item information (expiration date and amount)
    
* Shopping List Screen - to-do list for user
    * User should be able to add to-do items in the shopping list
    * Upon completing a task in the shopping list, the user should be able to select the task and a checkmark should appear to inform the user the task is completed.

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Pantry
* Shopping List

Optional:
* Account

**Flow Navigation** (Screen to Screen)

* Login/Register Screen
   * Account creation if no login is available
   * Navigates to User's Pantry page
* Pantry Screen
   * Selecting an item -> navigate to detailed view of item
   * Selecting shopping list tab -> navigate to shopping list screen
   * Selecting account page -> navigate to account page to show favorites and basic account info

## Wireframes
<img src="figma/wireframe.png" width=600>

### Interactive Prototype
<img src="figma/wireframe_walkthrough.gif" width=300>

## Schema
Models

Product
| Property | Type | Description |
| -------- | ---- | ----------- |
| productName | String | Name of the product in inventory |
| itemIcon | String | File path of the product stored |
| amount | Number | The amount of that particular item |
| expirationDate| DateTime | Expiration date of the item |

User
| Property | Type | Description |
| -------- | ---- | ----------- |
| username | String | Login for the user |
| password | String | Unique credential for the user (will be hashed)|
