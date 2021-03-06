# vue-masonry

Vue.js directive for masonry blocks layouting. Original [masonry library](http://masonry.desandro.com/).

## Install & Usage

 - Get from NPM:  ```npm install vue-masonry --save ```
 - Make sure that the masonry library is included, via ```<script async defer src="https://cdnjs.cloudflare.com/ajax/libs/masonry/4.0.0/masonry.pkgd.min.js"></script>``` or in other way.
 - Use in component code
    ```
    import {masonry, masonryTile} from 'vue-masonry';

    <div v-masonry transition-duration="0.3s" item-selector=".item">
        <div v-masonry-tile class="item" v-for="(item, index) in blocks">
           //some item markup
        </div>
    </div>
    ```



Properties currently available reproduce most of those on the [original masonry plugin](http://masonry.desandro.com/options.html):

 - ```item-selector=".item"``` - list element DOM item selector;
 - ```transition-duration="0.3s``` - duration of transitions;
 - ```column-width="#test"``` - element selector for column width;
 - ```origin-left="false"``` - set to group elements to the right instead of left by default
 - ```origin-top="false"``` - set to group elements to the bottom instead of top by default

### TODOs

 - implement Vue.nextTick() instead of setTimeout for initial rendering
 - add support for imageLoad plugin for image-based layouts

### License

 MIT
