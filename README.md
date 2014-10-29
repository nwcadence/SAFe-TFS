SAFe-TFS
========
This is a process template for Microsoft's Team Foundation Server designed to support organizations that are rolling out the Scaled Agile Framework (SAFe).

Currently we're in open-beta, please feel free to download and use the process template! For more information on the Scaled Agile Framework go to http://scaledagileframework.com.

*************** Release 3.0.0 ***********************

Major purpose of release: Finish customizing the fields and each work item type and make changes necessary to align with SAFe 3.0

Notes:
  -  Changed number version system so that our major version number (3) aligns with the Scaled Agile Framework's major version number.
  -  Updated all work item fields to reflect SAFe 3.0
  -  Updated State Flow for Epics to align with suggested states for epics in SAFe (both Business and Architectural Epics)
  -  Renamed Investment Theme to Strategic Theme
  -  Add "New" state to bug to resolve Kanban board issues and align with other work items in the requirements category

#Differences between SAFe-TFS and the Microsoft Guidance on SAFe#

Microsoft provides guidance on using TFS to support SAFe in a a whitepaper located at http://msdn.microsoft.com/en-us/library/dn798712.aspx. the approach taken here and approach taken by Microsoft are somewhat similar. The Microsoft guidance generally minimizes the changes needed to a process template to support SAFe, and can be used more easily with existing team projects.  The SAFe-TFS project, on the other hand, makes extensive use of custom work items types that map very closely to the SAFe 3.0 nomenclature. Additionally, there are aditional fields to support SAFe, mostly around estimation and WSJF prioritization.

#Answers to a few common design questions:#

Why separate ArchitecturalEpic and BusinessEpic work items? Why not Epic with a switch for Architecture / Business? 

>>Using two separate work item types allows color coordination and easy viewing on the backlog. It does however make querying more difficult, as you need to remember to use the category, or both types if you want to see all features. Separate work items also leave room for fields that may be specific to each work item in the future, as SAFe continues to evolve. 

Why separate User Story, Spike, Refactor work items? Why not a PBI with a switch?

>>Pretty much the same logic applies here, as above, with the addition that I wanted to follow the SAFe guidance on work item types as closely as possible. Reference here: http://scaledagileframework.com/agile-software-requirements-model/

Do you really need extra fields and meta data around Theme? Why not use a Tag?

>>While it would be possible to use Tags for Themes and store the documentation for the meta-data somewhere else (SharePoint or wherever), we wanted to provide the ability to manage your entire SAFe roll-out across multiple ARTs in a single instance of TFS. 
