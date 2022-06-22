# test2

1. Accessing the data Chris has can be done through [decrypt_raw_data.py] (https://github.com/lenasong/Phone-Dashboard-Scripts/blob/main/decrypt_raw_data.py), 
which will upload to a Dropbox folder, or [decrypt_raw_data_local.py] (https://github.com/lenasong/Phone-Dashboard-Scripts/blob/raw_data_tools/raw_data_tools/decrypt_raw_data_local.py), 
a very slightly amended version of Chris' code, which will download the desired data to your machine.
Care should be taken to ensure that the API did not run across any issues; occasionally, it will fail, but the program will keep running, so you should manually check that all the files did indeed download. 
A quick way of doing this to, within any of the folders created by [decrypt_raw_data_local.py] (https://github.com/lenasong/Phone-Dashboard-Scripts/blob/raw_data_tools/raw_data_tools/decrypt_raw_data_local.py), 
ensure that the file names have every increment of 100000 from 0 to the final number in the file names. Alternatively and more quickly, check that the number of files in the folder corresponds to the number in the file name.
2. Then run [read_decrypted_data.py] (https://github.com/lenasong/Phone-Dashboard-Scripts/blob/raw_data_tools/raw_data_tools/read_decrypted_data.py), which will read the decrypted data and refactor the data to have a single ping as a row, rather than the previous nested JSON array. This refactoring makes the data more intuitive and easier to look through. Study can then be done on the raw data. 
3. If you want to compare to data in the existing Phone Addiction Dropbox, it will be necessary to download/utilize the data in the Phone Addiction Dropbox. 
For the purposes of any code here, I take any subset of the data there, move it to a separate folder, which I then reorganize into "/root/dropboxdata/date/...," which contains a zipped folder downloaded from Dropbox and named the server name (such as "nyu-1") that contains the corresponding (to the date and server name) files from Dropbox. 
[dropbox_processor.py] (https://github.com/lenasong/Phone-Dashboard-Scripts/blob/raw_data_tools/raw_data_tools/utilities/dropbox_processor.py) will unzip the necessary files.
4. Included are a set of utilities that may help in case you may want to investigate the raw data or other issues come up.
Running [data_puller_plotter.ipynb] (https://github.com/lenasong/Phone-Dashboard-Scripts/blob/raw_data_tools/raw_data_tools/utilities/data_puller_plotter.ipynb) lets you extract data on certain days, as well as other desiderata such as if it falls under FITSBY, and screen active or not. It also makes convenient plots that demonstrate counts and so on.
You may occasionally want to look at data for one or a small number of IDS. Running [ID_extractor_plotter.ipynb] (https://github.com/lenasong/Phone-Dashboard-Scripts/blob/raw_data_tools/raw_data_tools/utilities/ID_extractor_plotter.ipynb) will extract more manageable datasets for the appropriate IDS provided.
