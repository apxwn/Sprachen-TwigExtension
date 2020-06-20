# Sprachen TwigExtension
## simple language related Twig Extensions

Two simple functions for Twig:

1. sprachen

Returns the name of a language in another language.

Usage: `sprachen(language_code, target_language_code)`

For example:

`{{ sprachen('de','ru')|capitalize }}`

returns:

`Немецкий`

2. accentsort

Returns a sorted array. Sorting goes in accordance to target language (e.g., considers accents).

Usage: `accentsort(array, language_code)`

For example:

`{% set array_alphabetisch = accentsort(array, grav.language.getActive) %}`

could return:

`Array (
    [0] => Álpha
    [1] => Àlpha
    [2] => Älpha
    [3] => かたかな
    ...
    )`
