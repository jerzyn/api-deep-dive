# API Design Workshop


## Requirements

- Read [Adidas API Guidelines](https://adidas.gitbook.io/api-guidelines)
- Git
- Code editor (e.g. [VS Code](https://code.visualstudio.com))
    * in case you are using VS Code, install extensions such as `openapi-lint`, `openapi-viewer` and `YAML`
- [Apiary](https://apiary.io) account within adidas group.
- [Swagger Editor](https://editor.swagger.io) For visualising and validating your specification.

## Design challenge

As a new assignment you are asked to write an API contract basing on a given list of affordances. You will base on a sample api description following adidas API guidelines and a number of predefined object models.

Your team decided wisely to think [API First](https://adidas.gitbook.io/api-guidelines/general-guidelines/api-first) and [API Design First](https://adidas.gitbook.io/api-guidelines/rest-api-guidelines/core-principles/design-maturity).

## API affordances (actions)

The existing core Product API provides this affordances:

- Retrieve the list of products
- Retrieve a single product
- Create a product
- Update an existing product (status...)
- Retrieve reviews about a product
- Add a product review
- Retrieve product reviews statistics
- Create a user
- Retrieve user profile
- Retrieve the user wishlist
- Add a product into the wishlist
- Delete a specific product from the wishlist
- Clear the wishlist

## Step1. Let's describe what actions our API affords

**TASK**: Translate the affordances into a REST API model. What endpoints will this API have? What operations will it perform on these endpoints? Can you find an alternative way to achieve similar, if not better, results from a design point of view?

## Step2. Formalize the design in the [Open API Specification](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md)

> The OAS (Open API Specification) file can be edited in whatever tool you like *BUT NOT GENERATED FROM YOUR CODE*. We suggest either using [Swagger Editor](https://editor.swagger.io) or VS Code with extensions. The most important thing is that the final one (the contract) *MUST* be in Apiary.

**TASK**: Extend the existing `sample-api.yaml`. First change the filename into a name of your project. 

We will walk step by step through the file explaining each of the different elements. Then basing on them you will, in pairs, complete a list of exercises defining subsequent parts of the API contract. 

_NOTE:_ Remember to validate your API specification after each exercise (step) completed.

## Step3. Verify the design using Apiary Documentation and Apiary Mock Service

**TASK**: Put your API contract into a new Apiary project. Check the validation. Does your API comply with the rules? If yes, try the Apiary Mock Service.

## Step4. Review the API Design

At this stage you:

- Ask feedback from your API users by sending them the documentation link.
- Ask feedback from your product owner

In our context it means that you will change your pairs and in those new pairs verify each other's design (peer review).

## Some example of bad designed APIs

### [[Sales and Distribution] Returns Confirmation API](https://returnsconfirmation.docs.apiary.io/)
Missing description
Missing examples
Missing HAL
Exposing internal model
Missing support contact

### [ATP Notification Service](https://atpnotificationservice.docs.apiary.io/)
Usage of acronyms, what's ATP stands for ?
Missing description / context
Missing HAL
Missing support contact

## Some example of good designed APIs

Sample APIs following the guidelines are available at [adidas-group GitHub](https://github.com/adidas-group). The samples include the following:

### [Simple API](https://github.com/adidas-group/demo-simple-api)
Very simple API including implementation, testing, and full CI/CD lifecycle.

### [Approval API](https://github.com/adidas-group/demo-approval-api)
Real-world API with state transition, API key client app authentication, exposed via API management.

### [Orders API](https://github.com/adidas-group/demo-orders-api)
Sample API used as the template for newly created projects at Apiary.

### [Inventory API](https://eainventoryapi.docs.apiary.io/)
Real-world Adidas Inventory API (WIP)

### [Appointment Service](https://github.com/adidas-group/demo-appointment-service)
Demo API, including implementation and testing used during training.

### [Complex Search Parameters](https://github.com/adidas-group/demo-complex-search)
Sample API showcasing description of complex query parameter rules.

### [CPM] Asset Trafficker https://assetmanager4.docs.apiary.io/