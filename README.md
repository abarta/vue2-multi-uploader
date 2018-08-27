# REPO MOVED: https://github.com/updivision/vue2-multi-uploader

# vue2-multi-uploader

> A drag and drop multiple file uploader component that uses Vue.js v2 and Axios. Uploader shows file names, sizes and total size of files added. It also allows
 setting a minimum required number of files to upload.

### Demo
See live demo [here](https://abarta.github.io/vue2-multi-uploader/demo/).

### Latest
PostData and other changes contributed by [SergioReis97](https://github.com/SergioReis97) via PR. Thanks!
Message props contributed by [Mushood](https://github.com/Mushood) via PR. Thank you!

Optional `maxItems` prop added to allow setting a maximum number of files allowed per upload.  
Default `maxItems` is set to 30.

Optional `method` prop allows PUT method to be used. Default method remains POST, if you want to use PUT just add `method="put"` to your template.

Optional `postMeta` prop added so you can include additional metadata that needs to be sent along. This prop can be in the form of a string, array or object and empty `postMeta` data is not sent. To pass a string use `:postMeta="'string'"`, to include an array you should use `:postMeta="['value']"` and for an object use `:postMeta="{name: 'value'}"`.

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

| Prop name        | Type           | Required  | Default  
| ------------- |:-------------:| -----:| -----:|
| postURL      | String |  yes |  -
| successMessagePath      | String    |   yes | -
| errorMessagePath | String     |    yes | -
| minItems | Number     |    no | 1
| maxItems | Number     |    no | 30
| method | String     |    no | POST
| postMeta | String, Array, Object     |    no | -
| postData |  Object  |    no | -
| showHttpMessages | Boolean     |    no | true
| postHeader |  Object     |    no | null

### Message Props
All text in the component is also configurable. Below is the list of available props that can be configured, if necessary. Default values are provided for each prop.

| Prop name         | Type            | Required    | Default  
| -------------     |:-------------:  | -----:      | -----:|
| headerMessage     | String          |    no       | Add files
| dropAreaPrimaryMessage  | String    |    no       | Drop multiple files here.
| dropAreaSecondaryMessage | String   |    no       | or click to upload
| fileNameMessage   | String          |    no       | Names
| fileSizeMessage   | String          |    no       | Sizes
| totalFileMessage  | String          |    no       | Total files:
| totalUploadSizeMessage | String     |    no       | Total upload size:
| removeFileMessage | String          |    no       | Remove files
| uploadButtonMessage  | String       |    no       | Upload
| cancelButtonMessage | String        |    no       | Cancel
| fileUploadErrorMessage   | String   |    no       | An error has occurred
| minFilesErrorMessage   | String     |    no       | Minimum files that need to be added to uploader
| maxFilesErrorMessage  | String      |    no       | Maximum files that can be added to uploader
| retryErrorMessage | String          |    no       | Please remove the files and try again.
| httpMethodErrorMessage | String     |    no       | This HTTP method is not allowed. Please use either 'put' or     'post' methods.


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
You can modify the minimum number of files required for the upload to take place by changing the value of minItems prop. Default is set to 1.
Here is an example template for uploading a minimum of 5 items and a maximum of 10 items:
``` html
<multiple-file-uploader postURL="http://.." successMessagePath="" errorMessagePath="" :minItems="5" :maxItems="10"></multiple-file-uploader>
```
### Events
Fires `upload-success` or `upload-error` respectively. Success handler receives axios response object. Error handler receives axios error object.
```html
<multiple-file-uploader postURL="http://.." successMessagePath="" errorMessagePath="" @upload-success='success_handler'></multiple-file-uploader>
```
```javascript
	...
	success_handler: function(response){

	},
	...
```

### Dependencies
Axios, ES6-Promise

### CSS
CSS style is not scoped so it's easy for you to overwrite your own style.
Bootstrap CSS is used in demo but not required for the component.

Class dropAreaDragging is active for giving some user feedback.
Example:

```
.dropAreaDragging{
   background-color:#ccc;
}
```

### LICENSE

---
The MIT License (MIT)

Copyright (c) 2017 UPDIVISION

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
