# Land cover chart generator

The LibreOffice macro in this repository generates a set of image files with charts and tables that can be included in a community-specific report on land cover and canopy potential. The community-specific input data is generated as a csv file (I'm not sure how). The macro pastes the input data into a "template" spreadsheet, which regenerates the charts and tables within the spreadsheet. Finally the macro export those charts and table to JPG file. 

## Important files
1. extensions/canopy_chart_generator.oxt  This LibreOffice extension contains all of the BASIC code and forms that comprise the macro
2. template/Template This spreadsheet contains the "template" for converting input data into the desired charts and tables. 

## Prerequisites
1. LibreOffice installed (tested with version 6.1.6.2 x64)
2. Git repository cloned

## Installation
1. Start LibreOffice Calc
2. Tools -> Extension Manager -> Add
3. Specify [path to git clone]/extensions/canopy_chart_generator.oxt and click OK

## Operation
