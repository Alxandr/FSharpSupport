YoloDev.FSharp.AspNet
=============

<h1>Project is deprecated, see <a href="https://github.com/YoloDev/YoloDev.Dnx.FSharp">YoloDev.Dnx.FSharp</a>.</h1>

FSharp Support for K

Usage
===
#### Step 1.
Add the yolodev myget feed to your `NuGet.Config` file. This file should be in your Solution folder. If it does not exist yet, you must create one. Proper casing of the filename is important! 

Sample:

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <add key="YoloDev" value="https://www.myget.org/F/yolodev/api/v2" />
    <add key="AspNetVNext" value="https://www.myget.org/F/aspnetvnext/api/v2" />
    <add key="NuGet.org" value="https://nuget.org/api/v2/" />
  </packageSources>
</configuration>
```

#### Step 2.
Create a new `ASP.NET vNext Empty Web Application` or `ASP.NET vNext Desktop Application` project in Visual Studio 2014. The new project system uses a `project.json` file to list all the dependencies. This file resides in the root folder of the project. Add the YoloDev.FSharp.AspNet library as a dependency. Because we're going to use an other language than C# we have to add a "language" key to the project.json file. You also need to add sources, since the default one just goes looking for *.cs. This is also quite important in F#, since file order matters. So be sure you list the sources in the right order. 

Sample:

```js
{
    "dependencies": {
        "YoloDev.FSharp.AspNet": "0.1-*"
    },
    "code": [ "file1.fs", "file2.fs" ],
    "language": {
        "name": "F#",
        "assembly": "YoloDev.FSharp.AspNet",
        "projectReferenceProviderType": "YoloDev.FSharp.AspNet.FSharpProjectReferenceProvider"
    },
    "frameworks": {
        "aspnet50": { }
    }
}
```

#### Step 3.
Change the following value in the properties dialog for the project:
![properties](http://i.imgur.com/F0Xgxhy.png)

#### Step 4.
Code in F#!

#### Step 5.
???

#### Step 6.
Profit!
