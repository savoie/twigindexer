# twigindexer
A slightly hacky web interface to easily collaborate on a yearbook index using google spreadsheets.

##How to:
1. Create a google spreadsheet with two worksheets:
  * 'Names', with one column: first cell in the column containing the header 'Name', followed by a list of indexable names.
  * 'Pages', with two columns: 'Page', followed by a list of page numbers, and 'Names': the text of each page to be indexed.
2. Go to File > Publish to the Web > Publish
3. Copy the ID of the spreadsheet (the bolded bit in the URL: /spreadsheets/d/**110COAd1mCVUHQ0zURb0T8iNAxLvYUY7RGA5Cu08gCaQ**/edit#gid=0) into http://savoie.github.io/twigindexer/
4. If your spreadsheet is perfectly spelled and contains only indexable text, you're done. The app has generated you an index! Otherwise see the next section.

## Dealing with an imperfect spreadsheet
1. There may be some text in your pages that doesn't match the names list. The app handles these on a page-by-page basis:
  * Highlighted in **green**: this text matches a full name in your names list. This *will* be indexed.
  * Highlighted in **red**: this text seems significant but is ignored because it doesn't match anything. Check to be sure it's spelled correctly. This *will not* be indexed. (hint: this means you can copy the entire text of a page into your spreadsheet and the app will automatically pick out names and ignore blurbs! Plus it will help you tidy up your spreadsheet, see step 3)
  * Not highlighted: ignored.
2. If there's something in red that the app should index, click *Modify* and edit the page text to fix spelling errors. (Also remember to fix them in the actual book!)
3. Clicking *Export Changes* will give you a prettified version of your pages worksheet, with only the green-highlighted stuff. Copy-paste this to replace the Pages worksheet if you want to skip the editing step next time.
