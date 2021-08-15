# Abstraction

Imagine for a minute a world without pronouns. Instead of saying, “He’s nice,” you would have to say, “John F. Jones is nice.”

Now imagine a world without pronouns and proper nouns. Instead of saying, “He’s nice,” or “John F. Junes is nice,” you have to say, “You know that boy I’ve been telling you about? The one with the wavy hair who always dresses so sharply? Who lives in the first floor apartment at 1345 27th Street? Well, he’s nice.”

Abstractions are absolutely everywhere in computers, and they are absolutely essential because we don’t want to have to think about all the details down to how electrons are moving in transistors. We simply assume the machine, the language, or the library, works as if it was as simple as the mental concept the abstraction represents.

It becomes a necessity as systems become complex. We can only hold so many ideas in our heads at once, and can only handle so much complexity in ideas. One way we handle complexity is by "chunking" ideas, breaking them up into concepts, so we can talk about them in terms of themselves, rather than in terms of their supporting components all the time. It's for us, not for the computer.

When you change your code that implements an abstraction, the user of the abstraction doesn't have to change their code. As long as the abstraction doesn't change, the users won't have to change their code. When you write code that uses an abstraction, you can write code once that will be reusable against any new code that implements that abstraction. You can write less code to do more.

