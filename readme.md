DataStax Docker bare-bones setup

Based on DataStax docker compose for a workshop - original repo [found here](https://github.com/datastaxdevs/workshop-introduction-to-nosql).

When I tried using the original docker setup on Win 11 / Docker Desktop / WSL, the studio container started, then failed -- apparently because of a problem in the volume mount located in datastax-studio-config.  For this config, I wiped that location clean and restarted / rebuilt the repo.  This setup should start and run, but will not contain the pre-loaded notebook found in the original.  You'll be able to create and use *a* graph DB with this setup, but you won't have all the pre-loaded data found in the workshop setup.