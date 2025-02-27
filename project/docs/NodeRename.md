
# Class: node rename


A node change where the name (aka rdfs:label) of the node changes

URI: [kgcl:NodeRename](http://w3id.org/kgcl/NodeRename)


[![img](https://yuml.me/diagram/nofunky;dir:TB/class/[TextualDiff],[TextualDiff]<has%20textual%20diff%200..1-++[NodeRename&#124;old_value:string%20%3F;new_value:string%20%3F;change_description:string%20%3F;about_node_representation(i):string%20%3F;language(i):language_tag%20%3F;old_value_type(i):string%20%3F;new_value_type(i):string%20%3F;new_language(i):string%20%3F;old_language(i):string%20%3F;new_datatype(i):string%20%3F;old_datatype(i):string%20%3F;id(i):string;type(i):string%20%3F;see_also(i):string%20%3F;pull_request(i):string%20%3F;creator(i):string%20%3F;change_date(i):string%20%3F;contributor(i):string%20%3F],[NameBecomesSynonym]-%20change%201%200..1>[NodeRename],[NodeChange]^-[NodeRename],[NodeChange],[Node],[NameBecomesSynonym],[Change],[Activity])](https://yuml.me/diagram/nofunky;dir:TB/class/[TextualDiff],[TextualDiff]<has%20textual%20diff%200..1-++[NodeRename&#124;old_value:string%20%3F;new_value:string%20%3F;change_description:string%20%3F;about_node_representation(i):string%20%3F;language(i):language_tag%20%3F;old_value_type(i):string%20%3F;new_value_type(i):string%20%3F;new_language(i):string%20%3F;old_language(i):string%20%3F;new_datatype(i):string%20%3F;old_datatype(i):string%20%3F;id(i):string;type(i):string%20%3F;see_also(i):string%20%3F;pull_request(i):string%20%3F;creator(i):string%20%3F;change_date(i):string%20%3F;contributor(i):string%20%3F],[NameBecomesSynonym]-%20change%201%200..1>[NodeRename],[NodeChange]^-[NodeRename],[NodeChange],[Node],[NameBecomesSynonym],[Change],[Activity])

## Parents

 *  is_a: [NodeChange](NodeChange.md) - A simple change where the change is about a node

## Referenced by Class

 *  **None** *[change 1](change_1.md)*  <sub>0..1</sub>  **[NodeRename](NodeRename.md)**
 *  **[NameBecomesSynonym](NameBecomesSynonym.md)** *[name becomes synonym➞change 1](name_becomes_synonym_change_1.md)*  <sub>0..1</sub>  **[NodeRename](NodeRename.md)**

## Attributes


### Own

 * [node rename➞old value](node_rename_old_value.md)  <sub>0..1</sub>
     * Description: The value of a property held in the old instance of the ontology
     * Range: [String](types/String.md)
 * [node rename➞new value](node_rename_new_value.md)  <sub>0..1</sub>
     * Description: The value of a property held in the new instance of the ontology
     * Range: [String](types/String.md)
 * [has textual diff](has_textual_diff.md)  <sub>0..1</sub>
     * Description: A representation of character-level changes on a textual literal property. For example, if a text definition may change by only a single character such as addition of a period, it is useful to be able to see this visually.
     * Range: [TextualDiff](TextualDiff.md)
 * [new language](new_language.md)  <sub>0..1</sub>
     * Description: The new language tag of a literal
     * Range: [String](types/String.md)
 * [old language](old_language.md)  <sub>0..1</sub>
     * Description: The old language tag of a literal
     * Range: [String](types/String.md)
 * [node rename➞change description](node_rename_change_description.md)  <sub>0..1</sub>
     * Description: A string serialization of the change. This should be both human-readable, and parseable.
     * Range: [String](types/String.md)
     * Example: rename UBERON:0002398 from 'manus' to 'hand' None
     * Example: move 'hand' from 'part of' 'hindlimb' to 'part of' 'forelimb' None
     * Example: merge 'cellular metabolic process' into 'metabolic process' None
     * Example: search and replace 'metabolic process' with 'metabolism' in all labels under 'biological process' None
     * Example: search and replace 'metabolic process' with 'metabolism' in all labels under 'biological process' retaining as 'exact synonym' None

### Inherited from node change:

 * [id](id.md)  <sub>1..1</sub>
     * Range: [String](types/String.md)
 * [type](type.md)  <sub>0..1</sub>
     * Range: [String](types/String.md)
 * [change➞was generated by](change_was_generated_by.md)  <sub>0..1</sub>
     * Range: [Activity](Activity.md)
 * [change➞see also](change_see_also.md)  <sub>0..1</sub>
     * Range: [String](types/String.md)
 * [change➞pull request](change_pull_request.md)  <sub>0..1</sub>
     * Range: [String](types/String.md)
 * [change➞creator](change_creator.md)  <sub>0..1</sub>
     * Range: [String](types/String.md)
 * [change➞change date](change_change_date.md)  <sub>0..1</sub>
     * Range: [String](types/String.md)
 * [contributor](contributor.md)  <sub>0..1</sub>
     * Range: [String](types/String.md)
 * [has undo](has_undo.md)  <sub>0..1</sub>
     * Description: A change that reverses this change
     * Range: [Change](Change.md)
 * [old value type](old_value_type.md)  <sub>0..1</sub>
     * Description: The type (IRI or Literal) of an old value
     * Range: [String](types/String.md)
 * [new value type](new_value_type.md)  <sub>0..1</sub>
     * Description: The type (IRI or Literal) of a new value
     * Range: [String](types/String.md)
 * [new datatype](new_datatype.md)  <sub>0..1</sub>
     * Description: The new datatype of a literal
     * Range: [String](types/String.md)
 * [old datatype](old_datatype.md)  <sub>0..1</sub>
     * Description: The old datatype of a literal
     * Range: [String](types/String.md)
 * [about node](about_node.md)  <sub>0..1</sub>
     * Range: [Node](Node.md)
 * [about node representation](about_node_representation.md)  <sub>0..1</sub>
     * Description: The representation of a node (URI, CURIE, label) 
     * Range: [String](types/String.md)
 * [language](language.md)  <sub>0..1</sub>
     * Description: The language tag of a literal
     * Range: [LanguageTag](types/LanguageTag.md)

## Other properties

|  |  |  |
| --- | --- | --- |
| **Examples:** | | Example(value="rename UBERON:0002398 from 'manus' to 'hand'", description="replacing the rdfs:label of 'manus' on an uberon class with the rdfs:label 'hand'") |

