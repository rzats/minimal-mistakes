---
title: "Google Summer of Code 2016 Final Report"
layout: single
type: posts
author_profile: true
comments: true
category: gsoc
share: true
related: true
excerpt: "A final report about my contributions to MovingBlocks as a part of Google Summer of Code 2016."
sitemap: false
permalink: /gsoc/2016-final-report
---

<hr />
**Organization:** MovingBlocks

**Project:** Standalone NUI extraction and visual NUI editor

**Product:** Terasology

<hr />

![Terasology's Gooey mascot]({{site.url}}/images/gsoc_2016_gooey.png)
<font color="gray" size="2"><i>Gooey - Terasology's cute slimy mascot!</i></font><br>

[Terasology](https://github.com/MovingBlocks/Terasology) is an open-source sandbox videogame, originally created as a Minecraft-inspired tech demo, later growing into a stable engine for voxel-based gameplay. The project's focused on architecture and extensibility, but as of early 2016 has released a first Alpha version to be a baseline engine for creating content and building gameplay on.

Terasology uses its' own NUI (New UI) framework for constructing and rendering user interfaces. The framework, while being a stable library with a significant selection of widgets and APIs, has relied on editing text files and (repeatedly) re-running the game to see how the edits turn out. Therefore, a standalone editor with a preview option has been proposed as a GSoC project. Having written a [proposal](https://github.com/rzats/gsoc-nui-editor/blob/master/Proposal/MovingBlocks-rzats-Visual-NUI-Editor.md) for the project - the only one I prepared for Google Summer of Code 2016 - I got selected to participate in this year's program.

Throughout the summer I've created an in-game visual editor for NUI elements (individual UI windows) as well as skins (collections of styles similar to CSS), allowing developers and modders to edit existing interface elements or create new ones with instant feedback being displayed in the editor as well as in-game. A short summary of the finished product can be found [here](https://github.com/Terasology/TutorialNui/wiki/Editor-Overview), and a more detailed feature set - [here](https://github.com/Terasology/TutorialNui/wiki/Editor-Quick-Start).

In addition to this, after some investigation I've created a [checklist](https://github.com/MovingBlocks/Terasology/issues/2307) of dependencies that need to be resolved in order to extract NUI into a separate library: while throughout the coding period I've mainly focused on the NUI editor, I'm planning to return to this checklist after this year's GSoC.

**Contribution Summary**

A complete list of my commits to the project can be found [here](https://github.com/MovingBlocks/Terasology/commits/develop?author=rzats), though it includes unrelated contributions before GSoC (and will likely include numerous future contributions!).

![GitHub LOC stats]({{site.url}}/images/gsoc_2016_loc_stats.png)
<font color="gray" size="2"><i>Git commit statistics for fun! (Disclaimer: may or may not be inflated by Apache headers)</i></font><br>

The pull requests relevant to the NUI editor (and related APIs) are:

**Pull Request ID** | **Summary**
[2338](https://github.com/MovingBlocks/Terasology/pull/2338)| An initial implementation for `UITreeView` - a core component of the editor
[2348](https://github.com/MovingBlocks/Terasology/pull/2348)| Followup PR to fix a silent null pointer exception
[2349](https://github.com/MovingBlocks/Terasology/pull/2349)| A `UITreeView`↔JSON serializer/deserializer; buttons to expand/contract tree view nodes
[2355](https://github.com/MovingBlocks/Terasology/pull/2355)| Improvements to the tree view APIs based on mentor feedback
[2360](https://github.com/MovingBlocks/Terasology/pull/2360)| Initial implementation for the NUI editor
[2375](https://github.com/MovingBlocks/Terasology/pull/2375)| A hotkey setup to run the editor
[2391](https://github.com/MovingBlocks/Terasology/pull/2391)| Context menu interface - needed for the editor but designed for general use
[2408](https://github.com/MovingBlocks/Terasology/pull/2408)| Icons for the editor tree view based on node types
[2409](https://github.com/MovingBlocks/Terasology/pull/2409)| Removes an obsolete testing screen - at this point the editor is the main testing environment
[2415](https://github.com/MovingBlocks/Terasology/pull/2415)| Smart "Add..." options based on node types
[2428](https://github.com/MovingBlocks/Terasology/pull/2428)| Minor tweaks based on mentor feedback
[2432](https://github.com/MovingBlocks/Terasology/pull/2432)| Skin editor based on the main screen editor
[2438](https://github.com/MovingBlocks/Terasology/pull/2438)| Documentation and implementations for the remaining feature set from the proposal
[2448](https://github.com/MovingBlocks/Terasology/pull/2448)| Backup & autosave functionality for the screen and skin editors
{: .text-center}
<br />

**Future Plans and Ideas**

Some of the areas I'll be working on in the future are:

- Adding additional visual feedback to the editor - for instance, clicking a widget in the editor area should select it in the preview widget and vice versa.
- Extracting the NUI framework into a standalone [repository](https://github.com/MovingBlocks/TeraNUI).
- Documenting the NUI framework from scratch, including Javadocs and [wiki tutorials](https://github.com/Terasology/TutorialNui/wiki).
- Continuing my [work](https://github.com/MovingBlocks/DestinationSol/pull/92) on integrating the [gestalt](https://github.com/MovingBlocks/gestalt) family of libraries into the open-source game [Destination Sol](https://github.com/MovingBlocks/DestinationSol).

Apart from that, I'll be on the lookout for other opportunities, major or minor, to contribute to MovingBlocks and FOSS in general!

**Acknowledgements**

I'm very thankful to my mentors, [Florian Köberle](https://github.com/flo) and [Rasmus Praestholm](https://github.com/Cervator). Their continuous support and guidance throughout the summer has been truly invaluable! I'd also like to thank <span style='color:#4885ed'>G</span><span style='color:#db3236'>o</span><span style='color:#f4c20d'>o</span><span  style='color:#4885ed'>g</span><span style='color:#3cba54'>l</span><span  style='color:#db3236'>e</span> for the wonderful opportunity to work on FOSS.

Thank you all!
