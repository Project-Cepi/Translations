# Translations
The central library for all translations for Cepi.

## Format
All translations are located in `src/`.
Each translation is seperated via namespace.

There is one common namespace, called `common`.
This namespace is shared between everything,
EX unknown command or no permission messages.

Namespaces usually depend on the extension,
EX `item` for the item extension namespace.

Locale codes can be found in the [Minecraft Wiki](https://minecraft.fandom.com/el/wiki/Language#:~:text=The%20choice%20of%20languages%20is,change%20the%20in%20game%20language.).

The whole format goes as this:

`src/{namespace}/bundle_{locale_code}.properties`

The file format for `.properties`
can be found at [Wikipedia](https://en.wikipedia.org/wiki/.properties)

It's usually seperated by key, for example: 


```properties
some.value = Hello
some.value2 = World

other.value = We
other.value2 = He
```

## Common Errors

[From Wikipedia](https://en.wikipedia.org/wiki/.properties)

The key characters =, and : should be written with
a preceding backslash to ensure that they are properly loaded.

Don't use quotes -- if you contributed a bunch of translations but they all have quotes, use the regex `"([\w \d%!':]+)"` on the src/ folder.