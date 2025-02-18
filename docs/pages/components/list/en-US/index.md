# List

Used to display a set of data

## Import

<!--{include:(components/list/fragments/import.md)}-->

## Examples

### Basic

<!--{include:`default.md`}-->

### Size

<!--{include:`size.md`}-->

### Border

<!--{include:`bordered.md`}-->

### Hover

<!--{include:`hover.md`}-->

### Sortable

> `index` of List.Item is required. (be unique in the collection)

<!--{include:`sortable.md`}-->

### Collection Sort

> `colection` has its own space, `index` of List.Item is required. (be unique in the collection)

<!--{include:`collection.md`}-->

#### Fixed Item Sort

> based on `collection`, Item can fixed during sort order.

<!--{include:`sort-fixed.md`}-->

### Custom

<!--{include:`custom.md`}-->

## Props

### `<List>`

| Property           | Type `(Default)`                                   | Description                          |
| ------------------ | -------------------------------------------------- | ------------------------------------ |
| autoScroll         | boolean `(true)`                                   | auto scroll when overflow            |
| bordered           | boolean                                            | bordered                             |
| hover              | boolean                                            | hover animation                      |
| onSort             | (payload:[Payload](#code-ts-payload-code)) => void | callback of end of sorting           |
| onSortEnd          | (payload:[Payload](#code-ts-payload-code)) => void | callback of end of sorting           |
| onSortMove         | (payload:[Payload](#code-ts-payload-code)) => void | callback of moving over a list items |
| onSortStart        | (payload:[Payload](#code-ts-payload-code)) => void | callback of beginning of sorting     |
| pressDelay         | number `(0)`                                       | delay before trigger sort            |
| size               | 'lg' &#124; 'md' &#124; 'sm' `(md)`                | list items size                      |
| sortable           | boolean                                            | can change list item order           |
| transitionDuration | number `(300)`                                     | duration of sort animation           |

### `<List.Item>`

| Property   | Type `(Default)`                    | Description                                     |
| ---------- | ----------------------------------- | ----------------------------------------------- |
| collection | number &#124; string `(0)`          | collection of list item                         |
| disabled   | boolean                             | not allowed to move this item                   |
| index \*   | number(required when sortable)      | index of item(must be unique in the collection) |
| size       | 'lg' &#124; 'md' &#124; 'sm' `(md)` | current item size                               |

### `ts:Payload`

```ts
interface Payload {
  collection: number | string;
  node: HTMLElement;
  newIndex: number;
  oldIndex: number;
}
```
