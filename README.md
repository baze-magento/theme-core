# *Core* Theme
Provides the core theme functionality to support bazedk's addon modules, when necessary. 

# Architecture
Modules that require theme changes <- **Core theme** (This Repo) -> Child "skin" themes

Standalone modules -> (no dependencies)

# Instructions
Other Modules MUST NOT include any changes to Template files, CSS, or similar. These should all be contained within the Theme. 

This base Theme MAY reference Configuration Options from any Modules.

Any references to Options that aren't included in standard Magento MUST fall back to defaults so that the Theme can function without the Module, and they MUST include a comment with the Module's Name for searchability.

----

When writing Composer dependencies, this Theme MUST NOT declare a dependency on feature-specific modules.

If this Theme makes reference to the Options of one of our Modules, and this is required for that Module to work correctly, the Module MUST declare a dependency on this Theme.
