# Python Streaming Support Library

Python version of the .NET Support Library. Used for when natively using Python to interact with Stream API using the Support Library.
All calls to the Support Library have been converted to Python.

At the moment this library only supports Windows.

## Requirements
- `Python >= 3.13`
- `protobuf >= 6.31.1`

## Install
Copy the following line for installing the python package while replacing all items for `{RELEASE VERSION HERE}` to the desired release version:

`python -m pip install https://github.com/Software-Products/MA.DataPlatforms.Streaming.Support.Library/releases/download/v{RELEASE VERISON HERE}/ma_dataplatforms_streaming_support_library-{RELEASE VERSION HERE}-py3-none-any.whl`

## Usage

Before using the package, you must add the following lines:

```
streaming_api_configuration = StreamingApiConfiguration(
    "localhost:9092", StreamCreationStrategy.TOPIC_BASE, [], 10
)
logger = Logger()
support_lib_api_factory = SupportLibraryBootstrapper.bootstrap(
    streaming_api_configuration, logger
)
```

This initialises the library and then gives you a support library factory which you can use to create the support library.

From there, all library calls are similar to those of the .NET Support Library.

## Sample Code
For sample code, please look at the [Sample Code Repository](https://github.com/mat-docs/MA.DataPlatforms.Streaming.Support.Library.SampleUsage)
