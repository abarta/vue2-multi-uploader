# vue2-multi-uploader

> A drag and drop multiple file uploader component that uses Vue.js v2 and Axios. Uploader shows file names, sizes and total size of files added. It also allows
 setting a minimum required number of files to upload.

### Demo
See live demo [here](https://abarta.github.io/vue2-multi-uploader/demo/).

### Latest
Optional prop `method` allows PUT method to be used. Default method remains POST, if you want to use PUT just add `method="put"` to your template.

Optional `postMeta` prop added so you can include additional metadata that needs to be sent along. This prop can be in the form of a string, array or object.

### Install

``` bash
npm install --save vue2-multi-uploader
```
#### ES6
```javascript
    import MultipleFileUploader from 'vue2-multi-uploader'
    export default {
        ...
        components: {
            MultipleFileUploader
        },
        ...
    }
```
### Props

| Prop name        | Type           | Required  |
| ------------- |:-------------:| -----:|
| postURL      | String |  yes
| successMessagePath      | String    |   yes |
| errorMessagePath | String     |    yes |
| minItems | Number     |    no |
| method | String     |    no |
| postMeta | String, Array, Object     |    no |

#### postURL
Set your POST url in the postURL prop.

#### JSON Responses
Set JSON success and error response messages to your custom JSON responses via props:
`successMessagePath`,
`errorMessagePath`

Example template to use:
``` html
<multiple-file-uploader postURL="http://.." successMessagePath="" errorMessagePath=""></multiple-file-uploader>
```
Minimum items to upload (optional)
You can modify the minimum number of files required for the upload to take place by changing the value of minItems prop. Default if set to 1. 
Here is an example template for uploading a minimum of 5 items:
``` html
<multiple-file-uploader postURL="http://.." successMessagePath="" errorMessagePath="" :minItems="5"></multiple-file-uploader>
```
### Dependencies
Axios, ES6-Promise

### CSS
CSS style is not scoped so it's easy for you to overwrite your own style.
Bootstrap CSS is used in demo but not required for the component.

### LICENSE

---
The MIT License (MIT)

Copyright (c) 2017 Andrei Barta @ UPDIVISION

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

