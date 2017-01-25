# Forge Quickstart Archetype
Used to rapidly create a maven based project. This archetype has no opinion on which type of service it will be used. 

## Installing

At the moment, we suggest installing to your local maven repository. This is to help reduce the clutter from accessing a remote one and its overwhelming number of archetype options. 


Download

	git clone https://github.com/saas-forge/forge-quickstart-archetype.git
	
Install

	mvn clean install archetype:update-local-catalog
	
## Creating a new Forge Quickstart project
When you are ready to create a new project using this archetype, from the command line:

	mvn archetype:generate -D archetypeCatalog=local
	
### Wizard Prompts

#### Choosing the archetype
Find the corresponding entry number in your local repository for this archetype. Use that value as the requested `Choose a number or ...` value prompted by maven and hit enter.

#### Define the group id 
For `Define value for property 'groupId': `, enter your projects group id, for example `com.example`. 

#### Define the artifact id
For `Define value for property 'artifactId': `, enter your project name, for example: `my-application`. This will not only define your projects name, it will also create the projects root directory based on this choice.

#### Define the version
For `Define value for property 'version':  1.0-SNAPSHOT:`, you may use the default value `1.0-SNAPSHOT` or choose to enter your own. 

#### Define the package
For `Define value for property 'package':  com.example:`, you may choose a different packaging convention or use the supplied default determined by your `groupId` choice in the above `Define the group id` step.

#### Review your project build 
Finally, the wizard will ask if the supplied information is correct, if yes, simply hit enter. 

### Change directory to your project
Once completed, your project from the archetype will be created in the present working directory. Simply

	cd my-application
	
Once in the projects root, you can confirm it is working by running the following command

	mvn clean install
	
This install will run all tests and confirm the initial correctness of the application. 