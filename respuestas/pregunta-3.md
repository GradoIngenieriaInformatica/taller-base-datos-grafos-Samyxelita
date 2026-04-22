MATCH (p:Persona)
WHERE NOT (p)-[:PARTICIPA_EN]->(:Proyecto)
RETURN p.nombre