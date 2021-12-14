# DataStax Docker bare-bones setup

## Background
Based on DataStax docker compose for the NoSQL workshop - original repo [found here](https://github.com/datastaxdevs/workshop-introduction-to-nosql).

When I tried using the original docker setup on Win 11 / Docker Desktop / WSL, the studio container started, then failed -- apparently because of a problem in the volume mount located in datastax-studio-config.  For this config, I wiped that location clean and restarted / rebuilt the repo.  This setup should start and run, but will not contain the pre-loaded notebook found in the original.  You'll be able to create and use *a* graph DB with this setup, but you won't have all the pre-loaded data found in the workshop setup.

However, Cedrick Lunven provided an export of the notebook used in the workshop, and if you import that into this image, you'll be up to speed in no time.

## Getting Started
Clone this repo and start the cluster:

`
docker compose up
`

Docker should show a "datastaxgraphdemo" app with two containers running.  The dse container is the DataStax Enterprise back-end, and the other container is the studio front-end - it should be running / listening on port 9091.  Browse to this port on localhost, and you'll (hopefully) see DataStax Studio with a bunch of notebooks.

Next: check / configure a connection to the dse server - this is the same as [the original instructions](https://github.com/datastaxdevs/workshop-introduction-to-nosql/blob/main/README.md) if you want to follow along there.  Pretty simple - just make sure there's a connection pointing at host 'dse', and select it.

Finally, import the tar file Workshop_Introduction_to_NoSQL_Graph_Databases_2021-12-14_17_35_15.studio-nb.tar using the "Import Notebook..." menu in DataStax Studio.  You should now be all caught up to step 5f in the origainl instructions.

