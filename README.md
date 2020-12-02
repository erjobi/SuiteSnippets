# <b>SuiteSnippets

This is an extention that contains snippets useful for writing SuiteScript 2.0 (or 2.X) for NetSuite.</b>

<li>All Information within these snippets was scraped from NetSuites Help Documents.

## Snippet Format

<ul>
<li><b>Prefix:</b>  SuiteScript method or property
<li><b>Description:</b> Information from the first table displayed in NetSuites help document for that particular method or property. (Description, Returns, Supported Script Types, Governance, etc.)
<li><b>Body:</b> 
<ul><li><b>Methods:</b> Display the piece of code needed to call them and provide tab stops to update options quickly
<li><b>Properties:</b> Generally provide a link to the NetSuite Help Documents 
</ul>
</uL>

# <b>Snippets</b>

You can type things like "**record.**" and you will see options for "**record.load**", "**record.copy**", "**record.attach**", etc.

<img alt="SuiteSnippets" width="850" src="https://raw.githubusercontent.com/erjobi/SuiteSnippets/master/updatedFullUse.gif" />

## <b>Snippet</b> Example

record.load(options)

<pre>
record.load({
    type: string*,
    id: number*,
    isDynamic: boolean true | false,
    defaultValues: Object
})</pre>

<b>Notes:</b>

<ul>
<li>First tab stop allows you to rename "record" to "r" or anything else you imported the module as
<li>After that, each value is a tab stop
<li>Default value of each key-value pair is the expected type
<li>Values ending with * indicate mandatory values
</ul>

# <b>Example Codes</b>

Also provided are code samples from the NetSuite Help Documentation.
<br>Simply add "x." to the begining of your results and you will see any code samples NetSuite has provided.

## <b>Example Codes</b> Example

x.record.load

<pre>
// Code Example 1
// Add additional code.
//...

// Load a sales order.

var objRecord = record.load({
    type: record.Type.SALES_ORDER, 
    id: 157,
    isDynamic: true,
});

// Load an instance of a custom record type with the ID customrecord_feature.

   var newFeatureRecord = record.load({
    type: 'customrecord_feature',
       id: 1,
       isDynamic: true                       
   });
...   
// Add additional code. 
</pre>

# <b>Enumerations</b>

Also provided are enumerations from NetSuite Help Documents.
<br>When typing in the prefix of the enumeration, select the Enum snippet to populate a list of available enumerations.

## <b>Enumeration</b> Example

record.Type
<img alt="enums" width="850" src="https://raw.githubusercontent.com/erjobi/SuiteSnippets/master/enums.png" />

# <b>CHANGE LOG</b>

<b>2020.2.0 - November 20 2020</b>

<ol>
<li> Changed Extension Versioning to mimic NetSuite releases
    <ul>
    <li>I intend to release a new update after each NetSuite release
    </ul>
<li> NetSuites 2020.2 Update included many updates to SuiteScript API
    <ul>
    <li>API changes/updates have been captured in this release
    <li>Please see <a href="https://www.system.netsuite.com/app/help/helpcenter.nl?fid=section_N3949604.html">[NetSuite 2020.2 SuiteScript Release Notes]</a>
    </ul>
<li> Added module names to snippet names to allow multiple snippets with the same name to function properly
    <ul>
    <li>Example: Field.Id is part of N/record, N/currentRecord, and N/ui/serverWidget
    <li>Previously, Field.Id for N/ui/serverWidget would overwrite the snippets for N/record and N/currentRecord
    <li>Now, all three are available 
    </ul>
<li> Examples now include a link to help docs
<li> Links to help docs now redirect correctly (using system.netsuite.com)
<li> serverWidget.fieldType ENUM was <i>actually</i> fixed this time
<li> Added link to buy me a coffee in SUPPORT section below :]
</ol>
<br>
<b>2.0.0 - August 10 2020</b>
<ul>
<li> NS 2020.1 Update included changes to SuiteScript - these have all been captured in this release
    <ul><li>Please see "NetSuite 2020.1 Release Notes"</uL>
<li> serverWidget.fieldType ENUM was missing some values - added missing values
<li> record.submitFields was missing a closing brace - updated
</ul>
<br>
<b>1.0.2 - May 27 2020</b>
<ul>
<li> Some enumerations were missing their choices - updated missing ones
<li> Some methods were showing a blank choice tab stop after them - found and removed the tab stop
<li> Updated Icon
</ul>
<br>
<br>
<b>1.0.1 - May 26 2020</b>
<ul>
<li> Example codes from help documents often include a line of "..." when NetSuite is indicating that there is code before/after the example. Updated these lines to "//..." so they are commented out by default.
</ul>
<br>

## <b>ABOUT ME</b>

Hi, my name is <i>Eric Birdsall</i>
<br>I'm a self taught programmer originally from upstate New York
<br><b>I believe in making tools that can be used to make tools</b>
<br> I hope you find this to be one of those tools
http://ericbirdsall.dev
<br><i>Please excuse my website, it is</i> <b>bad.</b>

<br>

## <b>SUPPORT</b>

A lot of time goes into maintaining this extension.<br>
It would mean the world to me if you [bought me a coffee](https://www.buymeacoffee.com/erjobi).


