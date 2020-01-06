My name is Huyen.

I was built my ERP application, but at the moment I have 2 module.
====Security Module: Handler login, authentication user with two scenario below:
  + Fist, User can login by {UserName: admin, pass: Abc123@}, if using incorrect userName or Password user can see validation message when user hover into input form. I using custome validation create by my coding, I dont use anything relative angular formnative. I using decorator design pattern for this case.
 + Second, When user using correct {Username and password} as {admin, Abc123@} the application will navigate user to InventoryModule and the product list is dislayed.
==== InventoryModule: Handler Get product, Create Product, Edit Product, Delete Product.
 + Product Lists: User can see default Product item was created by default Task when user first login into my application.
 + Create Product: User can create product when clicking into (+ Icon)Plus Icon abow and user can navigation to page Create Product.
	+ Name was required, 
	+ Quantity was required,
	+ Price was required.
	When user submit with invalid formation the validation rule will valiate. And User can not submit form create Product.
 + Edit Product: User can navigate Edit Product page when clicking to Edit button. User can not update existed Name of product.
 + Delete Product: User can delete product when clicking to Delete button, and products list will be updated.
=====================================
Technical used:
Font-End: 
	+ Angular:
		- Create Validation directive.
		- Build IoC container in order to handler dependency injection in application.
		- Using some design pattern such as Factory, Builder Decorator.
		- Create reuesable form same with Native form in angular 7+.
		- Build in Internationalization support multiple language. Currently, I only using english.
	+ .Net core(3.0)
		- Custome ActionFilterAttribute.
		- Create ValidationException.
		- Build IoC container for DI app.
		- Build Custome Data Anotaion such as Required, Maxlength, MinLength.
		- Build UnitofWork, enhancement with multiple DBContext such as EntityFramework, MongoDb,...
=======================================================================================
====>>Unfortunately, I have issue with bundling javascript framework, I can not bundle my client application and so that I can not deploy client application into Azute. But I was deployed into my IIS local.

My ERP application will be update with DDD and CQRS in the future.