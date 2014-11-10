tokenizr
========

[![Build Status](https://travis-ci.org/mikefrancis/tokenizr.svg?branch=master)](https://travis-ci.org/mikefrancis/tokenizr)

PHP library to generate unique, URL friendly tokens

## Installation

Add the following to your project's composer.json require block:

    "mikefrancis/tokenizr": "dev-master"

and run `composer update` to pull in the package.

## Basic Usage

Create a new `Tokenizr` instance:

    $tokenizr = new Tokenizr();

and then go ahead and generate some tokens:

    $token = $tokenizr->generate();
    
By default Tokenizr will generate URL friendly, alpha-numeric tokens. If you'd like to change the bank of characters which is used, you can do by overriding the default character set:

    $tokenizr->setCharacters('!@£$%^&*()');
    
You can also set a bunch of tokens first, as not to create duplicates when generating new ones:

    $tokenizr->setExistingTokens(['4uNq1', '6ijRw']);
