# Field Day, a plugin for Movable Type

> **About this fork:** The original
> [movabletype/mt-plugin-field-day](https://github.com/movabletype/mt-plugin-field-day)
> repository is archived. This fork adds a fix for a long-standing bug where a
> `<mt:EntryField>` (or other `Field`/`FieldGroup`) block that produces no
> output makes publishing fail with an empty error. The usual trigger is a
> block containing only `<mt:SetVarBlock>`:
>
>     <mt:EntryField field="hosts"><mt:SetVarBlock name="ids" function="push"><mt:EntryFieldValue></mt:SetVarBlock></mt:EntryField>
>
> The old workaround was a space before `</mt:EntryField>`, which adds stray
> whitespace to your output. With this fix the space is no longer needed. The
> change is in `plugins/FieldDay/lib/FieldDay/Template/PubTags.pm`.

* Author: Six Apart
* Copyright: 2008-2013 Six Apart Ltd.
* License: MIT
* Site: <http://www.movabletype.org/>


## Overview

FieldDay is a plugin for Movable Type that lets you add more fields to the MT
interface.


## Features

How is Field Day different from MT's built-in "Commercial Pack" implementation
of custom fields?

* You can define fields for templates, assets, comments, and blogs, as well as
  system-wide fields.
* Linked object field types let you connect any supported object type to any
  other.
* By organizing fields into groups and allowing multiple instances of each
  group, you can allow users to associate an unlimited amount of data with a
  given object.


## Documentation

* Field Day Basics: <http://github.com/movabletype/mt-plugin-field-day/wiki/Basics>
* Field Day Developer Notes: <http://github.com/movabletype/mt-plugin-field-day/wiki/Developer-Notes>


## Installation

1. Move the `FieldDay` plugin directory to the MT `plugins` directory.
2. Move the `FieldDay` mt-static directory to the `mt-static/plugins`
   directory.

Should look like this when installed:

    $MT_HOME/
        plugins/
            FieldDay/
                [plugin files here]
        mt-static/
            plugins/
                FieldDay/
                    [plugin static files here]


## Support

This plugin is not an official Six Apart release, and as such support for this
plugin is not available.
