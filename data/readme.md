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

