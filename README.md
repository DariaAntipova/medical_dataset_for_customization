# medical_dataset_for_customization

The task is to compile a disease-representative dataset for training a large language model on medicine based on translation detalizations of specific clients. To accomplish this task, I decided to compile a list of drugs mentioned in clients' translations, indicating their trade name, international nonproprietary name, diseases to treat, and the group of diseases to which they belong. Thus it is possible to select segments where drug names occur and collect statistics on which diseases or disease groups prevail in the translation detalizations and collect a list of representative orders whose translations can be used for customization.

Input: an excel-file of translation segments with customer and order numbers for each segment.
Output: 

The following steps were needed to accomplish the task:
1) Selecting a python library to retrieve medical entities, among which will be trade names of drugs. Retrieving medical entities.
2) By means of GPT, selecting trade names of drugs from the list of medical entities and specifying their international nonproprietary names, diseases to treat, and the group of diseases to which they belong.
3) From the translation detalizations, selecting segments where either the trade name of the drug or the international nonproprietary name occurs, and for each segment add columns with the trade name, the international nonproprietary of the drug and the group of diseases. Obtaining statistics on which groups prevail and the order numbers where they are mentioned.
