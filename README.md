# elastic-update

Element providing a way to update a single elasticsearch document based on an _id. 

Example:
```html
    <template is="dom-bind">
        <elastic-client
            config='{"host": "http://localhost:9200"}'
            client="{{esclient}}"
            cluster-status="{{my-status}}">
        </elastic-client>

        <elastic-update
            client="[[esclient]]"
            index="mockads"
            id="4"
            elastic-type="ad"
            body='{doc: {title: "new title here"}}'
            results="{{data}}"
            lastError="{{error}}">
        </elastic-update>
    </template>
```

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

To run the demo and unit tests, you will need a local elasticsearch instance and the mockads data referenced in the elastic-client-search repo.