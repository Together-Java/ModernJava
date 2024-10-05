# Validity

Now is this law literally true? No. It can't be. There are more
"properties" you can observe about a piece of software than
people on the planet.

The specific number of degrees your CPU heats up when running a program can, hypothetically, be relied on. Chances are that
won't happen though.

Personally I think that the expanded explanation on his website ([https://www.hyrumslaw.com/](https://www.hyrumslaw.com/)) is
more nuanced than the short version, if a lot less snappy and easy to remember. 

> Over the past couple years of doing low-level infrastructure migrations in one of the most complex software systems on the planet, I’ve made some observations about the differences between an interface and its implementations. We typically think of the interface as an abstraction for interacting with a system (like the steering wheel and pedals in a car), and the implementation as the way the system does its work (wheels and an engine). This is useful for a number of reasons, foremost among them that most useful systems rapidly become too complex for a single individual or group to completely understand, and abstractions are essential to managing that complexity.
> 
> Defining the correct level of abstraction is a completely separate discussion (see Mythical Man-Month), but we like to think that once an abstraction is defined, it is concrete. In other words, an interface should theoretically provide a clear separation between consumers of a system and its implementers. In practice, this theory breaks down as the use of a system grows and its users start to rely upon implementation details intentionally exposed through the interface, or which they divine through regular use. Spolsky’s “Law of Leaky Abstractions” embodies consumers’ reliance upon internal implementation details.
> 
> Taken to its logical extreme, this leads to the following observation, colloquially referred to as “The Law of Implicit Interfaces”: Given enough use, there is no such thing as a private implementation. That is, if an interface has enough consumers, they will collectively depend on every aspect of the implementation, intentionally or not. This effect serves to constrain changes to the implementation, which must now conform to both the explicitly documented interface, as well as the implicit interface captured by usage. We often refer to this phenomenon as "bug-for-bug compatibility."
>
> The creation of the implicit interface usually happens gradually, and interface consumers generally aren’t aware as it’s happening. For example, an interface may make no guarantees about performance, yet consumers often come to expect a certain level of performance from its implementation. Those expectations become part of the implicit interface to a system, and changes to the system must maintain these performance characteristics to continue functioning for its consumers.
> 
> Not all consumers depend upon the same implicit interface, but given enough consumers, the implicit interface will eventually exactly match the implementation. At this point, the interface has evaporated: the implementation has become the interface, and any changes to it will violate consumer expectations. With a bit of luck, widespread, comprehensive, and automated testing can detect these new expectations but not ameliorate them.
>
> Implicit interfaces result from the organic growth of large systems, and while we may wish the problem did not exist, designers and engineers would be wise to consider it when building and maintaining complex systems. So be aware of how the implicit interface constrains your system design and evolution, and know that for any reasonably popular system, the interface reaches much deeper than you think.