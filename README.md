# energy_geopolitics_transform
Of vital concern to the efficient use of global energy resources is to measure how productive energy use is. This is with the assumption that the supply of natural resources is finite. There are several metrics at the country level that may be pertinent in the discussion of global energy use.

The database itself is a collection of tuples implemented on a relational database management system (RDBMS), here PostgreSQL. There are six (6) relations for countries, country population, country gross domestic product, power plants, estimated power generation by power plants, and pollutants produced in the process of producing energy (or energy balance). With the exception of the relations countries and power plants, the other four (4) relations are weak entities with numeric attributes with the exception of their foreign key VARCHAR attribute.

Simple tabular reports listing global power plants and their locations, and estimated generation by power plant type. The international politics and relations aspect of this database implementation will be the energy balance for each country and how their population density and gross domestic product may affect future energy consumption behavior.

There are many resources on the internet including:

https://www.belfercenter.org/project/geopolitics-energy-project#:~:text=the%20late%201970s.-,The%20Geopolitics%20of%20Energy%20Project%20explores%20the%20intersection%20of%20energy,challenges%20to%20global%20energy%20security.

THE SQL COMPONENT
The current system stores its data and information in six relational database tables or relations within a single
PostgreSQL database accessible via phpPgAdmin or PuTTY Secure Shell connections from the Windows operating system. 

There are a minimum of design criteria as the six relations do not require flexibility for change. Because of the tuple
basis of the relations, a RDBMS was deemed suitable. Given that the current database holds time series or historical
data, it is unlikely to present difficulties for a rigid framework as is a relational database system. And since, the data
itself fits well into such a rigid schema, the database should be extremely efficient.

Constraints for the database are maintained through the use of keys and foreign keys, latter to maintain referential
integrity. Constraints against duplication are enforced through the use of primary keys and foreign keys.

The current power plant system is not foreseen to add attributes. That being the case, inserting nearly infinite tuples
should only pose issues of storage of large swaths of data. It is conceivable that the database can be distributed over
various nodes with copies of portions of the database per node. For example, the first 20 countries where the
country names start with the alphabet letter ‘a’ can be one such copy. Such horizontal scaling implementation would
present overall lower costs. Temporary views of the data for other countries can be conceivably stored in Views for
more complex analysis or reports. In the worst case, one week should be sufficient to rebuild the database in cases
where new attributes should be integrated into one or more relations within the existing database schema.
