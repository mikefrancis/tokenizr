tokenizr
========

[![Build Status](https://travis-ci.org/mikefrancis/tokenizr.svg?branch=master)](https://travis-ci.org/mikefrancis/tokenizr) [![Coverage Status](https://coveralls.io/repos/mikefrancis/tokenizr/badge.svg?branch=master&service=github)](https://coveralls.io/github/mikefrancis/tokenizr?branch=master) [![StyleCI](https://styleci.io/repos/26376775/shield)](https://styleci.io/repos/26376775)

PHP library to generate unique, URL friendly tokens. Built with TDD.

## Installation

Add the following to your project's composer.json require block:

    "mikefrancis/tokenizr": "^2.0"

and run `composer update` to pull in the package.

## Basic Usage

Create a new `Tokenizr` instance:

    $tokenizr = new MikeFrancis\Tokenizr\Tokenizr();

and then go ahead and generate some tokens:

    $token = $tokenizr->generate();
    
By default Tokenizr will generate URL friendly, alpha-numeric tokens. If you'd like to change the bank of characters which is used, you can do by overriding the default character set:

    $tokenizr->setCharacters('!@£$%^&*()');
    
You can also set a bunch of tokens first, as not to create duplicates when generating new ones:

    $tokenizr->setExistingTokens(['4uNq1', '6ijRw']);

By default, Tokenizr will generate 5 character strings, but if you'd like them to be longer/shorter just do the following before you generate any tokens:

    $tokenizr->setTokenLength(32);
