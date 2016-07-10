---
layout: post
title: First Steps with Apps Script&#58; Read from and Write to a Spreadsheet
excerpt_separator: <!--more-->
---
With [Apps Script](https://script.google.com/) the Google Apps get a lot more powerful. Unfortunately, the first steps are not too easy. I found it fairly hard to grasp the mental model of how the scripts interact with the Apps. With a [little script](https://drive.google.com/previewtemplate?id=0AmvOCZ6UGJOsdEJjaFZHb3luSVBHUzBib0VwSzhGZWc&mode=public) and some accompanying description I hope to provide the right hints for everyone to successfully read data from a spreadsheet, do something with it and write the results back to the sheet.
<!--more-->
## Open the Script
For the sake of simplicity, I'll only regard so called [*container-bound* scripts](https://developers.google.com/apps-script/scripts_containers#containerBound). Container-bound scripts are essentially scripts that live and die with their container: the spreadsheet, in our case. Anyway, open the [script](https://drive.google.com/previewtemplate?id=0AmvOCZ6UGJOsdEJjaFZHb3luSVBHUzBib0VwSzhGZWc&mode=public) and navigate to its source code.

## Single Reads/Writes
In general a spreadsheet is used to perform calculations on multiple entries of the same format. Hence, the same operation is performed on the data within different cells. The more simple approach on accomplishing this is by reading the data from the cell, performing the calculation on that data, writing it back to the spreadsheet and then jump to the next cell to do the same. This approach is implemented in the function *doSingle()*.

## Batch Read/Write
However, single reads and writes are slow with App Script. Hence, it is recommended to [batch](https://developers.google.com/apps-script/best_practices#batchOperations "Batch Operations: Best Practice by Apps Script Developer Documentation") the entire read process and then also batch the entire write process. This approach is shown in the *doBatch()* function. It reads the value of all selected cells into an array. Within the two for-loops the values are transformed by a function. The results of calling that function are saved into another array. At the end the values of that other array are written back to the sheet in one go.