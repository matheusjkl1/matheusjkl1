### Welcome! 歓迎します👋

[Curriculo](https://gitconnected.com/matheusjkl1)
[Linkedin](https://www.linkedin.com/in/matheusmendes16/)

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=matheusjkl1&show_icons=true&theme=dark)

import json
from dataclasses import asdict, dataclass


@dataclass
class Stack:
    languages   : tuple = ("Python", "JS", "Go")
    databases   : tuple = ("PostgreSQL", "Mongo", "Redis")
    misc        : tuple = ("Docker", "Celery", "RabbitMQ")
    ongoing     : tuple = ("Django", "DRF", "Trio")

    def serialize(self):
        return json.dumps(asdict(self), indent=4)


stack = Stack()
print(stack.serialize())
