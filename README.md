# schemaspy
Schemaspy for Postgresql


I've been using SchemaSpy for around last 2-3 years with Postgresql to show techinical clients that how our database and its schema is. Below information is I found at few different sites, basically http://schemaspy.org/ they have provided service for all database but still I want to add what specifically for postgresql but we can use core SchemaSpy for all databases. 

Below are the links of the same which are useful : 

https://github.com/schemaspy/schemaspy

https://schemaspy.readthedocs.io/en/latest/started.html#configuration

https://schemaspy.readthedocs.io/en/latest/installation.html

http://schemaspy.sourceforge.net/  to have extra oarameter to apply.

Currently SchemaSpy has released 6.0.0 version and this is awesome. 

So what basically you will need to : 

## Step 1 : ##

`apt-get install graphviz`

If you get error

    Failed to query Graphviz version information
    with: dot -V
    java.io.IOException: Cannot run program "dot": error=2, No such file or directory
    ref :https://sourceforge.net/p/schemaspy/discussion/462849/thread/38a9bfad/

then `apt install graphviz`

##  Step 2 :  ##

Install java, I used ubuntu so I've used below link to install JAVA.

https://thishosting.rocks/install-java-ubuntu/

I've used only `apt-get install default-jdk`

##  Step 3 :  ## 

Download latest version of Schema Spy at http://schemaspy.org/

##  Step 4 :  ## 
  
  Set password to your database.
  Now find appropriate JRE i.e. `postgresql-9.4.1212.jre6` and download. here https://jdbc.postgresql.org/download.html
    
##  Final Step : ##

Use command to generate schema related information : 

`java -jar schemaspy-6.0.0.jar -t pgsql -db imast -host localhost -u username -p password -o ./schemaspy -dp postgresql-9.4.1212.jre6 -s public -noads`

Now you'll beatiful output from it.

To have example or ready things I've connected my VERY OLD and STOPPED projects database and useful jar, jre files for you guys. 

I hope you people will like this. 
