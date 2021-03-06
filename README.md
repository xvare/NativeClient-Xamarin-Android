#Windows Azure Active Directory Binding Example for Android for Xamarin


This sample shows how to build a Xamarin binding to our native ADAL for Android library. This is a sample and is not to be used in production. We plan on adding a true cross platform mapping layer in the future. For those interested in binding to our Android library in .Net using Xamarin, this code is a good guide.

We provide the ADAL for Android jar along with resources in this repo. It is named ***AdalwithResources.zip*** and is located under /jars. You will need to use this .zip file instead of the standalone .jar file for the Xamarin bnding to work.

##### NOTE 

In the future we will update this sample to include other ADAL libraries as create a more robust mapping layer. At the moment, we are using the binding file directly to allow Xamarin developers on Android to use our library. 


## Quick Start

###Step 0: Learn about binding java libraries with Xamarin

* You'll get up to speed faster if you do some reading of the Xamarin documentation for Android Binding to native libraries located here: [Binding Android Libraries](http://docs.xamarin.com/guides/android/advanced_topics/java_integration_overview/binding_a_java_library_(.jar)/)

* Finally, you may want to read through how Xamarin works with Java here: [Xamarin for Java Developers](http://docs.xamarin.com/guides/android/advanced_topics/java_integration_overview/)


## Using Xamarin Studio


### Step 1: Download Xamarin Studio

You can get [Xamarin Studio](http://xamarin.com/studio?_bt=44014804148&_bk=xamarin%20studio&_bm=e&gclid=COqr3sHrs70CFUWVfgodkmEAwg) from the Xamarin website.

### Step 2: Create a "Android Java Binding Library" Project in Xamarin Studio

Select File -> New -> Solution and select "Android Java Binding Library"

### Step 3: Clone this code in to your Project directory

Go to the directory where you created your new project and clone the files in this repostiory. You will then need to add these files in to Xamarin Studio by clicking on your project tree and selecting "Add Files.." in the pulldown. 

###### NOTE

The names of the files in this repository should match closely the default files that are included in the Java Binding project for Xamarin. This will aid you in replacing the files or code with the correct files from our repository.

### Step 3: Add the latest version of ADAL for Java library to the Project

You will need to bind to **AdalWithResources.zip** in your Xamarin Studio Java Binding project as discissed in [Binding Java Libraries](http://docs.xamarin.com/guides/android/advanced_topics/java_integration_overview/binding_a_java_library_(.jar)/). The easiest way to do this is to use the included AdalWithResources.zip file in this repo. If you need to update the AdalWithResources.zip to use the latest ADAL for Android see the instructions below.


### Step 4: Run and use!

Run the project and then pull the .dll files out of the /bin directory Xamarin Studio will create.


## To update the AdalWithResources.zip file from the command line 
(if you wish to update a later version of the classes.jar library)

`cd azure-activedirectory-library-for-android/`

`android update project -p .`

`ant debug`

`zip -r AdalWithResources.zip bin/classes.jar bin/AndroidManifest.xml res`

You will need to bind to **classes.jar** from the ADAL for Android library. The easiest way to do this is to grab the latest ADAL for Java and compile the source.

You can get the latest ADAL for Java library here:

[https://github.com/MSOpenTech/azure-activedirectory-library-for-android](https://github.com/MSOpenTech/azure-activedirectory-library-for-android)


Add the dependency jar files to binding project as well if it has changed and keep them as an embebded referenced jar.


