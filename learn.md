# Learn Shopify Development

- Shopify is a powerful platform for building online stores. It's also a great platform for learning web development. This guide will help you get started.

## What is Shopify?

- Shopify is a platform for building online stores. It's a hosted solution, which means that you don't need to worry about hosting your own servers. Shopify takes care of that for you.

## What is Liquid?

- Liquid is a templating language that Shopify uses to render pages. It's similar to [Jinja](https://jinja.palletsprojects.com/en/2.11.x/) and [Django templates](https://docs.djangoproject.com/en/3.0/topics/templates/).

- The code will be a mix of HTML and Liquid. The Liquid code will be wrapped in `{% %}` or `{{ }}`.

## What is the Shopify API?

- The Shopify API is a RESTful API that allows you to interact with your store programmatically. You can use it to fetch data from your store, or to update data in your store.

## What is the Shopify CLI?

- The Shopify CLI is a command line tool that allows you to interact with your Shopify store. You can use it to create new projects, or to deploy your projects to your store.

## How does Shopify work?

- Shopify is a hosted solution, which means that you don't need to worry about hosting your own servers. Shopify takes care of that for you.

- When a request comes in, Shopify will render the page using Liquid. It will then send the rendered page back to the user. If the content is dynamic, Shopify will fetch the data from the Shopify API.

- In case the data isnt available, server of Shopify gives a 404 error.

## Shopify liquid is categorized into 3 parts:

- Objects
- Filters
- Tags

## Objects

- Objects are the data that you can access in your templates. For example, you can access the products in your store using the `products` object.

- They are variables that are used to store data which are carried on from one page to another with the help of liquid.

eg:

- `{{ product.title }}` - This will display the title of the product.

- `{{ product.price }}` - This will display the price of the product.

## Filters

- Filters are used to modify the data that you can access in your templates. For example, you can use the `money` filter to format the price of a product.

- They are used to modify the data that is stored in the objects.

- There are plenty of filters available in liquid. You can find the list of filters [here](https://shopify.github.io/liquid/filters/).

eg:

- `{{ product.price | money }}` - This will display the price of the product in the format of the currency that is set in your store.

- `{{ product.price | money_without_currency }}` - This will display the price of the product without the currency symbol.

- `{{ product.price | money_without_trailing_zeros | money_without_currency | prepend: '$' }}` - This will display the price of the product with a dollar sign in front of it.

- `{{ product.title | upcase }}` - This will display the title of the product in uppercase.

## Tags

- Tags are used to control the flow of the page. For example, you can use the `if` tag to check if a condition is true, and then display some content.

- They are closed with `{% end %}`.

eg:

- `{% if product.title == "My Product" %}` - This will check if the product title is "My Product".

- There are 4 types of tags:

- Control Flow Tags
- Iteration Tags
- Theme Tags
- Variable Assignment Tags

### Control Flow Tags

- Control Flow Tags are used to control the flow of the page. For example, you can use the `if` tag to check if a condition is true, and then display some content.

- They are closed with `{% end %}`.

eg:

- `{% if product.title == "My Product" %}` - This will check if the product title is "My Product".

- `{% elsif product.title == "My Product 2" %}` - This will check if the product title is "My Product 2".

- `{% else %}` - This will run if none of the above conditions are true.

- `{% endif %}` - This will close the `if` tag.

### Iteration Tags

- Iteration Tags are used to loop over a collection of objects. For example, you can use the `for` tag to loop over a collection of products.

- They are closed with `{% end %}`.

eg:

- `{% for product in products %}` - This will loop over all the products in the store.

- `{% endfor %}` - This will close the `for` tag.

another example:

- `{% for product in products %}` - This will loop over all the products in the store.

- `{{ product.title }}` - This will display the title of the product.

- `{{ product.price }}` - This will display the price of the product.

- `{% endfor %}` - This will close the `for` tag.

NOTE: We can combine the above two examples to get the title and price of all the products in the store.

### Theme Tags

- Theme Tags are used to include other files in your template. For example, you can use the `include` tag to include a header or footer in your template.

- They can be used for:

    - Template specific HTML codes
    - Dividing arrays into multiple pages
    - To make shopify themes use custom layouts/snippets

- Here we can find tags like:

    - `form` and `endform`

    - `section`

    - `layout`

    - `schema`

    - `paginate` and `endpaginate`

### Variable Assignment Tags

- Variable Assignment Tags are used to assign a value to a variable. For example, you can use the `assign` tag to assign a value to a variable.

- They are closed with `{% end %}`.

eg:

- `{% assign product_title = product.title %}` - This will assign the title of the product to the variable `product_title`.

- `{{ product_title }}` - This will display the value of the variable `product_title`.


## Types of Shopify Apps

- There are two types of Shopify apps: public apps and custom apps.

## Static vs Dynamic content

### Static content

- Static content is content that doesn't change. For example, the text on this page is static. It doesn't change when you refresh the page.

eg:

```liquid

{% raw %}

{{ "Hello World" }}

{% endraw %}

```

### Dynamic content

- Dynamic content is content that changes. For example, the time on this page is dynamic. It changes every time you refresh the page.
