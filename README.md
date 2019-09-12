# Land cover chart generator

The LibreOffice macro in this repository generates a set of image files with charts and tables that can be included in a community-specific report on land cover and canopy potential. The community-specific input data is generated as a csv file (I'm not sure how). The macro pastes the input data into a "template" spreadsheet, which regenerates the charts and tables within the spreadsheet. Finally the macro exports those charts and tables to a set of JPG files. 

## Important files
1. extensions/canopy_chart_generator.oxt  This LibreOffice extension contains all of the BASIC code and forms that comprise the macro
2. template/Template This spreadsheet contains the "template" for converting input data into the desired charts and tables. 

## Prerequisites
1. LibreOffice installed (tested with version 6.1.6.2 x64)
2. Git repository cloned

## Installation
1. Start LibreOffice Calc
2. Install the extension
    - Tools -> Extension Manager -> Add
    - Specify [path to git clone]/extensions/canopy_chart_generator.oxt and click OK
3. Set the output directory (where the generated images will be saved).
    - Tools -> Macros -> Edit Macros
    - My Macros & Dialogs -> CanopySummaryChartGenerator -> Basic Code -> Show Dialog
    - Edit the line that specified the output directory: ![Alt text](/images/screenshot_output_dir.jpg?raw=true "Edit output directory") 
4. Create a shortcut to run the macro
    - Tools -> Customize, Toolbar Tab
    - Category: Macros (at the bottom of the list)
    - Function: My Macros -> CanopySummaryChartGenerator -> BasicCode -> ShowDialog -> Click right arrow to add to Function list on right
    - Highlight ShowDialog and modify the icon to [path to git clone]/images/tree_icon.png
    - Highlight ShowDialog and modify the name to something more meaningful such as CanopyCharts. You should see the macro shortcut on your tool bar ![Alt text](/images/screenshot_tree_icon.jpg?raw=true "Macro shortcut")
    
## Operation
1. Generate the input csv. It should look like this (there are files in the test subdirectory that can be used as an example):
![Alt text](/images/screenshot_input_csv.jpg?raw=true "Input csv file")
2. Open the template in LibreOffice Calc 
3. Click the macro shortcut. This dialog should appear: ![Alt text](/images/screenshot_macro_dialog.jpg?raw=true "Macro dialog")
4. Point to the input csv file and fill in the square mileage of the community then click "Import data and generate charts"
5. You may see the data in the template being updated then finally a message to confirm the images were generated
6. The images will be in the designated output directory ![Alt text](/images/screenshot_output_files.jpg?raw=true "Output files")
7. You can now run the macro against another set of data or exit. When exiting it is probably best to discard any changes that the macro made to the template

## Updating
When installing an update to the macro, go through the same steps listed in the Installation section to install the extension and update the output directory. Unless there was a major change, the macro shortcut should still work. 
