# React-Tabs

> A simple tabs component for ReactJS (ES6/7 class).

## Usage

Import the Tabs and Tab components into your app.

```

    import {Tabs, Tab} from './Tabs';

```

Create the markup for your tabs using JSX.

```

    <Tabs className="tabs-wrapper">
        <Tab title="Tab One" active="true">Tab One Content</Tab>
        <Tab title="Tab Two">
            <div>Tab Two Content</div>
        </Tab> 
        <Tab title="Tab Three">
            <div>Tab <strong>Three</strong> Content</div>
        </Tab>
    </Tabs>

```

The above code would generate the following HTML.

```

    <div class="tabs-wrapper">
        <ul class="tabs-nav">
            <li class="active"><a href="#">Tab One</a></li>
            <li class=""><a href="#">Tab Two</a></li>
            <li class=""><a href="#">Tab Three</a></li>
        </ul>

        <div class="tabs-content">
            <div class="tab-panel active">Tab One Content</div>
            <div class="tab-panel">
                <div>Tab Two Content</div>
            </div>
            <div class="tab-panel">
                <div>Tab <strong>Three</strong> Content</div>
            </div>
        </div>
    </div>

```

Add some CSS to make the tabs work.

```

ul.tabs-nav {
    list-style: none;
}

ul.tabs-nav li {
    display: inline-block;
    margin: 0 40px 0 0;
    border: 1px solid #ccc;
}

ul.tabs-nav li a {
    padding: 20px 40px;
    display: block;
}

ul.tabs-nav li a:hover {
    background: #f1f1f1;
}

ul.tabs-nav li.active a {
    background: #f1f1f1;
}

.tabs-content div.tab-panel {
    display: none;
    visibility: hidden;
}

.tabs-content div.tab-panel.active {
    display: block;
    visibility: visible;
}

```


Check out the [working example](http://jsbin.com/xabafi/edit?output).


## <Tabs /> Properties

###className (optional)
Define the type message you want to define, this assaigns a class to the element.

type: `string`

## <Tab /> Properties

###title (required)
The text to be used for the tabs navigation anchor.

type: `string`

###className (optional)
Define a class to be added to the tab element.

type: `string`

###id (optional)
Define a id to be added to the tab element.

type: `string`

###active (optional)
Defines if the tab is active when initially rendered.

type: `boolean`
