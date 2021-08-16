# Practice
This project lets Jake contain his work on practice problems for various languages in one place. It is primarily intended to help organize interview prep.

## Disclaimer
Everything is tailored to Jake's development environment. Very little effort has been put into this being usable by others. It assumes the user is on a *nix system, and it relies on the user to have a command-line compiler/interpreter preconfigured for whatever language they wish to practice. All that said, if you still wish to fork this for your own purposes, go for it :)

## Practicing
Whenever you want to practice with a new question, do the following:
1. Ensure the language you're practicing is already configured. See [Adding a new Language](#add).
1. Ask the question you wish to answer. See [Asking a New Question](#ask).
1. Check your solution to the question. See [Checking Your Solution](#check).

### <a name="ask"></a>Asking a New Question
To ask a new question, run `ask.sh` in Terminal.

#### Generic Command
```
cd ~/<path>/<to>/practice
sh ask.sh <langauge> <question>
```

#### Example
```
cd ~/workspace/practice
sh ask.sh ruby merge_sort
```

### <a name="check"></a>Checking Your Solution
To check the outcome of your solution, run `check.sh` in Terminal.

#### Generic Command
```
cd ~/<path>/<to>/practice
sh check.sh <langauge> <question>
```

#### Example
```
cd ~/workspace/practice
sh check.sh java FizzBuzz
```

### <a name="add"></a>Adding a new Language
To add a new language, run `add-language.sh` in Terminal. This will come with configuration questions, so follow the dialogue until it confirms your new language.

**You must have a terminal command preconfigured in your development environment to compile/interpret any language you wish to add.** 

#### Generic Command
Without accounting for follow up questions, beginning to add a langauge looks like this:
```
sh add-language.sh <language>
```

If you wish to overwrite an existing language configuration, use the overwrite flag by writing `-o` after the langauge name:
```
sh add-language.sh <langauge> -o
```

#### Full Example for Adding Ruby
```
> cd ~/workspace/practice
> sh add-language.sh ruby
Which naming convention does ruby follow: snake_case, kebab-case, or PascalCase?
Acceptable responses are: snake, kebab, pascal, and cancel
> snake
What command can I use to run ruby from Terminal?
> ruby
Great! Everything is now configured for practicing ruby!
```
