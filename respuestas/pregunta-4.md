MATCH (p:Persona)-[:VIVE_EN]->(c:Ciudad)
WITH c, count(p) AS total_personas
WHERE total_personas > 2
RETURN c.nombre, total_personas