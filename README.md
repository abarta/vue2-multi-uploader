# vue2-multi-uploader

> Drag and drop multiple file uploader with Vue.js v2 and Axios

**Demo**
See live demo [here](https://abarta.github.io/vue2-multi-uploader/demo/).

**Current Version**
1.0.0

**Install**

``` bash
npm install --save vue2-multi-uploader
```
Import Component

    import MultipleFileUploader from 'vue2-multi-uploader'
    export default {
        components: {
            MultipleFileUploader
        }
    }

**Props**

| Prop name        | Type           | Required  |
| ------------- |:-------------:| -----:|
| postURL      | String |  yes
| successMessagePath      | String    |   yes |
| errorMessagePath | String     |    yes |
| minItems | Number     |    no |

postURL
Set your POST url in the postURL prop.

JSON Responses
Set JSON success and error response messages to your custom JSON responses via props:
`successMessagePath`,
`errorMessagePath`

Required props example template
``` bash
<multiple-file-uploader postURL="http://.." successMessagePath="" errorMessagePath=""></multiple-file-uploader>
```

Minimum items to upload (optional)
You can modify the minimum number of files required for the upload to take place by changing the value of minItems. Default if 2. 
If you set this prop to 1, you can use this uploader for a single file upload, like so:
``` bash
<multiple-file-uploader postURL="http://.." successMessagePath="" errorMessagePath="" minItems="1"></multiple-file-uploader>
```
**Dependencies**
Axios ^v0.15.3

**CSS**
Bootstrap CSS is used in demo but not required for the component.
CSS style is not scoped so it's easy for you to overwrite your own style.

**LICENSE**
---
The MIT License (MIT)

Copyright (c) 2017 Andrei Barta

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

