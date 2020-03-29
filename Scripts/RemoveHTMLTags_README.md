This routine can be used to clean a string of HTML tags from the input text.

The routine works with the following parameters:
CALL RemoveHTMLTags(InputText,VariableToBeUpdated)
where
 InputText           = the text to be changed
 VariableToBeUpdated = the name of the variable to be udpated.

 make sure you dont use brackets [], double quotes ", or reference the variable with $().

Examples:
 Call RemoveHTMLTags('TEXT','vCleanedHTML');

make sure you dont use brackets [] for table or columns, leaving them in '' is sufficient if a table or columns name shold be two words or more, e.g

 Inspired by: TylerR
   https://community.qlik.com/t5/Qlik-Sense-Documents-Videos/How-to-Efficiently-Clean-HTML-Tags-from-Your-Data-Source/ta-p/1688670  
