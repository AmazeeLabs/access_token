# access_token
Provides view access for restricted entity when a valid access token
is present in the GET url

## Compatibility
This module works with Drupal 8.x only. For Drupal 7 check [view_unpublished](https://www.drupal.org/project/view_unpublished).

## How it works
This module relies on *hook_entity_access()* to function.

When the access token is give in the URL and if it's valid, then it will grant *view* access to viewed entity _AND_ all other entities referenced by it (paragraphs, files, taxonomy etc).

It works only on entity canonical links. For example will work on _/node/{nid}_ but not on _/not-canonical/{nid}_

## Limitations and To Do:

* At the moment the the UI is limited to nodes only: access token is displayed as an message when viewing an unpublished node.
* Find a way to inform the editors about the access_token link of other entity types than nodes

