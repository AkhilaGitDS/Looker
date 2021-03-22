**+Editing and validating LookML Using the IDE: +**

Looker’s integrated development environment (IDE) has various features to help us in writing LookML.

+*Autosuggest:-*+

As we type, the IDE advise possible parameters and values that are sensitive to the conditions of what we are typing. 
For example, the advises for a dimension’s type parameter will only include valid options for that parameter. Also, fields in *sql* parameters have to be marked with ${...}, so the IDE adds that syntax when suggesting fields. Autosuggest automatically pop-up wherever it can be shown. To close it, press the Esc key on your keyboard. To view it at any point, press Ctrl+Space (Windows). Here is an instance:

<img src="/Images/LookML_AutosuggestIDE.png" width=500 hieght=700>

+*On-the-fly error checking:-*+

The IDE grasp syntax errors as we type. A red X in the spillway indicates a syntax error, which is underlined in red. When mouse pointer fly over the red X, a short description of the error appears. The LookML Validator is still required to complete a full model validation. Some errors, such as an invalid field reference due to a missing join, require a detail(thorough) look at the model and therefore are only come-up when the LookML Validator is run.Here is how error appears in tool:

<img src="/Images/LookML_ErrorCheckIDE.png" width=450 hieght=500>

+*Context-sensitive help panel:-*+

On the right side of the IDE is a context-sensitive help panel that actively updates based on the place of our cursor. The help panel provides the following:
+ A explanation of the LookML parameter.
+ A list of all possible subparameters or a list of allowed values.
+ Links to the documentation pages for the parameter and all subparameters. 
This is how QuickHelp in IDE looks :

<img src="/Images/LookML_QuickHelpIDE.png" width=550 hieght=700>
