This routine can be used to find a string of characters in a field ( e.g. hashtags in a description field
and store those in an new table (e.g. a hashtag table) with a link to the record where the string was found
It can also be used to find other character strings than hashtags, eg. CR-1234 or @P1234, see setting
of parameters below. The resulting string of records needs to be comprised
of ASCII characters (A-Z,a-z) and digits (0-9) only, with the exception of the hyphen which is also allowed
(e.g. REC-1234)

The routine works with the following parameters:
 CALL CreateMarker(SourceTable, SourceField,TargetTable, TargetColumn, KeyColumnName, StringIdentifier, MinLength, WordSeparator) where
   SourceTable      = the table which contains the field to be searched
   SourceField      = the field to be searched
   TargetTable      = the name of the new table which will contain the found strings (e.g. Hashtags)
   TargetColumn     = the field in the new table which will contain the found strings (e.g. Hashtags)
   KeyColumnName    = the field which links the SourceTable and TargetTable
   StringIdentifier = the string with which a substrings should start, e.g. # or @ etc. This can also
  					          be a longer string, e.g. CR- or #demo etc.
  					          If this parameter is not set it defaults to #
   MinLength        = the minimum length of the entire string to be found, defaults to 3
   WordSeparator    = the string of characters that separates words in the source field from each other.
                      If not set it defaults to a blank ' '

Make sure you don't use brackets [] for table or columns, leaving them in '' is sufficient if a table or columns name should be two words or more, e.g
* Call CreateMarker('Data Table','String Field','Hashtag Table','Hashtag Field','Key','#');
