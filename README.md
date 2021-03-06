
### Project Organization:

The way I am adopting my project organization is inspired by minimal data analysis template @ (https://github.com/shuzhao-li/cookiecutter-data-science-min). For my quick reference @ [Wiki](https://github.com/amnahsiddiqa/ProjectsOrganization/wiki/CookieCutter). 

Note: Syncing Synapse and local machine project directories. In future projects --> local machine replaced by Sumner.


![](Figures/ProjectOrganization.png?raw=true)

The whole idea is very simple and I would follow it like this for collaboration:

* All data in data folders in separate directories. 
  * One directory dedicated to immutable data (raw data) and rest as needed. 
  * For every project's metadata or any other supporting data (could be anything), It would depend if its needed to be in same heirachichal level as data or inside child data directories.   

* All code in notebooks (Jupyter/Rmd) in separate directories.
   * I like to keep one workflow notebook and put supplementary functions in source files ( be them .R, .py ). I am an R person so I use Rmd but ofcourse that could be a bash/python/jupytrt notebook/whatever you like workflow  script/md.
   
   * Blue box on LHS: One child level notebook dedicated to one task/question in main project. And the workflow notebook should be able to get up and running by setting paths     only.The input data should be sourced from data directory. However depending on a project I might end up with some supplementary data required for that task only-  so I would keep it inside the notebook directory and source it from there.
   
   * Red Box on RHS: Results/Output from a child notebook directory would end up in the same notebook directory for me.
   
   * Just to keep another copy intact, I would update after every finished task the synapse project folder. Besides many others, two key advantages I save a backup and second sometimes analysis is much complex and can take several hours of CPU time to run and it would be easier for collaborators/contributors to explore more on the same data that i produced for time being and verify analysis in their own time.
   
   
   
* At the end of every Task, I need to do only two things:
   * push to git repo of project
   * update synapse (I use same three liner at the end of evey notebook in  whole project for updates with a single synapse parent project id. This keep my synspase project synced with the project directory on my local machine) 
   * provenance on synapse is another story:Detials to add later.

* One last note: The html files rendered in Rmd .. Dropbox Sync note to add later.
   
 #### To Replicate Analysis:
 In order to replicate analysis in a project, the idea is that following steps should work and be able to walkthrough anybody else through whole project:
 
 * Download git repo of project
 * Follow instructions at main ReadMe.md
 * Rest every notebook's comments should provide enough additional information about each step of analysis
 * to follow discussions and comments, as a good practice try maintaining wiki page of synapse child folder for that notebook. 
   
   
  
  
  
  **After making peace with this , my Life is no less than heaven!!**



# SynapseThingies


### Synapse R client info @
* https://r-docs.synapse.org/articles/synapser.html


### Synapse Login setup @
https://r-docs.synapse.org/articles/manageSynapseCredentials.html


### SynExtra for dealing with complex file structures @
* https://r-docs.synapse.org/articles/synapser.html
* To access synExtra at git: https://github.com/ArtemSokolov/synExtra


### Synapse Config file handy example @ 
* Examples of setting up synapse config files parameters @ https://github.com/Sage-Bionetworks/synapsePythonClient/blob/master/synapseclient/.synapseConfig



Author: amnah.siddiqa@jax.org
