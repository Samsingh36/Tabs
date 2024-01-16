Live Deployed Link - https://l5q6d6-3000.csb.app/

User Tabs Component

Implementing a basic (not fully accessible) Tabs component in React is quite simple due to the fact that only one state value is needed, the currently active tab item. React also helps to keep the state and the UI in sync, which is more troublesome to do so in Vanilla JavaScript.

Props (API Design)

Part of the complexity of building a component is designing the API for it. In the case of React, it would be the props of the component. At the bare minimum, we will need the following props:

1. items: A list of item objects. Each item is an object with the fields:

2. value: A unique identifier for the tab item.

3. label: The text label to show in the tab item.

4. panel: The contents to show in the tab panel when the item is active.

5. defaultValue: The default tab item/panel to show. In case the defaultValue is not provided, we'll use the first item as the value. This is assuming that items is non-empty.

For controlled components, there will be a value and onChange props instead of a defaultValue prop.

Test Cases

1. All the provided items should be displayed.
 
2. The default active item should be reflected correctly.
  
3. Selecting the tab items updates the tab panel's contents with the active tab's panel details.
  
4. Test that you are able to initialize multiple instances of the component, each with independent states.
   
Accessibility

Accessibility is a crucial factor for a good Tabs component. The ARIA Authoring Practices Guide for Tabs has a long list of guidelines for the ARIA roles, states, and properties to add to the various elements of a Tab. Tabs II and Tabs III will focus on improving the accessibility of the Tabs component.

