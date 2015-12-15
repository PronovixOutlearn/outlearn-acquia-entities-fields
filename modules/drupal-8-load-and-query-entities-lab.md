<!--
{
"name" : "drupal-8-load-and-query-entities-lab",
"version" : "0.0.1",
"title" : "Lesson 6.3 - Labs and other information ",
"description" : "TBD",
"freshnessDate" : 2015-12-11,
"homepage" : "https://docs.acquia.com/articles/drupal-8-load-and-query-entities-lab",
"canonicalSource" : "https://docs.acquia.com/articles/drupal-8-load-and-query-entities-lab",
"license" : "CC BY-SA"
}
-->

<!-- @section -->

# Overview

<!-- @section -->

## Conclusion and summary

In this lesson, we’ve seen how to work with querying and loading entities in Drupal 8\. There has been an overhaul of the Drupal 7 `EntityFieldQuery` class that turned into a robust API for querying both content and configuration entities. We’ve looked at querying content entities but the system works just the same with config entities.

We’ve also seen how to load entities based on the IDs resulting from these queries and what is actually behind the wrapper functions that perform these operations. Next up, we are going to look at defining our own content entity type in Drupal 8\. For a refresher on how we do it in Drupal 7, you can check out these [Sitepoint articles](http://www.sitepoint.com/series/build-your-own-custom-entities-in-drupal/) on the subject.

<!-- @section -->

## Lab step by step instructions:

1.  Add five nodes of the content type **Article** with fake content as samples for this lab with at least one containing the title `ipsum lorem`.

    Alternately, add the field `field_tags` to the content type **Basic Page** by editing the content type and using the **Re-use existing field** to reference **Tags**. Use this in place of the five **articles**.

2.  Recursively copy the `page_example` module from [Lesson 1](https://docs.acquia.com/articles/articles/examples-module-symfony-controllers-and-menu) to a new module called `query_example`.
3.  Rename appropriate files and terms, methods, and classes inside `query_example` as appropriate.
4.  Modify the `PageExampleController` class:
    1.  Create a new method called `simpleQuery()` to return the list of NIDs.
    2.  Create a new method called `basicQuery()` to return the array generated by the method to `simpleQuery()`.
    3.  Create a new method called `intermediateQuery()` to generate a second page example for conditional tests.
    4.  Create a new method called `conditionalStaticQuery()` to return the array generated by the method to `intermediateQuery()`.
    5.  Create a new method called `advancedQuery()` to generate a third page example for conditional tests.
    6.  Create a new method called `conditionalGroupQuery()` to return the array generated by the method to `advancedQuery()`.
    7.  Edit the routing YAML file to add the appropriate paths for new simple, intermediate, and advanced query pages.

    Alternatively, you can copy all the code from `QueryExampleController.php` to avoid manually creating each method and then modify the names.

<!-- @section -->

## Additional exercise

*   Create a page which uses the `entity.manager` and `entity.query` services to display the node teasers for `simpleQuery()`.