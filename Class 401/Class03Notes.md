# File and Stream I/O

- File and stream I/O (input/output) refers to the transfer of data either to or from a storage medium. In .NET, the System.IO namespaces contain types that enable reading and writing, both synchronously and asynchronously, on data streams and files. These namespaces also contain types that perform compression and decompression on files, and types that enable communication through pipes and serial ports.

A file is an ordered and named collection of bytes that has persistent storage.

## Files and directories

You can use the types in the System.IO namespace to interact with files and directories. 

Here are some commonly used file and directory classes.

- File - provides static methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

- FileInfo - provides instance methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

- Directory - provides static methods for creating, moving, and enumerating through directories and subdirectories.

- DirectoryInfo - provides instance methods for creating, moving, and enumerating through directories and subdirectories.

- Path - provides methods and properties for processing directory strings in a cross-platform manner.


## Streams

The abstract base class Stream supports reading and writing bytes. **All classes that represent streams inherit from the Stream class.** The Stream class and its derived classes provide a common view of data sources and repositories, and isolate the programmer from the specific details of the operating system and underlying devices.

Streams involves three fundamental operations:

- Reading - transferring data from a stream into a data structure, such as an array of bytes.


- Writing - transferring data to a stream from a data source.


- Seeking - querying and modifying the current position within a stream.


- Depending on the underlying data source or repository, a stream might support only some of these capabilities. For example, the PipeStream class does not support seeking. The CanRead, CanWrite, and CanSeek properties of a stream specify the operations that the stream supports.


Here are some commonly used stream classes:

FileStream – for reading and writing to a file.

IsolatedStorageFileStream – for reading and writing to a file in isolated storage.

MemoryStream – for reading and writing to memory as the backing store.

BufferedStream – for improving performance of read and write operations.

NetworkStream – for reading and writing over network sockets.

PipeStream – for reading and writing over anonymous and named pipes.

CryptoStream – for linking data streams to cryptographic transformations.