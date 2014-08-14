internal_links
=======
SEO tool for adding links to text contained in Django apps databases.

**Renamed package: https://pypi.python.org/pypi/permalink_adder**

# Installation
Install with pip:

    pip install internal_links

# Usage
You need to specify where and what to look for in your Django app's settings in this manner:

    INTERNAL_LINKS_SETTINGS = [{'app': 'your_app_name',
                                'model_name': 'your_model_name',
                                'fields': ['list', 'of', 'fields', 'in', 'which', 'script', 'should', 'search'],
                                'words': ['list', 'of', 'words', 'to', 'search'],
                                'url': 'url_that_should_be_wrapped_around_found_text'
                                'target': False}] # setting it to e.g. '_blank' will add target="_blank" tag to link

Starting script with option `--start` will actually apply changes to database, instead of printing them out.

You can run the script either using `add_links` management command or call `link_adder` function from `adder.py` module. 

# Output
No output if there are no occurrences of words or when they're already wrapped.

Without `--start` option, script will only print out proposed changes.

# Changelog

## 0.1.5 - 14.08.2014
- **[new]** custom target as an option in settings

## 0.1.4.6 - 14.08.2014
- **[new]** package renamed from permalink_adder
- **[update]** improved readability

## 0.1.4.5 - 12.08.2014
- **[new]** dry_run as a command option

## 0.1.4.2 - 8.08.2014
- **[fix]** further description fixes

## 0.1.4.1 - 8.08.2014
- **[fix]** setup fix in order to display description

## 0.1.4 - 8.08.2014
- **[new]** introduced readability to output

## 0.1.3 - 8.08.2014
- **[fix]** bugfix for empty word string case, refactored adder.py

## 0.1.2 - 8.08.2014
- **[fix]** setup.py fix

## 0.1.1 - 8.08.2014
- **[new]** updated with manage.py command

## 0.1 - 8.08.2014
- Initial release