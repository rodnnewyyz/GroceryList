# GroceryList

This repository is the home base for an application that is being built as a learning exercise. We plan to blog about the challenges we face along the way and how we solve them. It is a mobile-only application and it will be built using the latest and greatest versions of Meteor and Angular.

# The Vision

If you collaborate with other people to shop for groceries, this application will help you to effectively communicate with your shopping partner(s). 

# The Main Features

This application will support two main features:

	- populating the grocery list with new items  
		- using in-app UI
		- [future] by parsing an email or text message

	- managing the list while you're shopping at the store	
		- view list items (it's time to fill your basket with... what, exactly?)
		- view special notes on a list item (for when the small details really matter)
		- marking items off the list (as you drop them into the physical cart)
		- returning items to the list (if you change your mind and put an item back on the shelf)

# Use Cases

## Add Item to List Using A Form

	user touches Add Item menu item
		app opens a new screen; user sees UI to enter name, price, quantity, and notes
	
	user enters a name	
	user enters a price
	user enters a 'per' unit ... kg, lb, each, bag, box, etc.
	user enters a quantity
	user enters free form notes (optional)

		for each text field, user will see a list of cached values, filtered to match user's entry on each keystroke

	user Saves item
		item gets added to the list
		the UI clears itself
		cart's item count is updated

## View List Items
	
	user touches Grocery List menu item
		app displays the grocery list
		items with notes are highlighted

	user touches Cart menu item
		app displays a list of items that have been placed in the cart 
		items with notes are highlighted

	user gestures to show details on a list item
		app displays item notes (optional)

	user gestures to move an item to the other list
		app moves item to other list and gives user an opportunity to undo
	

A list item has the following attributes

	- name (string)
	- price (number)
	- price 'per' unit (string)
	- quantity (number)
	- notes (string)
