# 2019-nCoVdata

Argonne is leading and coordinating five related computational efforts aimed at improving our
understanding of the SARS-nCoV-2 virus, the associated COVID-19 disease, and accelerating
the development of treatment options including antiviral drugs and vaccines.   This
computational effort complements the experimental laboratory efforts at Argonne and elsewhere.
The overall effort includes team members from multiple laboratories (Argonne and Brookhaven)
multiple universities (University of Chicago, University of Illinois, University of Virginia,
Rutgers University and George Mason University) and private research centers (JC Venter Institute).   

As of Thursday March 5th, there were 57 researchers involved in the effort coordinating their
work online via real-time messaging, conferencing, email and file sharing.
Argonne’s ALCF has made special queues available on the ALCF machines for the research
groups to gain rapid access to needed computing and Argonne and Brookhaven have also
identified additional computing resources for the team’s use.  These activities are
combining bioinformatics analysis, simulation and machine learning and are building a
local collection of relevant datasets.  In addition, Argonne is making time on our
computers available to any research group that needs significant computing for coronavirus work.


The five lines of attack include:

## Computational Drug Screening
Aims to accelerate the development of antiviral drugs. In this effort we are modeling proteins that play critical roles in the virus life cycle and selecting those for drug targets. We are screening three collections of drug candidates on these targets for inhibitor activity, 1) known and licensed drugs for quick repurposing opportunities (e.g. DrugBank), 2) library of 250M known small molecules that are drug like (e.g. PubChem) and 3) large-scale libraries (e.g. Enamine, ZINC) with billions of compounds that could be manufactured quickly for testing.  Our primary targets are existing drugs that could be repurposed quickly and that already are in the manufacturing pipelines.  Preliminary results are already being produced and will be made available to community wet labs in the coming days for additional testing and screening.

## Epitope Analysis
Aims to support vaccine development.  Vaccines work by exposing the immune system to molecules associated with the infectious agent in advance so the immune system can quickly recognize and ramp up when presented with a known challenge.  These molecules that stimulate the immune system are called antigens.  Epitope analysis is used to analyze the genome of the virus to identify candidate protein sequences that can serve as antigens to attempt to confer immunity without causing disease or runaway inflammation.  Determining the components and sub-sequences of the virus proteins that can serve this role requires analysis of previous antigens, virus evolution and human immune response.  Our goal in this effort is to expand the set of epitopes that could serve this role and make those available to the community for further testing and development.

## Host Response Analysis
Aims to identify additional drug targets in the host and to build models to attempt to predict which patients are likely to be at high risk.  The virus interacts with dozens of proteins in the human host, to initially enter the cell and later to suppress the cell’s defenses and to harness the cell’s machinery for replication.   Human proteins that interact with the virus are potential therapeutic targets.  The idea is to block those interactions via a drug and therefore slow down or stop the virus lifecycle. Host response analysis also tries to identify the specific mutations or cellular states of the host that determine the severity of infection.  This work involves building human protein interaction maps as well as studying data from other types of virus infections to identify key response signatures for SARS-CoV-2 that might be useful in predicting outcomes.  This effort feeds targets to the drug screening effort as well as supports model building to predict patient risk/outcome.

## Computational Epidemiology 
Aims to model the spread of the virus and the impact a pandemic could have on critical social services (police, fire, healthcare, etc.) in communities, regions and countries.  We are scaling agent-based models (which have been successfully used for many years for modelling Ebola, Zika and other outbreaks) to model the behavior of large-scale populations at the individual level to test models of infection, transmission, disease, outcome and recovery.  These models can account for person to person contact, flows of people to/from work, school, shopping etc.  Using the DOE supercomputers, we can model entire cities with millions of individuals and test hypotheses/polices for reducing rates of transmission as well as understanding the impact of loss of staffing for critical services.

## Virus Evolutionary Analysis
Aims to better understand the origin and structure of the virus genome, the types of selection pressure the virus is under and the structure of sub-clades of the virus and the impact of mutations on virulence, infectivity, survival and transmission.  This project supports the other four activities by giving us a deeper understanding of the SARS-CoV-2 virus in the context of other coronaviruses.  Key questions are which animal hosts are the main natural reservoir for the virus, when did it cross from animal to human, is it adapting to human host and what are the likely future changes in the virus.


All of these efforts build on the staff experience and infrastructure developed over many years by the long-standing federal investments in bioinformatics and computational biology programs supported by DOE-ASCR, DOE-BER (e.g. KBase) and NIH-NIAID (e.g. BV-BRC Center at UC/JCVI), the more recent efforts in Cancer supported by the DOE/NCI joint project (JDACS4C) including the DOE ECP CANDLE project and the DOE ALCF early science program.

