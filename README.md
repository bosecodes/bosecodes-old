​
from __future__ import annotations

import json
from dataclasses import asdict, dataclass


@dataclass
class Arsenal:
    languages: tuple[str, ...] = ("Python", "C++", "JAVA")
    ml-tech     : tuple[str, ...] = ("Pandas", "ScikitLearn", "Computer Vision", "CNNs")
    web  : tuple[str, ...] = ("Flask", "HTML", "Bootstrap")
    databases: tuple[str, ...] = ("SQLite", "MongoDB", "MySQL")

    def jsonify(self) -> str:
        return json.dumps(asdict(self), indent=4)


arsenal = Arsenal()
print(arsenal.jsonify())
​
