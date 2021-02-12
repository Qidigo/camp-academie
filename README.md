# Qidigo-iFrame

This project is built to be used with iFrames that are hosted directly on qidigo. That way, user information is ported between the two apps.

**Your organization identifier (organizationId):** 267


# Group listing

This component is used to display, under a list format, all the groups for a given activity. It also takes care of  the log in, register as well as the whole activity subscription process up until the desired item has been added to the cart. You need to pass an *activityId* url param for this to work properly. The identifier of an activity can be found directly in the
[manager platform of Qidigo](https://aide.qidigo.com/fr/comment-trouver-lidentifiant-dune-activite) (fr).

## Example of usage

![](https://cdn.loom.com/sessions/thumbnails/bacf4fb11b224658ac77ee6b786d4671-with-play.gif)

## Accepted parameters

| Parameters      | Description                                  | Possible values/format                     | Required? | Default |
| --------------- | -------------------------------------------- | ------------------------------------------ |:---------:|:-------:|
| activityId      | Filter the groups by activity                | integer                                    | x         |         |
| language        | Set the language                             | [fr\|en]                                   |           | fr      |
| primaryColor    | Change the primary color                     | hexadecimal value(without #) or color name |           | F40B17  |
| shoppingCartUrl | Action when the client clicks on "View cart" | link                                       |           | #       |
| gtag            | Google Analytics tracker                     | GTM-XXXXXXX                                |           |         |

## Integration

```html
<div>
    <iframe
            style="box-shadow: 0 1px 15px 3px rgba(50,50,50,0.10); border: 1px solid #E3E3E3; transition: height ease 0.3s; width: 100%; max-width: 1080px; min-height: 20px"
            id="qidigo-iframe-groups-and-offers"
            src="https://www.qidigo.com/embed/v1.0/groups-and-offers?{{PARAMETERS}}">
    </iframe>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/4.1.1/iframeResizer.min.js"
            integrity="sha256-cEc8isF4TnMrb5OarPG3xyR5aOlECPt9Dbup+rFaEcw=" crossorigin="anonymous"></script>
    <script>iFrameResize({log: true, checkOrigin: false}, 'qidigo-iframe-groups-and-offers')</script>
</div>
```

# Cart

This component allows the user to remove items from his cart, and redirect to Qidigo upon payment. You need to pass an *organizationId* url param for this to work properly. The identifier of an organization can be found directly in the manager platform of Qidigo.

## Example of usage

![](https://cdn.loom.com/sessions/thumbnails/830ab44d2e34455e956ff64c835eed49-with-play.gif)

## Accepted parameters

| Parameters     | Description                                                           | Possible values/format                     | Required? | Default |
| -------------- | --------------------------------------------------------------------- | ------------------------------------------ |:---------:| ------- |
| language       | Set the language                                                      | [fr\|en]                                   |           | fr      |
| organizationId | Filter cart items to show only the ones belonging to the organization | integer                                    | x         |         |
| primaryColor   | Change the primary color                                              | hexadecimal value(without #) or color name |           | F40B17  |
| gtag           | Google Analytics tracker                                              | GTM-XXXXXXX                                |           |         |

## Integration

```html
<div>
    <iframe
            style="box-shadow: 0 1px 15px 3px rgba(50,50,50,0.10); border: 1px solid #E3E3E3; transition: height ease 0.3s; width: 100%; max-width: 1080px; min-height: 20px"
            id="qidigo-iframe-cart"
            src="https://www.qidigo.com/embed/v1.0/cart?{{PARAMETERS}}">
    </iframe>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/4.1.1/iframeResizer.min.js"
            integrity="sha256-cEc8isF4TnMrb5OarPG3xyR5aOlECPt9Dbup+rFaEcw=" crossorigin="anonymous"></script>
    <script>iFrameResize({log: true, checkOrigin: false}, 'qidigo-iframe-cart')</script>
</div>
```

# Cart icon

This component displays the number of items in your cart, the timer and links to your shopping cart address. You need to pass a *shoppingCartUrl* url param for this to work properly.

## Accepted parameters

| Parameters      | Description                                                           | Possible values/format  | Required? | Default |
| --------------- | --------------------------------------------------------------------- | ------- |:---------:|:-------:|
| organizationId  | Filter cart items to show only the ones belonging to the organization | integer | x         |         |
| shoppingCartUrl | Set the action on click                                               | link    |           | #       |

## Integration

```html
<iframe
        scrolling="no"
        style="overflow:hidden; height: 24px; width: 36px; border: none;"
        id="qidigo-iframe-extend-cart-button"
        src="https://www.qidigo.com/embed/v1.0/add-to-wishlist?{{PARAMETERS}}">
</iframe>
```
