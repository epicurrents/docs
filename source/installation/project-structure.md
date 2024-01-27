Project structure
=================

The EpiCurrents project consists of four base components:
* The [core library](https://github.com/epicurrents/core).
* Modules for each individual study type.
* Loaders for each individual file format.
* Services that can be run in web workers.

## The core library

The EpiCurrents core library contains the EpiCurrents application class. All the other components must be registered to the core application in order to be used. In addition to the core application class itself, the library contains abstract base classes for most study types, services and loaders that can be used to build more specialized components.

## Study modules

A study module contains all the necessary classes and services for a study type (e.g. EEG or EMG) to be used in the application. Study modules are not tied to a specific file format but can be complemented with loaders of appropriate types.

## File loaders

A file loader is used to load (and if necessary, decode) files of a specific format into physical signals or other generic data types. A file loader may serve only a specific export format for a single study type, or a more general purpose file format like EDF.

## Services

Services offer additional functionality that a user may optionally incorporate into the application. The original intended purpose was to allow off-loading compute-intensive tasks to web workers, but they are not limited to this single design.