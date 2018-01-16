# MultiSelectDialog
A multi choice select dialog with Search and Text highlighting

Features
--------
* Provides Multi selection Dialog
* Search through list
* Highlighted the search text

Demo
--------
For a working implementation of this project see the `app/src/` folder.

<img src="ezgif.com-video-to-gif.gif">


Setup
--------

Gradle:

```
    dependencies {
         compile 'com.abdeveloper:multi-select-dialog:1.0'
    }
```

Usage
--------
See Sample in SampleApplication
```
MultiSelectDialog multiSelectDialog = new MultiSelectDialog()
                .title("your string") //setting title for dialog
                .titleSize(20) //setting textSize
                .positiveText("Done") //setting Submit text
                .negativeText("Cancel") //setting Cancel text
                .preSelectIDsList(alreadySelectedCountries) //List of ids that you need to be selected
                .multiSelectList(listOfCountries) // the multi select model list with ids and name
                .onSubmit(new MultiSelectDialog.SubmitCallbackListener() {
                    @Override
                    public void onDismiss(ArrayList<Integer> ids) {
                        //will return list of selected IDS
                        for(int i=0;i<ids.size();i++){
                            Toast.makeText(MainActivity.this,"Selected Ids : " + ids.get(i),Toast.LENGTH_SHORT).show();
                        }
                    }
                });

```


License
--------

    Copyright 2017 Abubakker Moallim

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.