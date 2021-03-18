**+PROJECT MANIFEST FILES:+**

  Project may contain a manifest file, which is used for project-level settings like as those:
  + For specifying other projects to import into the current project
  + Defining LookML constants
  + Specifying model localization settings
  + Adding extensions and custom visualizations to your project.
  
  We can use a project manifest file either for localization or to project import , but cannot use it for both functions.
  
  Each project can have only one manifest file. The file must be named **" manifest.lkml "** and be placed at the root level of your Git repo. When using folders in the IDE, be sure that the manifest.lkml file is kept at the root level of our project’s directory structure.
  
Use the project manifest file to specify default localization settings. For example:

**localization_settings: {**

  **default_locale: en**
  **localization_level: permissive**
**}**

To import LookML files from a different project, use the project manifest file to specify a name for your current project and the location of any external projects, which could be stored locally or remotely. Below is the instance:
  <img src="/Images/LookML_Project-Manifest1.png">

After defining the external projects in the project manifest file, we can use the **include** parameter in our model file to add files from those external project to your current project. For example:

  **+include: "//my_other_project/imported_view.view"**

  **+include: "//ga_360_block/*.view"**
  
  
