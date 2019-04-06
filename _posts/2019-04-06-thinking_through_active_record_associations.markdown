---
layout: post
title:      "Thinking through Active Record Associations"
date:       2019-04-06 19:13:55 +0000
permalink:  thinking_through_active_record_associations
---


Active Record Associations provide your code with a group of methods that connect two Active Record models. One simple line of code like 

```
has_many
```

Adds a number of methods to your model. The code resembles natural speech (i.e., a list has many items) and simplifies the coding process. But when learning Ruby on Rails, it is important to understand the processes behind this simple declaration.

Active record associations tell Rails that there is a connection between two models. What this means in practice is that Rails will create new methods attached to one or both models that allow one model to access the information stored in another model. These methods create shortcuts that make it seem like two separate database tables are contained within one another, and can operate upon one another in a seamless manner.

To provide a more concrete example, the belongs_to association is declared on one model, establishing that each instance of the declared upon model will be connected to one instance of another method. In more technical terms, the declared upon model will contain the foreign key of the other model.

**Methods**

Let’s look at some of the methods built into the different associations. If an Item model has been programmed with a belongs_to association to a List model (with a has_many association itself), Activer Record will create an association method than is named after the “parent” model. So for our item/list example, we might call an instance of the item class with the list method like:
```
@item.list
```
This would return the database information about the list that this item has been associated with. In this line of code, we can see the shortcut active record assocation has provided. It is as if “list’ is an attribute within the item database table that we can call as simply as an attribute like “name” that would be included in the list table.

If we wanted to assign a new item to a list, Active Record association provides a methods for that also. If @item is an unassociated object model, we can call
```
@item.list = @list
```
This will attach this instance of our item variable to the instance of the list that we are currently accessing. Calling this method will add the foreign key of this instance of the list model to this instance of our item model.

We can also look at the methods built into the has_many association. Let’s look at the collection method first. In our list/item example, we can reverse the order of the association method from the has_many relationship (making sure to pluralize):
```
@list.items
```
This will return all of the item objects that have been associated with the instance of the list object we are calling.

We can also add a new object to our “parent” object with the following method:
```
@list.items << @item1
```
Here we use the shovel operator to include a new instance of an item class to the collection object of the list. Active record does this by adding the foreign key of @list to this instance of item1. 

Of course Active Record associations add multiple new methods to each model they are declared upon, we have only surveyed the most basic methods here. Visit the Rails Guide to find out more about the methods I have discussed here and learn about more associations and other methods.

https://guides.rubyonrails.org/association_basics.html#has-many-association-reference

