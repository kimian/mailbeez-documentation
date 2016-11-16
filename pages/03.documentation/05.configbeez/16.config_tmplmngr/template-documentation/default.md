---
title: template documentation
published: true
template: docs
# theme: false
visible: false

process:
    twig: false
---



# Building Element Subtemplates

Element Subtemplates are the buildingblocks you can use in the visual editor to build the email templates.


Element Subtemplates are located in 

    /mailhive/configbeez/config_editor/elements/


e.g.

    /img_fullwidth/img_fullwidth.tpl.html
    

When inserting an element through the visual editor the smarty tags with {{ ... }} delimiters are processed once, e.g.
    
`{{$id}}` - inserts a unique id for this element
`{{$id + 1}} - inserts a unique id for the next element
    
    
"Normal" Smarty tags with delimiters `{ ... } are processed during the email generation.


Thanks to Editor Tags, that can be used within the subtemplate, the visual editor is able to generated dynamically a GUI for editing:


`[CONTAINER] ... [/CONTAINER]`  marking a container, which can be moved or deleted


`[CONTAINER_CONTROLS] ... [/CONTAINER_CONTROLS]` optional, marks where the controls-code are inserted in edit mode, by default directly following the `[CONTAINER]` tags


`[EDIT_TEXT title="coupon_text" id="{{$id+1}}"] ... [/EDIT_TEXT]` - used within a CONTAINER. the included text can be edited through a wysywig editor


`[EDIT_COMPLEX title="MyComplexEditor" id="{{$id}}"] .. [/EDIT_COMPLEX]` - used within a CONTAINER. Marking a complex editor section with multiple variables to edit

`[EDIT_COMPLEX_CONTROL] .. [/EDIT_COMPLEX_CONTROLS]` - optional, used within an EDIT_COMPLEX section , marks where the edit controls-code is inserted in edit mode, by default directly following the `[EDIT_COMPLEX]` tags


`[EDIT_COMPLEX_SECTION title="my Section"]` - optional, introduces a Section divider

`[EDIT_COMPLEX_GROUP sort="20" title="my Section"] .. [/EDIT_COMPLEX_GROUP]` - **NOT IMPLEMENTED YET** optional, grouping included fields into a tab
    

`[VAR_IMGSRC id='1' title='Image Url']..[VAR_IMGSRC]` - used within an EDIT_COMPLEX section, field with browser to select an image url

    example:
    
    <img src="`[VAR_IMGSRC id='1' title='Image Url'][##$catalog_server##][##$mailhive_path##]images/bugsbunny.png[/VAR_IMGSRC]`">


`[VAR_SWITCH id='1']ON[/VAR_SWITCH]` - used within an EDIT_COMPLEX section, toggle control within value ON|OFF

    example:
    
    {assign var="toggle_margin" value="[VAR_SWITCH title='add divider' id='1']ON[/VAR_SWITCH]"}
    {if $toggle_margin == 'ON'}
        <hr>
    {/if}


`[VAR_STRING id='1' title='Caption']...[/VAR_STRING]` - used within an EDIT_COMPLEX section, edit a single line text

    example:
    
    <img src="..."  alt="`[VAR_STRING id='1' title='Caption']Image Caption[/VAR_STRING]`">
    
    
`[VAR_COLOR id='1' title='Background-Color']...[/VAR_COLOR]` - used within an EDIT_COMPLEX section, colorpicker       

    example:
    
    <td bgcolor="`[VAR_COLOR id='1' title='Background-Color']#c0c0c0[/VAR_COLOR]`"> ...</td>
    
    
`[VAR_FONT id='1' title='FontFace'] ... [/VAR_FONT]` - used within an EDIT_COMPLEX section, fontface picker

    example:
        
    <h1 style="font-family: `[VAR_FONT id='1' title='FontFace']Arial[/VAR_FONX]```"> ...</h1>
        
        
If you want to nest fields or want to use fields multiple times you can achieve this by using smarty variables:

    example:
 
    [CONTAINER]
        [EDIT_COMPLEX title="Full Width" id="{{$id}}"]
        {assign var="fontcolor" value="[VAR_COLOR id='1' title='Font-Color']#ffffff[/VAR_COLOR]"}
            [VAR_TEXT id='1' title='myText']
                <h1 style="color:{$fontcolor};">Section Title</h1>
                <h3 style="color:{$fontcolor}">Subtitle</h3>
            [/VAR_TEXT]
        [/EDIT_COMPLEX]
    [/CONTAINER]