This project is an attempt to support the OMG Unified Architecture Framework (UAF) [1] in the Eclipse Papyrus modeling tool environment [2].

This projecty contains

* UAF.profile. A UML-profile of UAF to be used in Papyrus. The profile is based on the OMG UAF profile. See adjustments below
* UAF.css A stylesheet to provide UAF coloring schemes to Papyrus diagrams
* UAF to UML mappings.xlsx an overview of which metaclasses each UAF stereotype extends

 
The OMG UAF UML profile has been migrated to Papyrus with the following adjustments:

* References to OMG SysML 1.6 profile has been changed to the Papyrus SysML 1.6 profile provided in the Papyrus SysML 1.6 extension.

* References to primitive types has been changed to references to UML2 primitive types

* Spaces in package names have  been removed because Papyrus seems to have problem applying stereotypes defined within a profile package with spaces in its name. 

* The "viewpoint" property of the <<UAF::Summary and Overview::View>> stereotype has been removed as it conflicts with a property with identical name in the inherited <<SysML::ModelELements::View>> stereotype

* The "concern" and "method" properties of the <<UAF::Summary and Overview::ViewPoint>> have been removed as they conflicts with properties with identical names in the <<SysML::ModelELements::ViewPoint>> stereotype.

* The upper limit of the "endDate" property of the <<UAF::Projects::Roadmap::ActualProjectMilestone>> stereotype has been changed from 0 to 1.

* The multiplicity of all properties referring to UML meta classes (base_XXX) have been changed from 1 to 0..1.


To be able to use the profile, the SysML 1.6 extension to Papyrus must be installed


References:
[1] OMG Unified Architecture Framework (UAF)
    https://www.omg.org/uaf/

[2] Eclipse Papyrus modeling tool environment
    https://www.eclipse.org/papyrus 
    
[3] SysML 1.6 extension for Eclipse Papyrus
    https://marketplace.eclipse.org/content/papyrus-sysml-16