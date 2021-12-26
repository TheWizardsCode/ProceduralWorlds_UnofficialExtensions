# Procedural Worlds - Unofficial Extensions

This is where we keep some unofficial extensions for Procedural Worlds products. These are open source and as such there is no guarantee they will do what you want but we are always happy to work together to improve them. Use the issue tracker and pull requests system of GitHub and chat with us on Discord at http://bit.ly/WizardsCodeDiscord

IMPORTANT: you will need a copy of the appropriate Procedural Worlds tooling to make use of these extentions. See http://bit.ly/ProceduralWorlds. In some cases you will also need additional assets, such as models, these requirements will be described below as needed.

# Gaia Biomes

  * [Tropical Forest Pack](https://bit.ly/UnityTFP) See in action in our [Speed Build - Tropical Terrain using Gaia, Tropical Forrest Pack and Enviro](https://youtu.be/zciz3ZLNjJk) video. There are deeper dive videos on that channel too.

# Installation for Read Only Use 

This instalaltion process does not allow you to edit the files locally. You will be able to copy them into your project and edit them there. However this approach is really intended for initial testing. See below for a more flexible use scenario.

  1. Install Gaia tooling
  2. Select `Window -> Package Manager`
  3. Click the '+" in the top left
  4. Select 'Add package from Git URL'
  5. Paste in https://github.com/TheWizardsCode/ProceduralWorlds_UnofficialExtensions.git

  The code will be installed into your packages folder in the Project view. You cannot edit these files as they are read only, however, you can copy them into your project if you want to work with them. If you want to make changes that are part of the core project, however, you should use the development process below.

# Installation for Development

This installation process allows you to work on the extensions locally. We recommend this approach as it gives much more flexibility. However, it is a little longer to setup so you might want to start with the above.

Using this approach you will have one master project which acts as your development project for these tools and one or more game dev projects which use these tools (see next section). It is possible to do this with a single project but we recomend the two project approach since it keeps things neatly separated.

  1. Fork this project on GitHub
  2. Create a Unity project for doing your dev work in this project - we call these projects `PW-UnofficialExtensions-Dev` in order to distinguish them from our game work
  3. Install the Procedural Worlds tools into your project
  4. Clone your forked repository into your Unity projects Asset folder `git clone [YOUR_FORK_URL]`
  
In this setup the tools code is inside your Assets folder and thus the workflow is the same as it always is for Unity projects. All your normal development tools are available. You can create test scenes and other useful environments. This is where you will do your testing of any major changes and ensure any pull requests you issue are correctly setup. To make use of your local development code in another project follow the steps in the previous section, but rather than adding the package from a Git URL point to the copy on your local filesystem. You will then be able to edit the package code from within any of the projects that add the package in this way.

# Installing Development Code into Working Projects

The above instalation creates a dev project for these tools. You can use that approach to manage your game development projects too. However, we recommend using this approach described below for game development projects as it allows you to avoid having multiple Git repositories in the same project, which is always clumsy. The process is just like for the Read Only Use instructions above, however in this case you will have read and write access to the content. Any changes you make will be reflected back in the above development project and any other dev projects that use the approach described here.

  1. Create your Unity project as usual and install Gaia tooling
  2. Select `Window -> Package Manager`
  3. Click the '+" in the top left
  4. Select 'Add package from disk...'
  5. Locate the directory on disk that you checked out in step 4 in the previous section
  6. Select the `package.json` file

That's it you are up and running. These tools will be accessible through the packages section of your project, but unlike the first approach above you have write access.