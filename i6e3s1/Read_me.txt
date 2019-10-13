1. Installing the framework manually

a. Navigate to the framework's releases page at https://github.com/accord-net/framework/releases
b. Click to download the "libsonly" .rar release to your computer
c. Click to open the file. You will see the binaries are contained inside the "Release" folder
d. Navigate to the Release\net35 folder.
e. Extract the libraries that you think you might need in your application. More likely you will need:
	-Accord.dll
	-Accord.Math.dll
	-Accord.Math.Core.dll
f. Open Unity
g. Create a new or open an existing project
h. Make sure that your Unity project project is set to use .NET 2.0 instead of .NET 2.0 Subset in the project's settings. For this, navigate to Edit -> Project Settings -> Player and change the property Api Compatibility Level to .NET 2.0 if necessary.
i. Now, create a folder inside your project to hold the Accord.NET libraries. 
j. Copy them manually to your project.
k. Now, open your C# project in Visual Studio, and you will see that the project will have been automatically added to your project references.

2. Installing the framework through NuGet

a. To download the framework through NuGet, you can follow the steps below.
b. Open Unity.
c. Create or open an existing Unity project.
d. Make sure that your Unity project project is set to use .NET 2.0 instead of .NET 2.0 Subset in the project's settings. For this, navigate to Edit -> Project Settings -> Player and change the property Api Compatibility Level to .NET 2.0 if necessary.
e. Click Assets -> Open C# Project.
f. Create a new file named "nuget.config" in your project's solution with the following contents:

<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <config>
    <add key="repositoryPath" value="Assets\Packages" />
  </config>
</configuration>

g. Close Visual Studio. This is really necessary because the nuget.config file that we have just created will not be parsed/re-interpreted unless we close Visual Studio and re-open it again.
h. Click Assets -> Open C# Project again to re-open Visual Studio.
i. Search for the Accord.NET packages you would like to add (i.e. "Accord.MachineLearning").
j. Click on your application name on the right to mark its checkbox.
k. Click "Install" and accept the license terms.
l. The framework libraries should have been installed under the Assets folder and can now be used from within Unity.



