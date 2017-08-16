.. FlashText documentation master file, created by
   sphinx-quickstart on Wed Aug 16 22:47:29 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

FlashText's documentation!
=====================================


Installation
------------
::

    $ pip install flashtext

Usage
-----
Simple example
    >>> from flashtext.keyword import KeywordProcessor
    >>> keyword_processor = KeywordProcessor()
    >>> keyword_processor.add_keyword('Big Apple', 'New York')
    >>> keyword_processor.add_keyword('Bay Area')
    >>> keywords_found = keyword_processor.extract_keywords('I love Big Apple and Bay Area.')
    >>> keywords_found
    >>> ['New York', 'Bay Area']

Case Sensitive example
    >>> from flashtext.keyword import KeywordProcessor
    >>> keyword_processor = KeywordProcessor(case_sensitive=True)
    >>> keyword_processor.add_keyword('Big Apple', 'New York')
    >>> keyword_processor.add_keyword('Bay Area')
    >>> keywords_found = keyword_processor.extract_keywords('I love big Apple and Bay Area.')
    >>> keywords_found
    >>> ['Bay Area']

No clean name for Keywords
    >>> from flashtext.keyword import KeywordProcessor
    >>> keyword_processor = KeywordProcessor()
    >>> keyword_processor.add_keyword('Big Apple')
    >>> keyword_processor.add_keyword('Bay Area')
    >>> keywords_found = keyword_processor.extract_keywords('I love big Apple and Bay Area.')
    >>> keywords_found
    >>> ['Big Apple', 'Bay Area']

API doc
-------


.. toctree::
    :maxdepth: 2
    :caption: KeywordProcessor

    api

Contribute
----------

- Issue Tracker: https://github.com/vi3k6i5/flashtext/issues
- Source Code: https://github.com/vi3k6i5/flashtext/


License
-------

The project is licensed under the MIT license.