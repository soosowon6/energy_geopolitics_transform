# energy_geopolitics_transform
Of vital concern to the efficient use of global energy resources is to measure how productive energy use is. This is with the assumption that the supply of natural resources is finite. There are several metrics at the country level that may be pertinent in the discussion of global energy use.  The database itself is a collection of tuples implemented on a relational database management system (RDBMS), here PostgreSQL. There are six (6) relations for countries, country population, country gross domestic product, power plants, estimated power generation by power plants, and pollutants produced in the process of producing energy (or energy balance). With the exception of the relations countries and power plants, the other four (4) relations are weak entities with numeric attributes with the exception of their foreign key VARCHAR attribute.  Simple tabular reports listing global power plants and their locations, and estimated generation by power plant type. The international politics and relations aspect of this database implementation will be the energy balance for each country and how their population density and gross domestic product may affect future energy consumption behavior.