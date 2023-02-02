# pandas-io-exercies

## Benchmarking Pandas

**FYI: Because we're writing to databases and using c-performant packages such as pytables (for hdf5 file format), we must perform this exercise in Codespaces, which unlike replit, lets us create/write to a SQL database, and install the `pytables` library for the HDF5 file format. `pytables` suggests Anaconda for installation, so that's what we're using (specified in the devcontianer configuration)**

0. Open this repo in a codespace OR clone and open in VS Code locally. With the dev container extension installed, open the VS Code command palette and search for "add dev container configuration files." Choose the Anaconda3 + PosgreSQL option. Then select the "poetry" option for "features". Use the default settings and confirm that you have a `.devcontainer` folder in your project folder. Rebuild your codespace, or select "reopen in dev container" from the comman palette" if you're working locally.

1. Create a function that takes the number of rows, number of columns, and dtype as input arguments and outputs a DataFrame with simulated data from Faker. You only need to implement bool, int, float, str, and datetime dtypes.


3. Create a third function that takes
- a dataframe
- A string designating "columns" or "rows"
- A string designating a dtype

Implement a while loop that takes the dataframe and writes it to a CSV using the appropriate Pandas function. Use the ``timeit`  module to record the runtime of the write operation until the operation takes half a second. Store the number in a DataFrame where each row contains the number of rows/columns at the half second mark, dtype, and the runtime. Delete the csv before exiting the function.

See the Pandas [I/O docs](https://pandas.pydata.org/pandas-docs/stable/user_guide/io.html) if you need help with syntax.

4. Create a final function that uses the previous DataFrame with the results of the benchmarking. Use the built in Pandas bar plot functions to create a plot of the results

5. Modify your previous functions to incoporate SQL, HDF, and Parquet data types.
  
