XML and SOAP Play library
=========================

XML and SOAP Play library, for Scala to serialize/deserialize XML (and SOAP) without code generation or other magic.

You may use this api if like me:
- You don't like SOAP because it's not human-friendly at all, it's too verbose and the surrounding standards are just non-sense
- You hate WSDL because it's not humanly readable and requires tools to manipulate them
- You must pollute your code with esoteric annotations just to do RPC in the great majority of cases 
- You hate all those bloated frameworks to manage SOAP and the crazy standards around it
- You don't understand why we still use SOAP but you still have to communicate in SOAP in many cases so you still must bear it
- You just want to extract the data you need from SOAP frames you receive and to generate SOAP frames that look like what your client expect but you don't care about the standards behind that.

**This API is just a set of tools, almost only syntactic sugar to help you**:
- It DOES NOT pretend to provide pure standard SOAP.
- It DOES NOT generate WSDL so you must provide it yourself.
- It just helps you mimic SOAP by providing a few tools and helpers to deserialize/serialize.
- It just aims at being practical without needing deep knowledge of SOAP standards.
- It can serialize/deserialize SOAP so it can also do it for XML...
- It uses pure Scala XML library even if it's a bit incoherent sometimes. AntiXML could be cool too...

More information on https://github.com/giabao/scala-soap

### Install
add to build.sbt:
`libraryDependencies += "com.sandinh" %% "scala-soap" % "1.2.0"`

### Changelogs
##### v1.3.1
+ only update play 2.3.9, scala 2.11.6, scala-xml 1.0.4
+ remove crossBuild for scala 2.10

##### v1.3.0
+ update scala 2.11.5, sbt 0.13.7, slf4j-api 1.7.10, play-ws (optional dependency) 2.3.7
+ add scala-xml 1.0.3 as a dependency for scala-soap _2.11
+ make explicit result type of implicit defs & add `import scala.language.implicitConversions`
+ remove object BasicReaders, SpecialReaders, BasicWriters, SpecialWriters & remove trait DefaultImplicits

##### v1.2.1
+ update scala 2.11.1, play-ws (optional dependency) 2.3.0-RC2

##### v1.2.0
+ cross compile to scala 2.10 & 2.11
+ update optional dependency `play 2.2.2` to `play-ws 2.3.0-RC1`

##### v1.1.2
+ reformat code using scalariform
+ add traits WS11 & WS12
+ update scala 2.10.4

##### v1.1.1
+ Only update play 2.2.1 to 2.2.2

##### v1.0.0
+ Change package to com.sandinh
+ Add com.sandinh.soap.WS. Usage: see [WSSpec](https://github.com/giabao/scala-soap/blob/master/src/test/scala/com/sandinh/soap/WSSpec.scala)
+ Optional depends on "play" (require if you use WS)

##### v0.9.0
First version.

### Licence
This software is licensed under the Apache 2 license:
http://www.apache.org/licenses/LICENSE-2.0

Credits to Pascal Voitot and Paweł Prażak for previous version of this codebase

Credits to Étienne Vallette d'Osia for inspiring/tackling draft version of this code ;)
