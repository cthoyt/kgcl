
# Class: node obsoletion


Obsoletion of a node deprecates usage of that node, but does not delete it.

URI: [kgcl:NodeObsoletion](http://w3id.org/kgcl/NodeObsoletion)


[![img](https://yuml.me/diagram/nofunky;dir:TB/class/[OntologyElement],[Obsoletion],[NodeObsoletionWithNoDirectReplacement],[NodeObsoletionWithDirectReplacement],[Change]<associated%20change%20set%200..*-++[NodeObsoletion&#124;change_description:string%20%3F;about_node_representation(i):string%20%3F;language(i):language_tag%20%3F;old_value(i):string%20%3F;new_value(i):string%20%3F;old_value_type(i):string%20%3F;new_value_type(i):string%20%3F;new_language(i):string%20%3F;old_language(i):string%20%3F;new_datatype(i):string%20%3F;old_datatype(i):string%20%3F;id(i):string;type(i):string%20%3F;see_also(i):string%20%3F;pull_request(i):string%20%3F;creator(i):string%20%3F;change_date(i):string%20%3F;contributor(i):string%20%3F],[Node]<has%20nondirect%20replacement%200..*-%20[NodeObsoletion],[Node]<has%20direct%20replacement%200..1-%20[NodeObsoletion],[MultiNodeObsoletion]++-%20change%20set%200..*>[NodeObsoletion],[NodeObsoletion]uses%20-.->[Obsoletion],[NodeObsoletion]^-[NodeObsoletionWithNoDirectReplacement],[NodeObsoletion]^-[NodeObsoletionWithDirectReplacement],[NodeObsoletion]^-[NodeDirectMerge],[NodeChange]^-[NodeObsoletion],[NodeDirectMerge],[NodeChange],[Node],[MultiNodeObsoletion],[Change],[Activity])](https://yuml.me/diagram/nofunky;dir:TB/class/[OntologyElement],[Obsoletion],[NodeObsoletionWithNoDirectReplacement],[NodeObsoletionWithDirectReplacement],[Change]<associated%20change%20set%200..*-++[NodeObsoletion&#124;change_description:string%20%3F;about_node_representation(i):string%20%3F;language(i):language_tag%20%3F;old_value(i):string%20%3F;new_value(i):string%20%3F;old_value_type(i):string%20%3F;new_value_type(i):string%20%3F;new_language(i):string%20%3F;old_language(i):string%20%3F;new_datatype(i):string%20%3F;old_datatype(i):string%20%3F;id(i):string;type(i):string%20%3F;see_also(i):string%20%3F;pull_request(i):string%20%3F;creator(i):string%20%3F;change_date(i):string%20%3F;contributor(i):string%20%3F],[Node]<has%20nondirect%20replacement%200..*-%20[NodeObsoletion],[Node]<has%20direct%20replacement%200..1-%20[NodeObsoletion],[MultiNodeObsoletion]++-%20change%20set%200..*>[NodeObsoletion],[NodeObsoletion]uses%20-.->[Obsoletion],[NodeObsoletion]^-[NodeObsoletionWithNoDirectReplacement],[NodeObsoletion]^-[NodeObsoletionWithDirectReplacement],[NodeObsoletion]^-[NodeDirectMerge],[NodeChange]^-[NodeObsoletion],[NodeDirectMerge],[NodeChange],[Node],[MultiNodeObsoletion],[Change],[Activity])

## Parents

 *  is_a: [NodeChange](NodeChange.md) - A simple change where the change is about a node

## Uses Mixin

 *  mixin: [Obsoletion](Obsoletion.md) - Obsoletion of an element deprecates usage of that element, but does not delete that element.

## Children

 * [NodeDirectMerge](NodeDirectMerge.md) - An obsoletion change in which all metadata (including name/label) from the source node is deleted and added to the target node, and edges can automatically be rewired to point to the target node
 * [NodeObsoletionWithDirectReplacement](NodeObsoletionWithDirectReplacement.md) - An obsoletion change in which information from the obsoleted node is selectively copied to a single target, and edges can automatically be rewired to point to the target node
 * [NodeObsoletionWithNoDirectReplacement](NodeObsoletionWithNoDirectReplacement.md) - An obsoletion change in which there is no direct replacement

## Referenced by Class

 *  **[MultiNodeObsoletion](MultiNodeObsoletion.md)** *[multi node obsoletion➞change set](multi_node_obsoletion_change_set.md)*  <sub>0..\*</sub>  **[NodeObsoletion](NodeObsoletion.md)**

## Attributes


### Own

 * [has direct replacement](has_direct_replacement.md)  <sub>0..1</sub>
     * Description: An obsoletion replacement where it IS valid to automatically update annotations/edges pointing at the node with its direct replacement
     * Range: [Node](Node.md)
 * [has nondirect replacement](has_nondirect_replacement.md)  <sub>0..\*</sub>
     * Description: An obsoletion replacement where it is NOT valid to automatically update annotations/edges pointing at the node with its direct replacement
     * Range: [Node](Node.md)
 * [node obsoletion➞change description](node_obsoletion_change_description.md)  <sub>0..1</sub>
     * Description: A string serialization of the change. This should be both human-readable, and parseable.
     * Range: [String](types/String.md)
     * Example: rename UBERON:0002398 from 'manus' to 'hand' None
     * Example: move 'hand' from 'part of' 'hindlimb' to 'part of' 'forelimb' None
     * Example: merge 'cellular metabolic process' into 'metabolic process' None
     * Example: search and replace 'metabolic process' with 'metabolism' in all labels under 'biological process' None
     * Example: search and replace 'metabolic process' with 'metabolism' in all labels under 'biological process' retaining as 'exact synonym' None
 * [node obsoletion➞associated change set](node_obsoletion_associated_change_set.md)  <sub>0..\*</sub>
     * Description: All changes forced as a result of this obsoletion. For example, starting with `A subClassOf B subClassOf C`, if we obsolete node B, then we may decide to bundle in a node move change of A from B to C. Note: this change set is not considered a part of the obsoletion, as obsoletion is considered atomic/simple. Instead this is a reference to a change set that may exist elsewhere
     * Range: [Change](Change.md)

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
 * [old value](old_value.md)  <sub>0..1</sub>
     * Description: The value of a property held in the old instance of the ontology
     * Range: [String](types/String.md)
 * [new value](new_value.md)  <sub>0..1</sub>
     * Description: The value of a property held in the new instance of the ontology
     * Range: [String](types/String.md)
 * [old value type](old_value_type.md)  <sub>0..1</sub>
     * Description: The type (IRI or Literal) of an old value
     * Range: [String](types/String.md)
 * [new value type](new_value_type.md)  <sub>0..1</sub>
     * Description: The type (IRI or Literal) of a new value
     * Range: [String](types/String.md)
 * [new language](new_language.md)  <sub>0..1</sub>
     * Description: The new language tag of a literal
     * Range: [String](types/String.md)
 * [old language](old_language.md)  <sub>0..1</sub>
     * Description: The old language tag of a literal
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

### Mixed in from obsoletion:

 * [obsoletion➞about](obsoletion_about.md)  <sub>0..1</sub>
     * Description: The element that is obsoleted by this change.
     * Range: [OntologyElement](OntologyElement.md)

## Other properties

|  |  |  |
| --- | --- | --- |
| **Aliases:** | | node deprecation |
|  | | class obsoletion |
|  | | term obsoletion |
|  | | concept obsoletion |
| **See also:** | | [http://wiki.geneontology.org/index.php/Obsoleting_an_Existing_Ontology_Term](http://wiki.geneontology.org/index.php/Obsoleting_an_Existing_Ontology_Term) |

