# TS4 CAS Tools - updated to V3.8.2.0 on 3/18/2023 

## Additional Information
* This is a fork from MTS. 
* Original description by [CmarNYC](https://modthesims.info/member.php?u=3216596) who retired on earth and is now supporting the TS4 development in heaven.

### Requirements:
* XmodsDataLibSource (2023-03-18)

## Description

This is a full-purpose tool for creating CAS custom content for TS4. It's specifically meant to work with Milkshape 3D and to get around the limitations of using MS3D for Sims 4 meshes, but many of the functions can be done with OBJ or DAE files which can be used by almost any meshing program.

Here's a summary of the functions:

Cloning Tool - clone from game packages or custom packages

Clone Package Editor - working with custom content packages

    General CAS part properties - properties applied to all recolors
    Recolor Manager - properties for each recolor
    Previewer
    Color Sliders Manager - set limits and increment for color sliders
    HairColor Manager - set list of HairColor CASPs used with certain Wedding Stories items
    Mesh Manager - export and import meshes
    Mesh Fixing Tools - fixes / changes applied to all meshes
    Mesh Region Manager - view / modify regions
    Thumbnail Manager - set up custom thumbnails

Mesh Tools - working with meshes

    Auto Tool: Conversion/Auto Assignments - auto-assign bones, uv1, etc. from a reference mesh
    Conversions: TS4/other - converts TS meshes to and from other formats
    Separate Mesh Layers - creates an MS3D or OBJ mesh with layers separated into groups, mostly useful for alpha transparency hair
    GEOM Tools:
        Examine Mesh - see data in mesh
        View Mesh
        Combine GEOM meshes - combine two TS4 meshes
        Clean Mesh - remove duplicate vertices
    MS3D Tools - tools for Milkshape meshes
        Examine MS3D
    RIG Tools - look at skeleton data


In addition, if you click the Tools menu and Enable Special Tools, you'll see an additional Special Tools tab with various functions I've found useful for searching game packages.

Tutorial: Converting a TS3 dress to TS4
Tutorial: Converting a TS3 hair to TS4, with alpha transparency

This tool is in a perpetual state of beta, so check back for updates, fixes, new features, and so on.

As of V3.4, CAS Tools supports Legacy Edition compatibility. In the cloned package editor tab, general CAS part properties tab, there's now a checkbox for Legacy compatibility. What this does is save the package with the previous version of the CASP format. The only difference is that Legacy compatible packages cannot be set up to be created/knitted in-game, cannot use color sliders, and cannot link to HairColors. You can also convert a package that doesn't show up in Legacy Edition to be compatible by opening and saving it with CAS Tools.

Questions, bug reports, problems, and suggestions for the tool itself should be posted here. Questions and problems concerning a specific project should be posted in the TS4 Create / CAS Parts forum.

If you're having problems, please upload the package, mesh, texture, etc you're working with and explain exactly what you did step by step. 'I tried to import something and it didn't work' doesn't help me to help you.

### Additional Credits:
s4pe/s4pi is used by CAS Tools for package and image handling. s4pi/s4pe and CAS Tools are open source.

s4pe download: https://github.com/s4ptacle/Sims4Tools/releases

Latest working s4pi source: https://github.com/s4ptacle/Sims4Tools/tree/develop

### Updates:

#### 3/18/2023: V3.8.2.0
- Added the infant life stage.
- Added new body type categories.
- Updated tags.
*** This is very much an interim update and some functions probably don't work ***
The way EA set up infants makes it a bit more difficult to add them than it was to add toddlers. They also have added support for DDS textures for backpacks (and presumably other accessories) that seem not to have to use the usual uv0 template. I haven't had time yet to implement that or to test any of the auto tools. You should be able to do the basics of cloning an item and modifying meshes and textures, and if/when you come across errors please report them.

#### 7/31/2022: V3.8.1.0
- Updated tags for new High School categories.
- Added Body Hair and Body Scar search categories in the cloner tab.
- Now searches for downloaded content (DLC).
- Now uses a better folder browser for the game and user paths in the settings.

#### 7/4/2022: V3.8.0.0
- Updated for the June 2022 werewolf patch.
- LRLE compression is overhauled to work with the patched game, fixing textures that appear spotty in CAS and the game.
- Tags updated, scar and bite mark types added.
Note: I suspect werewolf parts, like the werewolf head and nude body, use a different rig. However, I haven't yet found any flag or marker that indicates this in the CASP. This should only be a problem if you export a mesh and need the correct rig for animation or whatever.

#### 3/7/2022: V3.7.1.0
- Items made for both sexes will now be included when filtering for one sex or the other.
- Added a setting for behavior when opening a package with outdated CASPs, which can be set to avoid popup prompts:

    Prompt
    Automatically update, no prompt
    Do not update, no prompt

Note that you can change this setting at any time by clicking File / Change Settings.

#### 2/26/2022: V3.7.0.0
- Updated to support new HairColor type used by certain new items in Wedding Stories to overlay color of built-in hair.
- Fix for bug causing crashing when updating older packages to latest version.

#### 2/23/2022: V3.6.1.0
- Updated to support certain new items introduced in Wedding Stories.

#### 2/17/2022: V3.6.0.0
- Updated for new version of CASP.
- Fix for bug causing color slider changes not to save properly when applied to a single CASP.
- The option to save non-slider compatible CASPs is removed since clothing CASPs now have slider data.
- Tags are updated.
There will be another update when I figure out what the new information in the CASP means.

#### 9/11/2021: V3.5.3.1
- Added fingernails and toenails to exclude parts.
- Added default vertex colors for fingernails and toenails.

#### 9/10/2021: V3.5.3
- Added support for fingernails and toenails.
- Overhauled the type filters in the cloning tab.
- Fixed the annoying 'unsaved mesh changes' message when you change a part type.
- Now changes the swatch color of eyecolors when cloning new custom content. The change is very small and serves only to keep the game from confusing them with EA eyecolors.
- Updated property tags.

#### 6/2/2021: V3.5.2
- Fix for bug causing uv1 autoassignment to crash on clothing/accessory meshes with more than the standard two uv maps. Extra maps will be removed.
- Restored the old method of assigning slotrays from a default body mesh as an option in the Mesh Fixing Tools tab. You can now choose which method to use since the new method of calculating slotray intersections, while more accurate, may not work correctly on some meshes depending on their shape.
- Updated property tags.

#### 1/19/2021: V3.5
Updated with full support for the LRLE texture format. Import PNG or DDS as usual and check the 'Save as LRLE' box to convert and save it as LRLE. Only diffuse/material textures can be saved as LRLE.
Added support for makeup sliders.
Notes:

    PNG or uncompressed DDS with or without mipmaps can be imported and converted to LRLE.
    PNG or compressed DDS with mipmaps should still be used for non-LRLE (RLE2) textures.
    Sliders only work with makeup at this time.
    While you can import textures as LRLE for any type of item, they may be significantly bigger than RLE2 textures and may not render well on clothing.
    Use of LRLE for items other than makeup is experimental.


#### 12/8/2020: V3.4.2
This is an interim update for the new CASP version introduced in the 12/7 patch. There's a chunk of new data in the new version, and I'll try to figure out what it does and update again. Note: Cloning one of the new child facepaints will NOT work.
Updated property tags.

#### 9/2/2020: V3.4.1
Bugfix - cloned CC packages should no longer contain extra copies of bumpmaps and emission maps.

#### 8/26/2020: V3.4
Added ability to edit new knitting/create-in-game settings.
Added Legacy Edition support. Please see the section above on Legacy compatibility for details.
Updated property tags.

#### 7/24/20: V3.3
Added a workaround for makeup/eyecolors/eyebrows affected by the Eco Lifestyle patch. Some items may still not have an accessible texture.
Added support for new version of the CASP resource.
DAE meshes should now save much faster.
Updated property tags.

#### 3/9/20: V3.2.1
Fixed incorrect list of flags to disable CAS Parts for Mermaids and Witches/Spellcasters.

#### 12/17/19: V3.2
Added ability to export and import meshes in Collada DAE format which can be imported to/exported from Blender. DAE meshes can be imported directly into a package just like TS4 geoms. Please be aware DAE takes a LONG time to save. DAE is not yet supported in the separate layers function.
Will now optionally copy thumbnails when cloning a custom package.
Update of property tags to support Witches.

#### 7/24/19: V3.0.0.1
Bugfix for program not starting on systems using some languages.
Added manual override of vertex ID in auto-conversion.

#### 7/17/19: V3.0.0.0
Update to support mermaid tails.
Auto-assignment enhanced to support skirts with built-in reference meshes.
Mesh fixers tab redone to make it easier to fix all meshes in a package.
Corrections to rigs exported with MS3D meshes.
Import/export of TS3 meshes is removed, to be replaced with Collada .dae in a future release.
Update of property tags.
This is an interim release! There are a lot of changes under the hood which means there are probably bugs I haven't caught, and I'm hoping to get Collada support working soon, hopefully allowing users to work with meshes in Blender and more easily import from-scratch meshes.

#### 12/21/18: V2.9.0.0
Easier import/export from/to .PNG
Updated CASP property tags and packs list for Get Famous and patches.
Minor and cosmetic changes.

#### 6/26/18: V2.8.0.0
Added ability to import/export textures from/to .PNG
Fixed bug causing an unrecognized property tag to prevent saving changes to a CASP.
Fixed incorrect values of Exclude Modifiers option in CASP general properties.
Updated list of CASP property tags for Seasons patch.
Minor and cosmetic changes.

#### 11/14/17: V2.7.2.0
Added a fix for transparency (SimGlass) hair which may look either very darkened or have a hard, bright shine. (Note for creators - this is caused by linking a bumpmap that doesn't exist or not linking a bumpmap in the shader at all respectively. I guess the new version rendering is less forgiving.) This fix is also in the Clone Package Editor / Mesh Properties and Fixers tab. It does the same thing as blanking the bumpmap but is done in one click. Should only be used on hairs with these problems. I've heard there may be problems with color in other hairs but without a sample package and a picture of what the hair is supposed to look like I can't test.
Fixed the vertex color correction in the same tab to maybe actually work. Updated vertex color standards.

#### 11/13/17: V2.7.1.0
Fixed bug in Autoconversion Tool that was making mesh faces separate in some morphs
Fixed bug causing current version reference meshes in autoconversion to be incorrectly rejected as not TS4
Added a fix for distortion of dress and skirt meshes in morphs, most visible in the fat morph. (Note for CC creators, the maximum red value for vertex color seems to now be 63. According to my tests values over that are causing distortion.) This fix, along with the arm position fix, is in the Clone Package Editor / Mesh Properties and Fixers tab.

#### 11/10/17: V2.7.0.1
Fixed failure to read textures from Cats & Dogs (and probably other packs).

#### 11/10/17: V2.7.0.0
Updated for the new version of the GEOM (mesh) resource in the 11/8/17 patch.
Will fix arm positioning in CC that now has the arms too close to or inside the body. Open the package in CAS Tools and save as a new, fixed package.
Arm position fix updated.
Additional option in mesh autoconversion to improve results with Milkshape head meshes by retaining the original vertex numbering.
Additional option in mesh autoconversion to force manually entered UV1 coordinates.
Tag list updated.
PLEASE NOTE: This is an interim release to deal with the November patch, but I haven't tested everything. Please report problems. When reporting a problem please be as detailed as possible and if relevant upload the package, mesh, image, etc you're getting an error with. This version is a fix only and should not be used for making cat and dog CAS Parts.
I'm going to see if I can do a small standalone tool to batch convert CC clothing to fix the arms.

#### 1/14/17: V2.4.0.0
Updated for the new version of the CASP resource in the 1/12/17 patch.
Support for toddlers added.
Support for new occult body part types added.
All meshes converted to ms3d should now have the correct skeleton.
Tag list updated.

#### 12/3/16: V2.3.0.0
Updated for the new version of the CASP resource in the 12/1/16 patch. EA hates me.

#### 9/25/16: V2.2.0.0
Fixed bug causing hex value error when auto-converting TS3 meshes with no reference mesh.
Fixed bug causing auto-conversion of .ms3d meshes with no skeleton to error out.
Exported DDS textures will now retain mipmaps.
Ability to view body morphs added to the CAS previewer. 