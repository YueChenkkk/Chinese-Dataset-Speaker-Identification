# Chinese-Dataset-Speaker-Identification
This is a Chinese dataset for speaker identification in novels. It's built on the Chinese novel *World of Plainness*.
This dataset was first released by Jiaxiang Chen in his paper "A Chinese Dataset for Identifying Speakers in Novels" on Interspeech 2019. 

## Content
The data has been divided into training set, development set and test set, containing 2000, 298 and 298 instances respectively. The subsets are saved in 3 different directories dataset/train, dataset/dev and dataset/test.

Each subset is further divided into 3 sub-categories *explicit*, *implicit* and *latent*, as mentioned in Chen's paper. Instances of different categories are saved in seperate files. xxx_unsplit.txt keeps all the instances in the three categories combined. The number of instances in each category is listed in the table. 

|     |*explicit*|*Implicit*|*Latent*|
|-----|------:   | -----:   | ----:  |
|Train|  393     |  220     |  1387  |
|Dev  |  44      |  31      |  223   |
|Test |  44      |  29      |  225   |

Besides, the name list and speech verb set is also provided. The speech verb set is used for the categorization mentioned aboved.

## Format
In each data file, instances are seperated by a blank line. Each instance have 24 lines. The first line indicates the index of the instance in the file. The following 21 lines is the textual segment for speaker identification, which is extracted from the novel. The 11th sentence is the center quote whose speaker needs to be identified. The following two lines are the name of the true speaker of the center quote, and the index of the true speaker in the name list (line index in name_list.txt).

In name_list.txt, each line lists the aliases of a novel character. The binary number 0/1 in front of the aliases is the gender information of that character, 0 for female and 1 for male.
