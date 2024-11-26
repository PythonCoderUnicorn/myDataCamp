# Data

The datasets used in DataCamp courses that are a mix of available from their course assets folder, data from within the course and copied, data from their data server, and lastly data from Kaggle.
Data in `.RDA` or `.RDS` will be converted to `CSV` for widespread use and utility, same goes for Python pickle files.

Note:

Datasets will have the course name or associated wording to the dataset as to indicate which dataset belongs to what course. `DataShell_Spotify_Popularity.csv` belongs to the course Data Science using the Terminal. 

----

`.fst` files
```
install.packages("fst")
library(fst)
df <- read_fst("your_data.fst")
```

feather files
```
pip install pyarrow
import pyarrow.feather as feather
df = feather.read_feather('your_file.feather')
```

pickle `.pkl`
```
import pickle
# Replace 'your_file.p' with the path to your file
with open('your_file.p', 'rb') as file:
    data = pickle.load(file)

print(data)
```

`.sav` file
```
library(haven)
haven::read_sav("importingData_big5.sav")
```

`.dta` STATA file 
```
library(haven)
haven::read_dta("importingData_educationequality.dta")
```

for Network Analysis using the networkx library `.p` file (cannot be coerced into .pkl)
```
import networkx as nx

# Load the DiGraph
with open('./Data/twitter_network_ego.p', 'rb') as file:
    G = pickle.load(file)
    

# Analyze the graph
print(G.nodes())
print(G.edges())

# Visualize the graph
nx.draw(G, with_labels=True)
```

twitter_network_ego.p file content
```
 .... (23233, 19681), (23233, 23265), (23233, 23266), (23233, 23267), (23233, 19682), (23233, 23268), (23233, 23269), (23233, 23270), (23233, 23271), (23233, 23272), (23233, 23273), (23233, 23274), (23233, 19673), (23233, 23275), (23233, 23276), (23233, 23277), (23233, 23278), (23233, 23279), (23233, 23280), (23233, 23281), (23233, 23282), (23233, 23283), (23233, 23284), (23285, 23286), (23285, 23287), (23285, 23288), (23285, 23289), (23285, 23290), (23285, 23291), (23285, 23292), (23285, 23293), (23285, 23294), (23285, 23295), (23285, 23296), (23285, 23297), (23285, 23298), (23285, 23299), (23285, 23300), (23285, 23301), (23285, 23302), (23285, 23303), (23285, 23304), (23285, 23305), (23307, 663), (23307, 23308), (23307, 664), (23307, 23309), (23307, 665), (23307, 2815), (23307, 23310), (23307, 666), (23311, 23312), (23324, 23325), (23324, 23326), (23324, 23327), (23324, 23328), (23324, 23329), (23324, 23330), (23324, 23331), (23324, 23332), (23324, 23333), (23324, 762), (23324, 23334), (23324, 23335), (23324, 23336)]
```














