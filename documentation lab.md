# Documentation Lab
## Instructions
In this lab, we'll practice reading documentation and looking for answers to our questions in the following documentation sources:
1. [CollectionBuilder documentation](https://collectionbuilder.github.io/cb-docs/)
2. [SUCHO documentation](https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template)
3. [Alex's TEI guidelines for archival transcription](https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/)

Answer the following questions using the documentation above. Turn in your completed Markdown file to the assignment on Canvas.
## Collection Builder
***For all answers in this section, give the answer and the URL of the page where you found it.***

1. **Which fields are required for *all items* in CollectionBuilder-GH metadata?**  
objectid, filename, title, format.  
https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/#required-fields-for-collectionbuilder-gh-and-sheets
2. **What file do you need to edit to add a new page to your navigation bar?**  
Go to the "_data” directory and open the “config-nav.csv" 
https://collectionbuilder.github.io/cb-docs/docs/pages/add_page/#add-a-new-page-to-the-nav
3. **What metadata fields are required to support the map visualization in CollectionBuilder-GH metadata?**  
latitude, longitude, date, subject, and location.  
https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/#fields-required-for-visualizations
4. **What four columns are included in the config-metadata.csv file?**  
field, display_name, browse_link, and external_link.  
https://collectionbuilder.github.io/cb-docs/docs/customization/config-metadata/#metadata--item-page-configuration-config-metadatacsv
5. **If you wanted a metadata field called "archive" in your metadata field to display as "Holding Institution" in the metadata section of each item's page, what file would you edit? (Bonus point: what columns of that file would you edit and what text would you input in each column?)**  
display_name and external_link (if applicable). Quoted from the documentation, "if you’d like the field “original-collection” to appear as “Original Archival Collection” on the item page, you’d enter Original Archival Collection in the second column," and then edit the external link to contain the desired title as well.  
https://collectionbuilder.github.io/cb-docs/docs/customization/config-metadata/
6. **How should the date September 8, 2023 be formatted so that the timeline visualization works?**  
`yyyy-mm-dd` or `mm/dd/yyyy`.  
https://collectionbuilder.github.io/cb-docs/docs/metadata/gh_metadata/#date
7. **What column in what file allows you determine whether a field can be used for sorting on the Browse page of your website?**  
`sort_name`; fifth column.  
https://collectionbuilder.github.io/cb-docs/docs/customization/config-browse/#sort_name
8. **How do you change which metadata fields contribute values to the "Subjects" visualization page?**  
Choosing metadata fields and listing them under "subjects-fields" in "_data/theme.yml"  
https://collectionbuilder.github.io/cb-docs/docs/theme/subjects/#subjects-fields
9. **What three items (keys) are in the YAML front matter of any of the markdown page files?**  
title, layout, and permalink.  
https://collectionbuilder.github.io/cb-docs/docs/pages/basics/#yaml-front-matter
10. **When filling in "metadata: " with the name of your metadata sheet on your "\_config.yml" file, should you include the file extension?**  
No.
https://collectionbuilder.github.io/cb-docs/docs/config/collection/#metadata
11. **Which file controls the display options for most of your website?**  
"_data/theme.yml"  
https://collectionbuilder.github.io/cb-docs/docs/theme/#theme-configuration-options
12. **How can you separate multiple values in a single field in your metadata file?**  
A semicolon.
https://collectionbuilder.github.io/cb-docs/docs/metadata/formatting/#formatting-your-metadata
13. **Find the example code for including a PDF from your collection (with a caption) on one of your interpretive pages (hint: start with the "Feature Includes" page)**  
```
{% include feature/pdf.html objectid="demo_002" width="50" caption="a pdf from the collection" %}
```  
https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html

## SUCHO Metadata
1. **Which metadata fields are always required for a SUCHO item?**  
Progress, Claimed by, title, identifier, subject headings, original subject headings (if present), creator (if present), date (if present), language (if applicable), source URL, host institution, host location, original description (if present), description.  
https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template
2. **What character separates multiple values in Column E and Column F?**  
semi-colons  
https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template (See Column E and Column F sub-headings)
3. **Format the name "Yevhen Federovych Stankovych" according to the content guidelines for Creator**  
Stankovych, Yevhen Federovych  
https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template  
(See Column G Creator)
4. **What is the cardinality of the field "date?""**  
3, `YYYY-MM-DD`. 
https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template
5. **What would be the correctly formatted value for the field "Host Location" for an item held by an institution in Lviv, the capital of Ukraine's Lviv Oblast?**  
Lviv (Q36036)  
Copy the city name and Q-code from the top of the page and paste into the cell.  
https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template  
(See Column L Host Location)
6. **If you wanted to indicate that you were working on a row in our metadata spreadsheet, how would you do that?**  
Choose "In Progress" from drop down option in column A  
https://wiki.sucho.org/en/tutorials/internet-archive/spreadsheet-metadata-template  
(View table at end; Column A's Description)

## Alex's TEI guidelines
1. **What tag should be used to indicate deleted text?**  
"`<del>` is used to indicate deletions in the text. Surround the deleted letter, word, phrase, or lines with `<del>`."  
https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#deletions-del
2. **When should `<damage>` be used instead of `<gap>`?**  
"<damage> should be used when there is physical damage to the text (torn pages, holes, ink burn, wormholes, etc.) but it is still possible to read the text with certainty. Use @type to indicate the type of damage. <damage> can encompass all or parts of words (i.e., <damage> can begin and/or end in the middle of a word)."  
https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#damage

3. **How would you indicate that a word is repeated in the following code block?**
```xml
<p>
The quick brown fox jumped over the the lazy dog.
</p>
```  
"When a word or phrase is repeated by accident in the text, add @rend="repeated word" to the `<sic>`. No `<corr>` will be necessary."  
https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#corrections-sic-corr 

4. **Which tag is used to enclose an entire list of non-book items and which tag is used to enclose a list of books? Which tag should be used to enclose an individual non-book item, and which tag should enclose an individual book item?**  
"For non-book lists of items (e.g., inventories of household books), use `<list>` and `<item>`." For book lists, "A list of book items, regardless of whether there are line breaks between each item or not, should be enclosed in a `<listBibl>` and then each item inside a `<bibl>`." "If books and non-book items are mixed in the same list, open and close `<list>` and `<listBibl>` as necessary. It’s important to keep the books separate from other goods for data extraction."  
https://alexandraewingate.com/projects/encoding-guidelines-for-initial-archival-tei-transcription/#lists-structural-markup