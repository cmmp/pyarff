# Pyarff

This is very simple code to read and write arff-based files in python that
consist of only doubles. The reader can also read the class attribute if it 
is of string type in addition to double.

Numpy is used for reading/writing.

## Sample code for reading a file:
```python
import arffreader as ar
X, sup = ar.readarff("highdataproclus.arff")
```

## Sample code for writing a file:
```python
import arffwriter as af

attNames = ['att-' + str(i + 1) for i in xrange(data.shape[1])]
attNames.append("class")

meta = af.Metadata('highdim-proclus-generator', attNames)

# write dataset to stdout:
af.write_arff(data, sup.astype("str"), meta)
```