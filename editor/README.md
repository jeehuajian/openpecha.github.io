# OpenPech Editor

## HFML
HFML—Human-Friendly Markup Language (https://github.com/OpenPecha/hfml)—is a markup language meant to help readers, including non-specialists, contribute meaningful semantic annotations to etexts in plain text format. They are flexible, and updatable. Some common tags only require an identifier at the tag start (title, author, chapter, etc.). For example: <k1བྱང་ཆུབ་སེམས་དཔའི་སྤྱོད་པ་ལ་འཇུག་པ་བཞུགས་སོ།།>. Here, “k1” is an annotation identifier for a title annotation. In case of possible overlapping tags, an identifier is needed at both start and end (citations, definitions, instances, etc.). For example: <gའགྲོ་ལ་ཕན་པར་བྱེད་རྣམས་ལམ་ཤེས་ཉིད་ཀྱིས་འཇིག་རྟེན་དོན་སྒྲུབ་མཛད་པ་གང་g>ཞེས་གསུངས་པ་ཡིན་པའི་ཕྱིར།. In some cases, a tag needs to contain a payload, especially for an annotation like a correction to the text: <error,suggestion>. 
To track HFML annotations across versions, every annotation is given a unique ID (unique IDs are essential for annotation transfer as well as linked data). As mentioned above, embedding IDs directly can lead to unwieldy character strings that are unintuitive for users (OPF utilizes UUID4). So OpenPecha makes use of Tofu-IDs. These are user-friendly, since they embed as single characters, while still preserving annotation IDs. In other words, annotations in OPF are tracked using UUID4 (a system of universally unique identifiers); in HFML, this UUID is rendered as a Tofu-ID to give it a user-friendly view. 

# Editor
[Openpecha editor](http://editor.openpecha.org/P000100) uses [HFML](https://github.com/OpenPecha/hfml) for creating and 
uploading new annotations, and [openpecha-toolkit](https://github.com/OpenPecha/openpecha-toolkit) for parsing annotated
text from the editor and converting OPF pecha to format like .epub.
