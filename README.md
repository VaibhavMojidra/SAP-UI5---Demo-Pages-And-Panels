# SAP UI5 Demo Pages And Panels

In SAPUI5, Pages and Panels are UI components used to structure and organize the content of an application.

We put both the input field and the text inside a containing control called sap/m/Page. The page provides an aggregation to 0..N other controls called content. It also displays the title attribute in a header section on top of the content. The page itself is placed into the pages aggregation of another control called sap/m/App which does the following important things for us:

It writes a bunch of properties into the header of the index.html that are necessary for proper display on mobile devices.

It offers functionality to navigate between pages with animations. We will use this soon.

In order to make the fullscreen height of the view work properly, we add the displayBlock attribute with the value true to the view. The actual content is wrapped inside a Panel control, in order to group related content.

### Code Explaination


Refer to [/webapp/view/App.view.xml](https://github.com/VaibhavMojidra/SAP-UI5---Demo-Pages-And-Panels/blob/master/webapp/view/App.view.xml "App.view.xml")


- `<mvc:View xmlns="sap.m" xmlns:mvc="sap.ui.core.mvc" displayBlock="true">`: This is the root element of the view. It uses the `sap.m` library and the `sap.ui.core.mvc` library for MVC (Model-View-Controller) support. The `displayBlock="true"` attribute ensures that the view takes up the full screen.

- `<App>`: This is a container that holds one or more pages. It's part of the `sap.m` library.

- `<pages>`: This is where you define the pages of your app.

- `<Page title="{i18n>pageTitle}">`: This creates a new page with a title. The title is taken from the internationalization model (`i18n`), which allows for multi-language support.

- `<content>`: This is where you define the content of your page.

- `<Panel headerText="{i18n>panelTitle}">`: This creates a new panel with a header. The header text is taken from the internationalization model.

- `<VBox class="sapUiSmallMargin">`: This creates a vertical layout box (VBox) with a small margin around it. Inside this VBox, there are two controls:

    - `<Text text="{/name}"/>`: This displays a text element whose value is bound to the `/name` property of the model.
    
    - `<Input value="{/name}" valueLiveUpdate="true" width="30%">`: This creates an input field whose value is also bound to the `/name` property of the model. The `valueLiveUpdate="true"` attribute ensures that the model is updated as soon as the user types into the field.

---

[![Vaibhav Mojidra - 1.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Pages-And-Panels/master/screenshots/1.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - 2.gif](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Pages-And-Panels/master/screenshots/2.gif "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)

[![Vaibhav Mojidra - 3.jpeg](https://raw.githubusercontent.com/VaibhavMojidra/SAP-UI5---Demo-Pages-And-Panels/master/screenshots/3.jpeg "Vaibhav Mojidra")](https://vaibhavmojidra.github.io/site/)