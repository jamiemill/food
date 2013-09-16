# Food

Flat-file database of ingredient by recipe, with shell scripts to query.

This project has two purposes:

- to store a list of my favourite recipies by name, for inspiration purposes
- to spit out the ingredients I need for any set of recipies to make online food shopping painless!

## Usage

The workflow is:

    $ ./ingredients bangers-and-mash.txt french-onion-soup.txt

Zsh makes autocomplete work nicely so I can see the available recipies and don't have to type full names.

The ingredients will be de-duped and output one-per-line for pasting into Tesco Online.

    baguette
    balsamic vinegar
    bangers
    bay leaf
    beef oxo
    butter
    fresh thyme
    frozen peas
    garlic
    gruyére or other melting cheese
    olive oil
    onions (lots)
    potatoes
    red onion
    stock (beef, chicken or veg)

## Adding Recipies

Create a text file named after the recipe, containing its ingredients one-per-line. Comments start with #.

## Tips

Now and then it's probably good to type `./ingredients *.txt` to check for spelling variations that can be normalised.

You can type `./counts` to get a count of the number of recipies each ingredient is used in, to see what is most common and what to keep stocked up.

    10 onion
    10 olive oil
    10 garlic
     8 parmesan
     6 tinned tomatoes
     5 chicken stock
     5 butter
     4 olives
     4 ginger
     4 flour
     ... etc

## Limitations

Doesn't add up quantities or anything clever like that.

I'm not bothering to add the actual recipies, just their names and ingredients. But recipe steps could be added in comment lines starting with # in the same file.

