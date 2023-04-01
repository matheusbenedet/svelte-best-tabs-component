# Svelte Best Tabs Component

A flexible and easy-to-use Svelte tabs component that allows you to create tabbed interfaces.

## Installation

To install this plugin, simply run the following command:

```
npm install --save svelte-best-tabs-component
```

## Usage

Import and use the `Tabs` and `TabItem` components in your Svelte project.

```svelte
<script>
    import Tabs from "svelte-tabs-component/Tabs.svelte";
    import TabItem from "svelte-tabs-component/TabItem.svelte";
</script>

<Tabs>
    <TabItem title="General Data">
        Content here ...
    </TabItem>

    <TabItem title="Invoice">
        Another content here...
    </TabItem>
</Tabs>
```

## API

### Tabs

The `Tabs` component is a container for `TabItem` components. It manages the active tab state and provides context for the child components.

| Prop           | Type   | Description                                     | Default |
| -------------- | ------ | ----------------------------------------------- | ------- |
| `activeTabValue` | any | The initial value of the active tab. If not provided, the first tab will be active. | `null` |

### TabItem

The `TabItem` component represents an individual tab within the `Tabs` component.

| Prop    | Type   | Description                                                 | Default |
| ------- | ------ | ----------------------------------------------------------- | ------- |
| `title` | string | The title to be displayed in the tab header.                | `""`    |
| `icon`  | string | An optional icon classname to be displayed in the tab header. | `""`    |
| `value` | any    | An optional unique value for the tab. If not provided, a unique `Symbol` will be generated. | `Symbol()` |

## Example

```svelte
<script>
    import Tabs from "svelte-tabs-component/Tabs.svelte";
    import TabItem from "svelte-tabs-component/TabItem.svelte";
</script>

<Tabs activeTabValue="invoice">
    <TabItem title="General Data" value="general">
        Content for General Data tab...
    </TabItem>

    <TabItem title="Invoice" icon="ti ti-receipt" value="invoice">
        Content for Invoice tab...
    </TabItem>
</Tabs>
```

In this example, the `Tabs` component has an initial active tab value of `"invoice"`, which means that the second `TabItem` with the title "Invoice" will be active initially. The tabs also include an optional icon property, which renders an icon inside the tab header.

## License

This project is licensed under the [MIT License](LICENSE).
