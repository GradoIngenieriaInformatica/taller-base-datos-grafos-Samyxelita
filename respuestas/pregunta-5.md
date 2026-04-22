MATCH (p1:Persona)-[:TRABAJA_EN]->(e:Empresa)<-[:TRABAJA_EN]-(p2:Persona)
MATCH (p1)-[:VIVE_EN]->(c1:Ciudad)
MATCH (p2)-[:VIVE_EN]->(c2:Ciudad)
WHERE p1 <> p2 AND c1 <> c2
RETURN DISTINCT p1.nombre