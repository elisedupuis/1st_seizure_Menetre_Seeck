# The first seizure, a monocentric study


### Data dictionary

1. **database**: The data acquisition was done in two steps, this variable specifies to which of the steps the data point belongs, type character
2. **ordre**: Order in which the patients were entered in the database, type numeric
3. **code.pat**: code attributed to each patient, type character 
4. **age**: Patient's age, type numeric
5. **genre**: Patient's gender, type character
6. **atcd.enfance**: Relevant medical history of the patient during his childhood, type character
7. **atcd.famille**: Relevant medical history of the patient's close family, type character
8. **date.1st.EEG**: Date of the first standard EEG after the index event, type Date (lubridate)
9. **res.1st.EEG**: Result of the first EEG (normal, abnormal, none, none but proposed), type character
10. **pointes.1st.EEG**: Presence of epileptic spikes on the standard EEG (focal, generalised, NA), type character
11. **slow.1st.EEG**: Presence of a slowing or non-epileptic abnormalities on the standard EEG (focal, generalised, NA), type character
12. **tt.1st.EEG**: Drugs active during the standard EEG that could have reduce the spike detection (none, BZD, AED, antidepressant, neuroleptics, other, none/other, NA), type character
13. **res.lt.EEG**: Result of the first long-term EEG (normal, abnormal, none, none but proposed), type character
14. **pointes.lt.EEG**: Presence of epileptic spikes on the LT EEG (focal, generalised, NA), type character
15. **slow.lt.EEG**: Presence of a slowing or non-epileptic abnormalities on the LT EEG (focal, generalised, NA), type character
16. **tt.lt.EEG**: Drugs active during the LT EEG that could have reduce the spike detection (none, BZD, AED, antidepressant, neuroleptics, other, none/other, NA), type character
17. **normal.1st.lt.EEG**: Combination of the normality information of the standard and LT EEG, type character
18. **date.CT**: Date of the realisation of the first CT after the index event, type Date(lubridate)
19. **res.CT**: Result of the brain CT (normal, abnormal, none, none but proposed). abnromal CT contain all types of abnormalities: epileptogenic or not, type character
20. **les.CT**: Type of abnormalities (dementia, vascular, tumor, malformation, unknown, none, NA), type = character
21. **res.IRM**: Result of the brain MRI (normal, abnormal, none, none but proposed). abnromal MRI contain all types of abnormalities: epileptogenic or not, type character
22. **date.IRM**: date of the first MRI after first event, type Date (lubridate)
23.**les.IRM**: Type of abnormalities (dementia, vascular, tumor, malformation, unknown, none, NA), type = character
24. **les.epi**: Combined information of CT and MRI specifying if the lesion is epileptogenic, non-epileptogenic, suspicious, or normal
25. **date.1st.cs.su**: Date of the first consultation to the emergency department (ED) after the index event, type POSIXct
26. **date.1st.cs.epi**: Date of the first consultation in the epileptology unit of the HUG, type POSIXct
27. **dx.final**: Final diagnosis (Acute symptomatic seizure (crise provoquee), unknown, cardiovascular origin, psychogenic, other, epilepsy (crise epilepsie) vaso-vagal syncopes, cardiac origin, cardiac) retained after 2 years follow-up (for patients for whom the follow-up information was available), type character
28. **type.epi.final**: For patients with dx.final == crise epilepsie, specification of the epilepsy type (NA, non-lesional, idiopathic generalised (IGE), unknown), type character
29. **dx.final.margitta**: Correction of the diagnosis a posteriori by MS, type character
30. **cat.dx.final**: To be removed, type logical
31. **resident**: to understand why patients were lost in follow-up, infromation of where the patients are living (TRUE = Geneva's area, FALSE = other canton or country), type logical
32. **veille.sommeil**: Did the event happened during sleep or wake time, type character 
33. **status.neuro**: Results of the neuro status (normal, abnormal, none, none but proposed), type character
34. **commentaire**: Brief description of the cases in french, type character
35. **n.ret.SU**: Number of times a patient came back to the ED for a relapse, type numeric
36. **n.recidives.rapp**: Number of reported relapses in consultations, type numeric
37. **n.tot.recidives**: Number of total relapses combining reported and ED consultations, type numeric
38. **type.resident**: Description if the patient lives in another canton, country, had the first seizure while traveling..., type character
39. **SBB.1**: Number of seizures before the index event (1 = first seizure, 2 = one seizure before the index event, 3 = more than one seizure before the index event), type = numeric
40. **SBB.2**: Trajectory of the patients after the ED (1 = hospitalisation, 2 = ambulatory cares or lost, 4 = hospitalisation but with an admission in the intensive care unit before), type = numeric
41.  **SBB.3**: Trajectory of patients after the ED (1 = hospitalisation in epileptology, 2 = hospitalisation in neurology, 3 = hospitalised in the intensive care unit and lost, 4 = hospitalised in neurosurgery, 5 = hospitalised in psychiatry, 6 = hospitalised in another service, 7 = specialised ambulatory cares, 8 = followed outside the hospital or lost), type numeric
42. **SBB.4**: Long term follow-up information for patients with SBB.3 = 7 (1 = other specialised follow-up, 2 = epileptology, 3 = neurology, 4 = neurosurgery, 5 = psychatry), type = numeric
43. **SBB.5**: Trajectory of patients followed-up in epileptology 
  1. follow-up of 12 to 24 months
  2. follow-up by a private neurologist after a 3 months follow-up in the epileptology unit
  3. follow-up by the neurology service after a 3 months follow-up in the epileptology unit
  4. follow-up of 3 to 6 months in the epileptology unit and then stop because not needed
  5. follow-up of 3 to 6 months in the epileptology unit and then followed-up by a private neurologist
  6. follow-up of 6 to 12 months in the epileptology unit and then follow-up not needed anymore
  7. follow-up of 6 to 12 months in the epileptology unit and then followed-up by a private neurologist
  8. follow-up of 6 to 12 months in the epileptology unit and then followed-up by another service
  9. follow-up of 3 to 6 months in the epileptology unit and then followed-up by another service
  10. follow-up by the neurosurgery service after a 3 months follow-up in the epileptology unit
  11. follow-up by another service after a 3 months follow-up in the epileptology unit
  12. 3 months follow-up in the epileptology unit and then lost
  13. 3 months follow-up in the epileptology unit and then follow-up not needed anymore
  14. follow-up of 3 to 6 months in the epileptology unit and then patient lost 
  15. follow-up of 3 to 6 months in the epileptology unit and then follow-up not needed 
  16. follow-up of 6 to 12 months in the epileptology unit and then patient lost 
  17. follow-up of 6 to 12 months in the epileptology unit and then follow-up not needed  
  18. after a follow-up of 12 to 24 months in epileptology, follow-up scheduled
  19. after a follow-up of 12 to 24 months in epileptology, patient lost
  20. after a follow-up of 12 to 24 months in epileptology, follow-up not needed
  21. Follow-up in epileptology at 3 months and then the patient deceased
  22. Follow-up in epileptology at 3 to 6 months and then the patient deceased
  23. Follow-up in epileptology at 6 to 12 months and then the patient deceased
  24. Follow-up in epileptology at 12 to 24 months and then the patient deceased
44. **doute.critere**: Patients for whom the inclusion criteria have been discussed, type logical
45. **date.1st.1st.sz**: Date of the first event event before the index event, type Date (lubridate)
46. **date.2nd.1st.sz**: Date of an eventual second event before the index event, type POSIXct
47. **date.dern.1st.sz**: In case of more than 2 seizures before the index event, date of the last event before the index one, type POSIXct
48. **date.adm.si**: Date of hospitalisation in the intensive care unit, type POSIXct
49. **date.sortie.si**: Date of the end of hospitalisation in the intensive care unit, type Date (lubridate)
50. **date.1st.cs.neuro**: Date of the first consultation in the neurology service, type POSIXct
51. **date.dern.cs.neuro**: Date of the last consultation in the neurology service, type POSIXct
52. **raison_stop_suivi.neuro**: Motive of the interruption of follow-up by the neurology service, type character
53. **date.1st.cs.neurochir**: Date of the first consultation in the neurosurgery service, type POSIXct
54. **date.dern.cs.neurochir**: Date of the last consultation in the neurosurgery service, type POSIXct
55. **raison_stop_suivi.neurochir**: Motive of the interruption of follow-up by the neurosurgery service, type character
56. **date.1st.cs.psy**: Date of the first consultation in the psychiatry service, type POSIXct
57. **date.dern.cs.psy**: Date of the last consultation in the psychiatry service, type POSIXct
58. **raison_stop_suivi.psy**: Motive of the interruption of follow-up by the psychiatry service, type character
59. **date.1st.cs.autre**: Date of the first consultation in another service, type POSIXct
60. **date.dern.cs.autre**: Date of the last consultation in anothers ervice, type POSIXct
61. **raison_stop_suivi.autre**: Motive of the interruption of follow-up by another service, type character
62. **type_suivi.autre**: By which other service the patient was followed-up, type character
63. **date.dern.cs.epi**: Date of the last consultation in the epileptology unit, type POSIXct
64. **date.entree.1st.hospit**: Date of hospitalisation of the patient, type POSIXct
65. **srv.1st.hospit.si_autre**: If SBB.3 = 6, in which service the patient was hospitalised, type character
66. **date.debut.tt**: Date at which the anti-epileptic drug was prescribed, type POSIXct
67. **date.fin.tt**: Date of the end of treatment, type POSIXct
68. **date.dx.final**: Date at which the final diagnosis was announced to the patient, type Date (lubridate)
69. **date.deces**: Date of decease, type POSIXct
70. **cause.deces**: Origin of the death, type character
71. **date.entree.2nd.hospit**: In case of a second hospitalisation after the seizure (seizure --> emergency dept. --> hospitalisation --> 2nd hospitalisation), date of entry in the service, type POSIXct
72. **date.sortie.2nd.hospit**: In case of a second hospitalisation after the first seizure, date of release from the hospital, type POSIXct
73. **srv.2nd.hospit**: Medical service in which the second hospitalisation took place, type character
74. **type.1st.sz**: type of the first seizure (secondary generalized seizures; focals, generalized, acute symptomatic, unknown), type character
75. **type.principal.seizure**: Main type of seizure experienced by a patient, type character
76. **dx.initial**: diagnosis proposed after the first consultation, type character
77. **type.epi.initial**: Epilepsy type proposed after the first consultation, type character
78. **type.autre.initial**: For patients who recieved the diagnosis other, specification of the origin of the episode after the first consultation, type character
79. **type.autre.final**: For patients who recieved the diagnosis other, specification of the origin of the episode after 2 years follow-up, type character
80. **type.cardiovasculaire**: For the patients who recived the diagnosis of cardiovascular origin to their first event, description of the type of cardiovascular disease, type character
81. **date.sortie.1st.hospit**: Date of release after the first hospitalisation, type POSIXct
82. **review.dx**: Patients for whom the diagnosis needed a review, irrelevant column, type logical
83. **AED**: Is the patient under anti-epileptic drug ? type logical
84. **EEG.result_resume**: Summary column groupping the information of the different modalities of pointes.1st.EEG and slow.1st.EEG, type character
85. **EEG.lt.result_resume**: Summary column groupping the information of the different modalities of pointes.lt.EEG and slow.lt.EEG, type character
86. **operated**: Has the patient been operated ? type logical
87. **ATCD_specific**: Description of the medical history before the first event, type character
88. **les.progressive**: For patients who showed a brain lesion, specification if the lesion was progressive or not, type character
89. **type_EGI**: For patients with generalized epilepsy, specification of the type of generalized epilepsy, type character
90. **dx.general**: Reformulation of the column dx.final (Epileptic seizure, non-epileptic event, unknown), type character
91. **dx.event**: Reformulation of the column dx.final (Acute syptomatic seizure, Epilepsy, cardiovascular...), type character
92. **dx.epi**: Reformulation of the column dx.final and type.epi.final (focal vs. generalized), type character
  

