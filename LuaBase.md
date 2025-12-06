---
tags:
  - Obsidian
  - PKSPKMS
  - Programming_Language/Java
  - Programming_Language/Lua
status:
  - Inactive
type:
  - Project
creationDate: 2025-08-21
modifiedDate: 2025-12-05
published: 2025-12-02
access: Public
digitalGarden: Seed
---

Why must I write [[JavaScript]] to define conditions in an embedded DSL not directly related to the web? Must I use the lingua franca of the web everywhere? Instead, I have made my own version of [Obsidian](./Obsidian.html)'s [Base](https://help.obsidian.md/bases) using [[Lua]] instead of JavaScript in another project of mine, [PKSPKMS](./PKSPKMS.html). Woe unto me.

It's wrapped up inside [PKSPKMS](./PKSPKMS.html) and very fragile. I think it could be refactored out easily into a separate library (translation from Obsidian specific file property names would need to be sorted out too). I don't know it's useful for anyone but me though.

I'm not very good at writing Lua, I'm fine at [[Java]] and joining the skills inside another programs operations has resulted in code that is *in need of improvement*.

## Why

I want to be able to write my own parser for Obsidian Bases syntax so I can use it's features outside of Obsidian but, oh pooh, it's JavaScript. I don't want to stick a browser or a JS engine in somewhere. I think Lua's a better option. It's easier for me to implement and embed. I get to make something too.

## Example

Example, modified version from the Base docs:

```yaml
filters:
  or:
    - 'hasProperty(file, "tag")'
    - and:
	    - 'hasPropertyValue(file, "tag", "book")'
	    - 'hasPropertyValue(file, "link", "Textbook")'
    - not:
        - 'hasPropertyValue(file, "tag", "book")'
        - 'hasPropertyValue(file, "folder", "*/Required Reading/*")'
formulas:
  formatted_price: 'if hasProperty(file, "price") then return string.format("%.2f", file:get("price")) .. " dollars" end'
  ppu: "toFixed((file:get('price') / file:get('age')), 2)"
views:
  - type: table
    name: "My table"
    limit: 10
    filters:
      and:
        - 'file:get("status") != "done"'
        - or:
            - "formula:ppu(file) > 5"
            - "file:get('price') > 2.1"
    order: # note order differs that it returns how to get the value, then the column name
      - 'file:get(name), "Name"'
      - 'file:get(ext), "Ext"'
      - 'file:get(age), "Age"'
      - 'formula:ppu(file), "PPU"'
      - 'formula:formatted_price(file), "Price'
```

Internally, it runs each of the `filters` values as expressions and `order` creates a function that returns a value for the column and name of the column (Lua supports multiple return values from functions).

## Functions

Lua functions loaded before expressions are ran:

```lua
function hasProperty(file, prop_name)  
    return file:get(prop_name) ~= nil
end  

-- doesn't work for arrays, TODO: fix
function hasPropertyValue(file, prop_name, value)  
    local val = file:get(prop_name)    
    if type(val) == "userdata" then
		return val:contains(value)    
	end    
	return val == value
end  

function getPropertyValue(file, prop_name, default_value)  
	local val = file:get(prop_name)  
	if val == nil then
		return default_value  
	end  
	return val
end
```

## Obsidian Base To LuaBase

PKSPKMS currently naively uses regex to convert expressions into their Lua equivalents. It's very faulty and error prone with very limited definitions.

Doesn't support:

 - Filters:
	 - Anything other than `and`
 - No `limit`
 - Sorts only by first column given
 - `displayName` to order (column) name not translated to LuaBase
 - Nearly all [functions](https://help.obsidian.md/bases/functions) not accounted for/implemented
