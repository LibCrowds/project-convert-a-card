# project-convert-a-card

:warning: This task presenter is now built in to https://github.com/LibCrowds/libcrowds

This is the template for the Convert-a-Card projects seen on LibCrowds. The
project relies on an instance of the
[pybossa-z3950](https://github.com/alexandermendes/pybossa-z3950) plugin to be
running on your PyBossa server. Your CORS settings will also need to be setup to
allow queries to that server from wherever this project is running.


## Supported languages

The following languages (or writing systems) are currently supported:

- Pinyin
- Indonesian
- Urdu

To add support for another language update the `libs` variable and `getLibs()`
function in [template.html](template.html) and add a descriptive paragraph
to the bottom of [long_description.md](long_description.md).
