# System.IO

### Reading List:

##### [File and Stream I/O](https://docs.microsoft.com/en-us/dotnet/standard/io/)
##### [Write to a file](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-write-text-to-a-file)
##### [Read to a file](https://docs.microsoft.com/en-us/dotnet/standard/io/how-to-read-and-write-to-a-newly-created-data-file)
---

#### File and Stream I/O

File and stream I/O (input/output) - the transfer of data either to or from a storage medium. 

In the .NET Framework, the System.IO namespaces contain types that enable reading and writing, both synchronously and asynchronously, on data streams and files.

*File V. Stream* - A file is an ordered and named collection of bytes that has persistent storage. A stream is a sequence of bytes that you can use to read from and write to a backing store, which can be one of several storage mediums 

**Files and directories**

You can use the types in the System.IO namespace to interact with files and directories. For example, you can get and set properties for files and directories, and retrieve collections of files and directories based on search criteria.

*Commonly used file and directory classes*: File, FileInfo, Directory, DirectoryInfo, Path.


**Streams**

Streams involve three fundamental operations:

*Reading* - transferring data from a stream into a data structure, such as an array of bytes.

*Writing* - transferring data to a stream from a data source.

*Seeking* - querying and modifying the current position within a stream.

*Commonly used stream classes*: FileStream, IsolatedStorageFileStream, MemoryStream, BufferedStream,  NetworkStream, PipeStream, CryptoStream.

**Readers and writers**

The reader and writer types handle the conversion of the encoded characters to and from bytes so the stream can complete the operation. Each reader and writer class is associated with a stream, which can be retrieved through the class's BaseStream property.

*Commonly used reader and writer classes*: BinaryReader and BinaryWriter, StreamReader and StreamWriter, StringReader and StringWriter, TextReader and TextWriter.

**Asynchronous I/O operations**

Reading or writing a large amount of data can be resource-intensive. You should perform these tasks asynchronously if your application needs to remain responsive to the user. 

With synchronous I/O operations, the UI thread is blocked until the resource-intensive operation has completed. 

The asynchronous members contain Async in their names. You use these methods with the async and await keywords.

**Compression**

The System.IO.Compression namespace contains types for compressing and decompressing files and streams.

*Commonly used compressing and decompressing classes*: ZipArchive, ZipArchiveEntry, ZipFile, ZipFileExtensions, DeflateStream, GZipStream.

**Isolated storage**

Isolated storage is a data storage mechanism that provides isolation and safety by defining standardized ways of associating code with saved data. 
The storage provides a virtual file system that is isolated by user, assembly, and (optionally) domain.

**I/O and security**

When you use the classes in the System.IO namespace, you must follow operating system security requirements such as access control lists (ACLs) to control access to files and directories. 

Default security policies prevent Internet or intranet applications from accessing files on the user’s computer. Therefore, do not use the I/O classes that require a path to a physical file when writing code that will be downloaded over the Internet or intranet.
