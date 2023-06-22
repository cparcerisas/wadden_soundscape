# Categorize Wadden Sea soundscapes 

This code reproduces the code in: https://github.com/lifewatch/categorizing_soundscapes
Slightly adapted for the Wadden Sea data. 

The same LICENSE applies. 

Read the comments to change the variables depending on the needs. 

You should run the jupyter notebooks in order. 

* 0_create_dataset will create a dataset. You don't need to move your wav files, just pass the correct path. 
However, you SHOULD have a data_summary in data/raw_data (or somewhere else and change the path). It should 
create one .nc file per row that you listed in your metadata, and store it in data/raw_data/deployments
* 1_add_env_data will add the environmental data to the nc files created in 0. It will create the same amount of files 
which 0 created, but store them in data/processed and with an additional _env.nc at the end of the name
* 2_prepare data will join all the deployments in one single dataset so they can be analyzed. It will create several 
.pkl files under data/processed 
* 3_clustering_paper will produce plots and csv files with the output, they will be stored in the output folder 
automatically. You don't need to create an output folder, it will be automatically done and filled. 