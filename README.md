```py
from dataclasses import dataclass, field
from typing import List, Dict

@dataclass
class Me:
    name: str = "Gabriel"
    age: int = 16
    education: List[str] = field(default_factory=lambda: ["High School"])
    hobbies: List[str] = field(default_factory=lambda: ["Computer Science", "Fashion", "Music"])

    def languages(self) -> Dict[str, List[str]]:
        return {
            "human": ["English", "French"],
            "programming": ["Python", "Go", "JavaScript", "SQLI", "PHP"]
        }

    def current_location(self) -> str:
        return "France, FR"

    def next_locations(self) -> List[str]:
        return ["Kobe, JP"]

    def currently(self) -> Dict[str, List[str]]:
        return {
            "studying": ["React Native + Next.js", "Rust", "Cybersecurity"],
            "tinkering": ["AI/ML", "Learning Solidity"]
        }
```
