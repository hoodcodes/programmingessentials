##### Documentation

“Redundant comments are just places to collect lies and misinformation.” 
― Robert C. Martin, Clean Code: A Handbook of Agile Software Craftsmanship

“I’ve learned over the past few years that comments should be considered smells.” 
― Ron Lisle

"Code never lies, comments sometimes do." - Ron Jeffries 

Documenting Code Notes	


This was interesting to read the MS docs on everything available in XML Documentation:  https://docs.microsoft.com/en-us/dotnet/csharp/codedoc  

Normally, I use what is provided automatically and most commonly:
<summary>
<param>
<returns>  

Several tags I never knew existed:
<remarks> - supplements the info about types/members that the <summary> tag provides.
<value>  - Similar to the <returns> tag,  intended for your properties
<example> - include an example in your documentation.  This also involves using the child <code> tag.
<para> - for formatting content within its parent tag.  Divides text into paragraphs.
<exception> - so you can let your developers know that a method can throw specific exceptions.
<c> - you can make part of text as code.  Like the <code> tag but inline.
<see> - lets you create a clickable link to a doc page for another code element.  
<seealso> - used in the same way as <see>.
 <permission> - lets you document the access of a member.  




MS recommendations:
Document all publicly visible types
If you document private members - you expose the inner (potentially confidential) workings of your library. - So, in general - don’t.
Bare minimum: have a summary tag for Intellisense.  
Use complete sentences with full stops.
Partial classes are fully supported.  Documentation is concatenated into a single entry for that type.
Compiler verifies the syntax of these tags:
<exception>
<include>
<param>
<see>
<seealso>
<typeparam>


Some FYIs:
If you want angle brackets to appear in the text of a documentation comment, use the HTML encoding of < and > which is &lt; and &gt; respectively.  Example:  
/// <summary>
/// This property always returns a value &lt; 1.
/// </summary>





References:
https://docs.microsoft.com/en-us/dotnet/csharp/codedoc 
https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/xmldoc/index
https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments



