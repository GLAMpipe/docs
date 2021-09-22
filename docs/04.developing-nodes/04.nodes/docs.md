---
title: Scripts
---

Node can have several scripts.

### run.js
Run script is executed once per record (excluding source nodes). By setting **out.value** or **out.setter** node can save the result of its operation.


    out.say('progress', context.data.photo.title._content); 
    if(context.data.stat != 'fail') {
        out.value = context.data.photo;
    } else {
        out.value = context.data.stat;
    }


### login.js
Upload nodes must provide login script. It will pass required login information to Metapipe (usually username, passwd and url).


### init.js
Init script is called once when running node.

    out.say('progress', 'Starting replacing..');
    /* set output field */
    out.field = context.node.params.out_field; 

### pre_run.js
pre_run is run before actual run script. Lookup nodes, for example, sets the **out.url** here..

    var base_url = 'https://api.flickr.com/services/rest/?method=flickr.photos.getSizes';
    var format = '&format=json&nojsoncallback=?';
    out.url = base_url + '&photo_id=' + context.doc[context.node.params.field] + format + '&api_key=' + context.node.settings.apikey


### finish
This is called when every record has been processed. 

    out.say('finish', 'Replace done!');

