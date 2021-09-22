---
title: Settings
---

- Settings view is displayed to user when the node is selected in a project view (unless hidden by the user). 
- User can alter settings at anytime. 
- Settings are saved **only** when the node is executed by clicking "Batch run", "Import data" on "Run for this" buttons.



## settings.html
Settings are defined in settings.html in plain html. Settings can also have interactive elements.

**NOTE: Only inputs with class "node-settings" are sent to the GLAMpipe**. 

	<input class="node-settings dynamic_field" name="my_setting" \>


**NOTE: If you add a "dynamic_field" class to a select, then that select is filled with current collection fields.** 

Here are part of the settings of the Script node:

    <setting>
        <settinginfo>
            <settingtitle>
                Example setting: field selection (in field)
            </settingtitle>
            <settinginstructions>
                Choose a field from record fields.<br>
                In your script you can get the value of the field like this: <br>
                <strong>context.doc[context.node.settings.in_field]</strong>
            </settinginstructions>
        </settinginfo>

        <settingaction>
            <label>record field</label>
            <select name="in_field" class="node-settings dynamic_field">
                <option value="">choose field</option>
            </select>
        </settingaction>
    </setting>


### Access settings

If node has input named "separator" in settings view, the value is then later accessible in node scripts via context object like this:

	var sep = context.node.settings.separator;


