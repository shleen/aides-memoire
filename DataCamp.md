# An Exhaustive Compilation of Learnings from Various DataCamp Courses

It seems I have somehow stumbled upon a DataCamp account that has been paid for for half a year. I musn't waste such an amazing resource, in my quest to determine if Data Science is part of My Career Goals. This will be a documentation of things I have learnt from the various courses I end up taking- disremembering & all that.

Enjoy.


### Courses taken (or, as indicated, in the process of taking)
- [Convolutional Neural Networks for Image Processing](https://www.datacamp.com/courses/convolutional-neural-networks-for-image-processing)


## General
// General information picked up from the courses I take will be filed here.

A **tidy** dataset contains a single observation in each row & each column contains a variable.

## Python
// Learnings pertaining to the Python programming language will be filed here.

#### matplotlib
- Install (from the terminal) with `pip3 install matplotlib`.
- Import with `import matpotlib as mpl`.

**Displaying an image**
```python
# Load the image
img = mpl.pyplot.imread('img_location.png')

# Display the image
mpl.pyplot.imshow(img)
mpl.pyplot.show()
```

**Modifying the colors of an image**

Assume that we've loaded the image with `img = mpl.pyplot.imread('img_location.png')`.

`img` is now an array containing a child array [x, y, z] for each pixel in `img`. x & y correspond with the location of the pixel in the image in question, & z is yet another array [r, g, b] where r, g, & b are all between 0 & 1 & are indicative of the strength of each color channel in the pixel in question. i.e. a red pixel has a z = [1, 0, 0].

We can now modify the colors in the image- for example, creating a red square in the top-left 20x20 pixels in `img`.
```python 
# Modify the red channel
img[:20, :20, 0] = 1

# Modify the green channel
img[:20, :20, 1] = 0

# Modify the blue channel
img[:20, :20, 2] = 0

# Display the image
mpl.pyplot.imshow(img)
mpl.pyplot.show()
```

#### numpy
- Install (from the terminal) with `pip3 install numpy`.
- Import with `import numpy as np`.

**one-hot encoding image labels**
```python
# Get the total number of categories
# It's possible to explore doing this dynamically- getting the number of unique values in the label column, for example.
n_categories = 3

# Store all your categories
# Doing this dynamically is definitely also possible. 
categories = np.array(['category 1', 'category 2', 'category 3'])

# Initialize your dummy columns (all values default to zero)
# nrow = number of rows in your dataset
# ncol = number of unique categories
ohe_labels = np.zeros(len(dataframe), n_categories)

# Do the encoding
for i in range(len(dataframe))L
    # Get the column corresponding with the label
    j = np.where(dataframe['label'][i] == categories)

    # Update the value accordingly
    ohe_labels[i, j] = 1
```

#### keras
- Install (from the terminal) with `pip3 install keras`.
- Import with `import keras as k`.

**Building a fully connected model**
```python
# Initialize the model
model = k.models.Sequential()

# Create input layer 
# Note- the first parameter into k.layers.Dense() represents the complexity of relationships the model is able to follow. 
#       input_shape represents the number of connections between the input & the first layer. This is typically the number of pixels in your images. This example takes 28x28 images, hence 784.
model.add(k.layers.Dense(10, activation='relu', input_shape=(784,,)))

# Create hidden layer
model.add(k.layers.Dense(10, activation='relu'))

# Create output layer
model.add(k.layers.Dense(n_categories, activation='softmax')

# Compile the model
# Declare the optimization & loss functions to use, as well as any additional metrics to report
model.compile(optimizer='adam',
              loss='categorical_crossentropy',
              metrics=['accuracy'])

# Fit the model to the training data
model.fit(train_data, train_labels, 
          validation_split=0.2,
          epochs=3)

# Evaluate the model (i.e. put the testing data into the model)
model.evaluate(test_data, test_labels)
```

## R
// Learnings pertaining to the R programming language will be filed here.

### Data Descriptions- The R Way
- `base` package's `str()` function. Can be used on basically anything & will more often than not provide a useful overview of some key characteristics of the given object.
- `dplyr` package's `glimpse()` function. Gives you the same information as `base` package's `str()` but gives as comprehensive a preview of the data as possible.

#### tidyr
- Install with `install.packages('tidyr')`.
- Load into the current environment with `library('tidyr')`.

- Used to, ykno, tidy your data.

**gather()**

Used when a dataset has columns that aren't variables, that you want to collapse into key-value pairs.

**spread()**

The opposite of `gather()`. Takes key-value pairs & spreads them across multiple columns. Is useful when column values should be column names. Helps in compacting a dataset

**separate()**

Used to split a single column into multiple. e.g. column **year\_mo** contains strings like **2018\_02** representing the observation's year & month stamps. We'd use `separate()` to split this column into a **year** & **month** column, each with their corresponding values. By default, any non-alphanumeric character is used as the delimiter.

**unite()**

The opposite of `separate()`. Concatenates given columns, by default, using underscores. 

#### lubridate
- Install with `install.packages('lubridate')`.
- Load into the current environment with `library('lubridate')`.

- Used to parse & handle datetime values in R.

#### stringr
- Install with `install.packages('stringr')`.
- Load into the current environment with `library('stringr')`.

- Used for string manipulation purposes.

#### ggplot2
- Install with `install.packages('ggplot2')`.
- Load into the current environment with `library('ggplot2')`.

- Perhaps the most widely used data visualization package for R.

**The `position` Argument**

Used with bar plots- `geom_bar()` & `geom_histogram()` to indicate how the plot's bars should be drawn. Possible values- 

- `stack`: (default) Bars are indicative of counts & are stacked vertically.
- `fill`: Bars are indicative of proportions & are stacked vertically.
- `dodge`: Bars are indicative of counts & are placed horizontally adjacent to each other.
