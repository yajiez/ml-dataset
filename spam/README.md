# SPAM E-mail Database

## Sources

- Source: UCI Machine Learning Repository http://www.ics.uci.edu/~mlearn/MLRepository.html

- Creators: Mark Hopkins, Erik Reeber, George Forman, Jaap Suermondt Hewlett-Packard Labs, 1501 Page Mill Rd., Palo Alto, CA 94304
- Donor: George Forman (gforman at nospam hpl.hp.com)  650-857-7835
- Generated: June-July 1999

## Past Usage

- Hewlett-Packard Internal-only Technical Report. External forthcoming.

- Determine whether a given email is spam or not.

- ~7% misclassification error. 

  False positives (marking good mail as spam) are very undesirable. If we insist on zero false positives in the training/testing set, 20-25% of the spam passed through the filter.

  
## Relevant Information

The "spam" concept is diverse: advertisements for products/websites, make money fast schemes, chain letters, pornography...

Our collection of spam e-mails came from our postmaster and individuals who had filed spam.  Our collection of non-spam e-mails came from filed work and personal e-mails, and hence the word 'george' and the area code '650' are indicators of non-spam.  These are useful when constructing a personalized spam filter.  One would either have to blind such non-spam indicators or get a very wide collection of non-spam to generate a general purpose spam filter.

- For background on spam: Cranor, Lorrie F., LaMacchia, Brian A.  Spam! Communications of the ACM, 41(8):74-83, 1998.

- Number of Instances: 4601 (1813 Spam = 39.4%)

- Number of Attributes: 58 (57 continuous, 1 nominal class label)

## Attribute Information

The last column of 'spambase.data' denotes whether the e-mail was considered spam (1) or not (0), i.e. unsolicited commercial e-mail.  Most of the attributes indicate whether a particular word or character was frequently occuring in the e-mail.  The run-length attributes (55-57) measure the length of sequences of consecutive capital letters.  For the statistical measures of each attribute, see the end of this file.  

Here are the definitions of the attributes:

- 48 continuous real [0,100] attributes of type `word_freq_WORD` = percentage of words in the e-mail that match WORD,
  i.e. 100 * (number of times the WORD appears in the e-mail) / total number of words in e-mail.  A "word" in this case is any 
  string of alphanumeric characters bounded by non-alphanumeric characters or end-of-string.

- 6 continuous real [0,100] attributes of type `char_freq_CHAR` = percentage of characters in the e-mail that match CHAR,
  i.e. 100 * (number of CHAR occurences) / total characters in e-mail
- 1 continuous real [1,...] attribute of type `capital_run_length_average` = average length of uninterrupted sequences of capital letters
- 1 continuous integer [1,...] attribute of type `capital_run_length_longest` = length of longest uninterrupted sequence of capital letters
- 1 continuous integer [1,...] attribute of type `capital_run_length_total` = sum of length of uninterrupted sequences of capital letters = total number of capital letters in the e-mail
- 1 nominal {0,1} class attribute of type spam = denotes whether the e-mail was considered spam (1) or not (0),  i.e. unsolicited commercial e-mail.  

## Missing Attribute Values

None

## Class Distribution

Spam: 		1813  (39.4%)
Non-Spam: 2788  (60.6%)
