```
from dataclasses import dataclass, field
from typing import List, Dict

@dataclass
class Sy:
    name: str = "Sy Rashid"
    age: int = 33
    work: List[str] = field(default_factory=lambda: ["ARTSVP", "MangoTree Dev"])
    education: List[str] = field(default_factory=lambda: ["Georgia Tech MSCS", "Le Wagon", "HBX/HBS", "Georgia Tech BSNRE"])
    hobbies: List[str] = field(default_factory=lambda: ["Skydiving", "Snowboarding", "Burritos"])

    def languages(self) -> Dict[str, List[str]]:
        return {
            "human": ["English", "Bengali", "Portuguese", "Spanish"],
            "programming": ["Python", "Go", "JavaScript", "SQL", "C"]
        }

    def currentLocation(self) -> str:
        return "Lisbon, PT"

    def nextLocations(self) -> List[str]:
        return ["Chamonix, FR"]

    def currently(self) -> Dict[str, List[str]]:
        return {
            "studying": ["Natural Language Processing", "Deep Learning", "Language of Proofs"],
            "reading": ["The Moral Animal", "Discrete Mathematics and Its Applications"],
            "tinkering": ["PR Stacking (Graphite)", "Quant Trading", "Frontside Shifty"]
        }
```
