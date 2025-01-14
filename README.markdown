Project UppercuT - Builds in Seconds, Not Days
=======
  
![UppercuT](https://github.com/chucknorris/uppercut/raw/master/docs/logo/UppercuT_Logo_Small.jpg "UppercuT - insanely easy. Insanely.")  
  
# LICENSE
Apache 2.0 - see docs/legal (just LEGAL in the zip folder)  
  
# IMPORTANT
NOTE: If you are looking at the source - please run build.bat before opening the solution. It creates the SolutionVersion.cs file that is necessary for a successful build.  
  
# INFO
## Overview
UppercuT is a conventional automated .NET build framework (templated NAnt). UppercuT is the insanely easy to use build framework.  
  
It seeks to solve both maintenance concerns and ease of build to help you concentrate on what you really want to do: write code. Upgrading the build should take seconds, not hours. And that is where UppercuT will beat any other automated build system hands down.  
  
UppercuT uses conventions and has a simple configuration file for you to edit. Getting from zero to build takes literally less than five minutes. If you are still writing your own build scripts, you are working too hard.  
  
UppercuT is extremely powerful because it is customizable and extendable. Every step of the build process is customizable with a pre, post and replace hook.  
  
UppercuT is not a build server, but it integrates nicely with CruiseControl.NET, TeamCity, Hudson, etc.  
  
## Join the mailing list
 Ask questions - get answers - [http://groups.google.com/group/chucknorrisframework](http://groups.google.com/group/chucknorrisframework)  
  
## Getting started with UppercuT
### Downloads
 You can download UppercuT from [http://code.google.com/p/uppercut/downloads/list](http://code.google.com/p/uppercut/downloads/list)
  
 You can also obtain a copy from the build server at [http://teamcity.codebetter.com](http://teamcity.codebetter.com).
  
### Gems  
If you have Ruby 1.8.6+ (and Gems 1.3.7+) installed, you can get the current release of UppercuT to your machine the fastest!  
  
1. Type 'gem install uppercutbuild'  
2. At the top level directory (trunk or branch name) type 'uppercutbuild init' for bringing in uppercut for the first time or 'uppercutbuild upgrade' if you already uppercut and are just wanting to upgrade the build folder.   
  
### Source
This is the best way to get to the bleeding edge of the code.  
  
1. Clone the source down to your machine.  
  `git clone git://github.com/chucknorris/uppercut.git`  
2. Type `cd uppercut`  
3. Type `git config core.autocrlf false` to set line endings to auto convert for this repository  
4. Type `git status`. You should not see any files to change.  
5. Run `build.bat`. NOTE: You must have git on the path (open a regular command line and type git).  
  
# REQUIREMENTS
* .NET Framework 3.5  
* Source control on the command line and in PATH environment variable - svn for Subversion / tf for TFS / git for Git  

# DONATE
Donations Accepted - If you enjoy using this product or it has saved you time and money in some way, please consider making a donation.  
It helps keep to the product updated, pays for site hosting, etc. https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=4410250

# RELEASE NOTES
=1.x.x.x=  
* Adding in support for StorEvil.  
  
==1.4.1.0==  
* FIX: Issue 40 - customizations fail when the folder path has build in it more than once - see http://code.google.com/p/uppercut/issues/detail?id=40 for details. (418)  
* FIX: Issue 39 - The detailed build.log is not being written to sometimes - see http://code.google.com/p/uppercut/issues/detail?id=39 for details. (415)  
  
==1.4.0.0==  
* FIX: Issue 33 - Cannot build .NET 1.0 and 1.1 Solutions - see http://code.google.com/p/uppercut/issues/detail?id=33 for details. (412)  
* Issue 37 - Enhancement: Add support for Microsoft's built-in code metrics. New settings have been added to the uppercut.config: <property name="app.metric" value="C:${path.separator}Program Files (x86)${path.separator}Microsoft Visual Studio 10.0${path.separator}Team Tools${path.separator}Static Analysis Tools${path.separator}FxCop${path.separator}Metrics.exe" overwrite="false" /> - see http://code.google.com/p/uppercut/issues/detail?id=37 for details. (410)  
* Issue 34 - Enhancement: MSBuild output is logged for CC.NET to merge in - see http://code.google.com/p/uppercut/issues/detail?id=34 for details. (410)  
* Issue 36 - Enhancement: Open creates SolutionVersion if missing - see http://code.google.com/p/uppercut/issues/detail?id=36 for details. (407)  
* FIX: Issue 35 - Open fails on Windows platform when VSLauncher.exe is missing - see http://code.google.com/p/uppercut/issues/detail?id=35 for details. (407)  
* Issue 28 - Enhancement: Allow setting of Ruby and PowerShell path via variable - see http://code.google.com/p/uppercut/issues/detail?id=28 for details. (405)  
* Issue 38 - Enhancement - Pass properties to ruby/powershell extensions. New settings have been added to the uppercut.config: <property name="app.ruby" value="C:\Ruby\bin\ruby.exe" overwrite="false" /> <property name="app.powershell" value="%WINDIR%\System32\WindowsPowerShell\v1.0\powershell.exe" overwrite="false" /> and this setting has been removed: <property name="allow.powershell.unrestricted" value="false" overwrite="false" /> - see http://code.google.com/p/uppercut/issues/detail?id=38 for details. (404)  
* Console Logging is very reduced with all detail to build.log. (400)  
* Issue 32: Upgrade to NAnt 0.91 Alpha 2 - see http://code.google.com/p/uppercut/issues/detail?id=32 for details. (400)  
* FIX: Settings file values should be able to have more than one other settings value token - see https://github.com/chucknorris/uppercut/issues/3 for details. (400)  
* FIX : Nunit now generates a report when the tests fail. (399)  
* FIX: Issue 31 - Log file copied to code_drop directory before build is complete - see http://code.google.com/p/uppercut/issues/detail?id=31 for details. (396)  
* Issue 29 - Handle Readonly Files during build - allows you to build against source controls that mark files readonly (looking at you TFS) - see http://code.google.com/p/uppercut/issues/detail?id=29 for details. (396)  
* FIX: Obfuscation should find files that are versioning with SemVer. (395)  
* Allowing arguments to be passed into the build.bat file as pass through to nant. (389)  
* NuGet support enhancements to allow subdirectories for building multiple nuget packages in a single solution. (388)  
* Adding in _PublishedApplications known folder. - see http://code.google.com/p/uppercut/issues/detail?id=27 for details. (386)  
  
==1.3.0.0==  
* Fix for spaces in the path when trying to resolve the revision for SVN - see http://code.google.com/p/uppercut/issues/detail?id=25 for details. (385)  
* xUnit Support for automated testing. Will handle multiple test assemblies for you. (384)  
  
=1.2.0.0=  
* NuGet Support. New settings have been added to the uppercut.config: <property name="app.nuget" value="..${path.separator}${folder.references}${path.separator}NuGet${path.separator}NuGet.exe" overwrite="false" /> and a tool that goes under the lib folder: NuGet  - see http://code.google.com/p/uppercut/issues/detail?id=20 for details. (378)  
  
=1.1.1.0=  
* Including Eazfuscator in the output (375)  
* Adding a build.log to the output of the build  - see http://code.google.com/p/uppercut/issues/detail?id=22 for details. (373)  
  
=1.1.0.0=  
* Added support for obfuscation. New settings have been added to the uppercut.config: <property name="obfuscation" value="false" overwrite="false" /> <property name="app.eazfuscator" value="..${path.separator}${folder.references}${path.separator}Eazfuscator.NET${path.separator}Eazfuscator.NET.exe" overwrite="false" /> and a tool that goes under the lib folder: Eazfuscator.NET  - see http://code.google.com/p/uppercut/issues/detail?id=21 for details. (372)  
  
=1.0.6.0=  
* Updating xbuild for use with 32bit windows machines. (369)  
* Gallio NAnt tasks were not being loaded - see http://code.google.com/p/uppercut/issues/detail?id=17 for details. (368)  
  
=1.0.5.0=  
* Now builds mono correctly on windows. (366)  
  
=1.0.4.0=  
* Gems builds default to not using the build date as part of the version. A new setting has been added to the uppercut.config: <property name="use.gem.build_date" value="false" overwrite="false" /> (364)  
* Gems builds now include a version suffix so you can be in prerelease mode or dev mode when using semantic versioning. A new setting has been added to the uppercut.config: <property name="version.gem.suffix" value="" overwrite="false" /> (364)  
* ILMerge step now merges the xml documents together. (363)  
  
=1.0.3.0=  
* Fixed a bug with path to solution no longer being respected at v1 after Linux patch. (361)  
* Upgraded Mono Migration Analyzer to v2.6 (360)  
  
=1.0.2.0=  
* Default versioning follows the old scheme. Semantic versioning is accomplished by adding this to your config file: <property name="version.use_semanticversioning" value="true" overwrite="false" /> (r357)  
* Gem building failure will not fail the build. (r357)  
* UppercuT reported version fix. (r357)  
  
=1.0.1.0=  
* UppercuT has an option to use the old versioning as well. You need to add this to your config file: <property name="version.use_semanticversioning" value="false" overwrite="false" /> (r354)  
* Linux fixes for opening items (from Svein Ackenhausen) (r355)  
  
=1.0.0.0=  
* UppercuT now uses semantic versioning See http://SemVer.org for details. You need to add this to your config file: <property name="version.patch" value="0" overwrite="false" /> (r351)  
* UppercuT now builds on Linux (patch from Svein Ackenhausen). (r350)  
* Non multi targeting now works like it did before any of this multitargeting started. (r348)  
  
=0.9.0.346=  
* Fixed general compile issues related to multi-targeting changes from last release (r346)  
* Gems by default are now versioned with datestamp on the end (YYYYMMDD) (r342)  
* Changed the default test framework to NUnit. (r340)  
* Changed 'uppercutbuild install to 'uppercutbuild init' (r339)  
  
=0.9.0.337=  
* ILMerge is now a step of the build process. Please check the configuration for the new setting. (r337)  
* UppercuT now has the command 'uppercutbuild upgrade'. (r336)  
* Zip will not include the gems folder. (r334)  
* UppercuT (through gems) can copy UppercuT to a solution directory by issuing 'uppercutbuild install' at the top level directory (trunk or branch name). (r333)  
  
=0.9.0.328=  
* Now supports building gems - see http://code.google.com/p/uppercut/issues/detail?id=16 for details.  (r328)  
* The version hash for SVN and TFS should just use version.revision. (r321)  
* General fix - when a step of the build process fails the build, any extensions or custom tasks related to it should also fail the build. (r319)  
  
=0.9.0.318=  
* Nitriq support. Please check for a new setting in the config. (r317)  
* OutputPath is configurable not to be overridden by UppercuT - see http://code.google.com/p/uppercut/issues/detail?id=15 for details.   Please check for a new setting in the config. (r316)  
* Multi-targeting for building your product on several frameworks at once  - see http://code.google.com/p/uppercut/issues/detail?id=14 for details. (r316)  
* Zip uses the version hash (which is only different if you are git or mercurial). (r313)  
  
=0.9.0.306=  
* Added a framework switch for NUnit - handling .NET 4.0 Support (r305)  
* Zip.build handles HG versioning (r304)  
* Nitriq support. Please check for a new setting in the config. (r302)  
* NUnit default is now 2.5.5. (r300)  
* CLS Compliance is now an opt in setting. Please check for a new setting in the config. (r299)  
  
=0.9.0.297=  
* .NET 4.0 Support (r296)  
* Fixed a bug with property setting in tfs.step (r293)  
* Uppercut now houses it's assemblies in the build folder. Please ensure you compare your NAnt folder and remove the assemblies that are no longer there if upgrading (r292)  
  
=0.9.0.286=  
* NUnit tester now runs console version. This fixes a TestFixtureSetup issue - see http://code.google.com/p/uppercut/issues/detail?id=10 for details (r285)  
  
=0.9.0.282=  
* Mercurial (HG) support for versioning (r282)  
  
=0.9.0.273=  
* Enhanced Git Versioning to better work with Hudson (r272)  
  
=0.9.0.266=  
* Adding the ability to use PowerShell to write custom tasks. To run powershell - you need to set unrestricted if you are not going to sign the scripts. Because this possibly exposes a possible security hole, it is turned off by default. There is a property (allow.powershell.unrestricted) you can set to true in the Uppercut.config file. Look in the external tools section for the setting. (r266)  
* Adding the ability to use Ruby to write custom tasks. (r265)  
* Enhanced support of Git versioning on TeamCity. (r263)  
* Fixed a small bug in NAnt related to running .NET 4.0. (r262)  
* DocBuilder will do both .template and .xml now. (r247)  
  
=0.9.0.246=  
* Fixed - Git versioning had an issue with creating the initial tag for versioning - see http://code.google.com/p/uppercut/issues/detail?id=9 for details (r243)  
* Zip nows versions the zip file name by default. Check your zip.post.build. You may need to remove or change zip.post.build. (r240)  
* Support for .NET 4.0 beta2 has been added. (r238)  
  
=0.9.0.235=  
* UppercuT supports Git for versioning - The numbering system is branch specific.  
* Added ILMERGE tasks to the samples  
* Code is now built to a folder under build_output. This is the same folder it goes to under code_drop, so in the case of uppercut, build_output\UppercuT\ instead of just build_output.  
  * BREAKING CHANGE: For your custom tasks, you may need to make changes.  

# CREDITS
see docs/legal/CREDITS (just LEGAL/Credits in the zip folder)  