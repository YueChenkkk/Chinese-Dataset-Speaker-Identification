# Chinese-Dataset-Speaker-Identification
This is a Chinese dataset for speaker identification in novels. It's built on the Chinese novel *World of Plainness*.

This dataset was first released by Jiaxiang Chen in his paper "A Chinese Dataset for Identifying Speakers in Novels" on Interspeech 2019. We added a bit more annotations and released the refined version here.

## Content
The data has been divided into training set, development set and test set, containing 2000, 298 and 298 instances respectively. The subsets are saved in 3 different directories dataset/train, dataset/dev and dataset/test.

Each subset is further divided into 3 sub-categories *explicit*, *implicit* and *latent*, as mentioned in Chen's paper. Instances of different categories are saved in separate files. \*\*\*_unsplit.txt keeps all the instances in the three categories combined. The number of instances in each category is listed in the table. 

|     |*Explicit*|*Implicit*|*Latent*| Total |
|-----|:-----:   |:-----:   |:----:  |:-------:|
|Train|  393     |  220     |  1387  |  2000  |
|Dev  |  44      |  31      |  223   |  298   |
|Test |  44      |  29      |  225   |  298   |

Besides, the name list and speech verb set are also provided. The speech verb set is used for the categorization mentioned above.

## Data Format
In each data file, instances are seperated by a blank line. The first line indicates the index of the instance in the file. The following 21 lines are the continuous sentences for speaker identification, which were extracted from the novel. Among them the 11th sentence is the center quote whose speaker needs to be identified. The following two lines are the name of the true speaker of the center quote, along with the index of the true speaker in the name list (line index in name_list.txt). The last line indicates the category of the instance (one of explicit/implicit/latent).

In name_list.txt, each line lists the aliases of a novel character. The binary number 0/1 in front of the aliases is the gender information of that character, 0 for female and 1 for male.
