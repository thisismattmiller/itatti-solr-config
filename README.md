# itatti-solr-config
Solr 5.5 config files for Itatti Berenson portal

This is the config files that Solr 5 can use.

Install solr

Make sure you have java 8 installed

Download zip: http://archive.apache.org/dist/lucene/solr/5.5.2/
`wget http://archive.apache.org/dist/lucene/solr/5.5.2/`

Extract
`unzip solr-5.5.2.zip`

Clone this repo, it contains the configurations we want to use with our portal
`git clone https://github.com/thisismattmiller/itatti-solr-config`

Start solr
`bin/solr start`

Create the core with our config, use the path to where you git cloned above
`bin/solr create_core -c blacklight-core -d /path/to/your/git/directory/itatti-solr-config/conf`


To Update
If changes are made to the solr config and you need to update the server you can:
Delete the core, restart and create it again with the updated config info
```
bin/solr delete -c blacklight-core
bin/solr restart
bin/solr create_core -c blacklight-core -d /path/to/your/git/directory/itatti-solr-config/conf
```
