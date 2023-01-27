# Objects
- Generally speaking, Objects are entities that have data and behavior. In VTK, however, Objects often separate the data and the behavior.

## Attributes
- Attributes define the state of an object. They have a name, data type, and data value.

## Classes

## Instance
- A specific instance of an object.

## Instantiation
- The process of initializing an object from a class, this includes defining initial state.

## Methods
- Methods are functions that are associated with an object.

## Operations
- Functions that can be applied to an object, these are called methods when the operations are being implementing on a specific object.

## Properties
- The combination of attributes and methods that define a given object.

# Types Of Objects in VTK.js
- There are three primary types of objects in the *visualization pipeline*: mapper objects, process objects, and filter objects. In addition there are data objects which are passed through the *visualization pipeline* and acted upon by the other types of objects.

## Data Objects
- Objects that contain data and have methods for accessing and manipulating that data.

## Mapper Objects
- Objects that have one or more input *data objects* AND conclude the *visualization pipeline* by converting data to graphical primitives. These may also be called *sinks*.

### Writer Objects
- A specific type of mapper object that writes data to a file or interface (e.g. on another device or of another application).

## Process Objects
- Objects that operate on input data and generate output data. This can be the creation of new data or transformation of the existing data.

### Filter Objects
- A specific type of process object that has both input and output processes (as opposed to a source object which only has an output process or a mapper object which only has an input process).

### Source Objects
- A specific type of process object that interfaces with external data sources OR generates data from provided parameters.
- Source objects may also be called *data source objects* or *sources*.

#### Procedural Objects
- A source object that generates data from provided parameters.

#### Reader Objects
- A source object that reads in external data and transforms it into a format usable by VTK.