# Welcome to Jessica's Lab 3 Report (:

## Researching Commands

This week I will be researching some commands involved with grep. *What is grep exactly?* Grep is a powerful command-line tool in Linux that searches for text and strings in a file. The basic syntax to use grep when searching through a file is: 
`grep [command modifers] pattern [file-name]`. 
I will be demonstrating three different command-line options and three examples using it from the files and directories in `./techinical`.

## How to: Match lines that end with a specified string
The `$` symbol specifies the end of a line. You can attach `$` to the end of a string with grep to find lines that match the given pattern. This command in the terminal looks like:
`grep "string-you-are-searching-for$" file-name`

1. This is a command line input that I typed into the terminal:
~~~
grep "flights.$" technical/911report/chapter-10.txt
~~~
I am searching for sentences that end with "flights." in the Chapter 10 text file of the 911 report. This is the command line output that resulted from my input:
~~~
who left the United States on charter flights.
links to terrorism departed on these flights.
~~~
The output consists of two lines in the Chapter 10 text file that end with "flights.". By inputting the grep command, I can quickly see what flights were involved in this chapter. That said, I believe this may not be the most optimal command to do so because it doesn't search for all the mentions of "flight" in the file; it just looks at the last few strings in a line.

2. This is a second command line input that I typed into the terminal:
~~~
grep "Agency.$" technical/911report/chapter-13.1.txt
~~~
I am searching for sentences that end with ".Agency." in the Chapter 13.1 text file of the 911 report. This is the command line output that resulted from my input:
~~~
the National Security Agency.
agencies housed within the Department of Defense: the National Security Agency,
~~~
The output consists of two lines in the Chapter 13.1 text file that end with "Agency.". By inputting the grep command, I can quickly see what Agencies were mentioned in this chapter. Again, I believe this is not an optimal command to do so, but it succeeds its purpose to find a sentence that matches the string I want to find at the end of a line. 

3. This is a third command line input that I typed into the terminal:
~~~
grep "San Diego.$" technical/911report/chapter-7.txt
~~~
I am searching for sentences that end with ".San Diego." in the Chapter 7 text file of the 911 report. This is the command line output that resulted from my input:
~~~
earlier, he joined Nawaf al Hazmi in San Diego.
~~~
The output consists of one line in the Chapter 7 text file that ends with "San Diego.". By inputting the grep command, I can quickly see if the San Diego location was mentioned in this chapter. My opinion regarding the use of this command still stands.

## How to: Check for whole words and their line in a file
The `w` letter specifies a whole word. You can write `w` before the string you want to find with grep to find lines that match the given pattern. The outplay will display the whole line (not sentence) that the word is in. This command in the terminal looks like:
`grep -w "string-you-are-searching-for" file-name`

1. This is a command line input that I typed into the terminal:
~~~
grep -w "law enforcement" technical/911report/chapter-3.txt
~~~
I am searching for any appearance of the words "law enforcement" in the Chapter 3 text file of the 911 report. This is the command line output that resulted from my input:
~~~
        that the law enforcement system was well-equipped to cope with terrorism. Neither attacks).10 The law enforcement process is concerned with proving the guilt of thus begins with the nation's vast complex of law enforcement agencies.
The Justice Department and the FBI At the federal level, much law enforcement The chief vehicle for INS and for state and local participation in law enforcement Other federal law enforcement resources, also not seriously enlisted for 
        sprawling U.S. law enforcement community was engaged in countering terrorism. Moreover, law enforcement could be effective only after specific individuals were demands, get the plane to land safely, and then let law enforcement or the military 
As for law enforcement, there were only 33 armed and trained federal air marshals as 
        specifically accorded "no police, subpoena, or law enforcement powers or internal parts of the federal bureaucracy, particularly the law enforcement and intelligence problem, not just a law enforcement issue. They reinforced the authority of the
~~~
The output consists of multiple lines in the Chapter 3 text file that mentions the word "law enforcement". The lines are listed in subsequential order in which they appear in the file (lines 1, 2, 3...). The output also shows a distinction between the beginning and middle of a paragraph. For instance, if "law enforcement" appears in the first line of a paragraph, it will not be indented; if the word appears in the middle of the paragraph, it will be indented. By inputting the grep command, I can easily get an idea of how law enforcements were involved in this chapter.

2. This is a second command line input that I typed into the terminal:
~~~
grep -w "effects" technical/biomed/1468-6708-3-4.txt
~~~
I am searching for any appearance of the word "effects" in the 1468-6708-3-4 text file of the biomed file. This is the command line output that resulted from my input:
~~~
        withdrawal for symptomatic adverse effects 2) lack of
        To demonstrate with simple algebra the effects and key
        withdrew early because of adverse effects, lack of response
        effective control of BP and no side effects.' Obviously,
        protocol with effective control of BP and no side effects,
        effects with the study therapies at Month 6 ('responders'
        response and some because of side effects, but the paper
        effective control of BP and no side effects' (as explained
        BP without side effects with the study therapies at Month
        effects, then the calculation in (a) would be appropriate.
        response' and 'side effects', a better estimate could be
        treatment effects will be less biased. Since PI does less
        side effects without affecting the efficacy of the study
~~~
The output consists of multiple lines in the 1468-6708-3-4 text file that mentions the word "effects". Again, the lines are listed in subsequential order and since no lines are indented, I know that all the mentions of the word "effects" is in the middle of a paragraph. By inputting the grep command, I can easily get an idea of what treatment effects were involved in the experiments mentioned in this file.

3. This is a third command line input that I typed into the terminal:
~~~
grep -w "protein" technical/biomed/1471-2091-3-22.txt
~~~
I am searching for any appearance of the word "protein" in the 1471-2091-3-22.txt file of the biomed file. This is the command line output that resulted from my input:
~~~
transfers ubiquitin to the target protein. E3 enzymes are
        protein Hrt1p/Rbx1p/Roc1p, the adapter protein Skp1p, and
        Cdc53p/CUL1-related protein, was shown to associate with
        pip1 (pop interacting protein 1),
        with Pop1p and Pop2p, protein lysate was prepared from
        F-box protein dependency of this reaction (Fig. 2D, lane
        protein (GFP) at low levels from an inducible pRep81
        Rum1p protein stability in wild-type and 
        heterodimerizing F-box protein partners does not rule out
        The phenomenon of F-box protein oligomerization is not
        yeast F-box protein Met30p was recently shown to regulate
        The idea developed above that F-box protein
        by binding to protein A.
        Immunocomplexes were collected by binding to protein A or
        SCF: SKP1/CUL1/F-box protein
~~~
The output consists of multiple lines in the 1471-2091-3-22 text file that mentions the word "protein". There is one line indented which tells me that that line is the first sentence in a paragraph; the rest are in the middle. By inputting the grep command, I can easily get an idea of what proteins were involved in the research mentioned in this file.

## How to: Check n lines before, after (or both) from a string in file
The `A` letter followed by n number reveals a searched string and n lines after that result. You can write `A[number]` before the string you want to find with grep to find lines that match the given pattern and a certain number of liens after it. This command in the terminal looks like:
`grep -A[numer] "string-you-are-searching-for" file-name`. You can use the same syntax but with the `B` letter to reveal the searched string and n lines before the result. You can use the `C` letter to reveal the searched string and n lines before AND after the result. I will only be going over the letter `A`.

1. This is a command line input that I typed into the terminal:
~~~
grep -A1 rationale technical/government/Alcohol_Problems/Session3-PDF.txt
~~~
I am searching for lines with the word "rationale" in it and ONE line after in the Session 3 PDF text file of the Alcohol Problems report in the government file. This is the command line output that resulted from my input:
~~~
examine the rationale for intervening, types of interventions and
interveners, and barriers and concerns that need to be addressed.
--
The rationale for interventions in the emergency setting is that
the medical condition or injury prompting admission provides a
~~~
The output consists of four lines - there are two lines that mention "rationale" in the Session 3 PDF text file and is one other line printed beneath each of these two lines (this is the ONE line that follows the line that mentions "rationale"). Each of these two sections are separated by two dashes which make it easier for users to see which line is associated with what. By inputting the grep command, I can get an idea of what the rationale was in this text with more context. If I wanted to get even more context, I can increase the number after the letter `A` to see more lines that proceed the line that mentions "rationale".'

2. This is a second command line input that I typed into the terminal:
~~~
grep -A2 abuse technical/government/Alcohol_Problems/Session3-PDF.txt
~~~
I am searching for lines with the word "abuse" in it and TWO lines after in the Session 3 PDF text file of the Alcohol Problems report in the government file. This is the command line output that resulted from my input:
~~~
and his or her drinking or drug abuse and may be more motivated to
change.13-15
* Presenter
--
of a substance abuse counselor mobilizing the family, and at times
the employer, to intervene with the patient's drinking and to
arrange for immediate entry to a residential substance abuse
treatment program after discharge. This program appeared to be
successful in getting problem-drinking patients to treatment, but
--
examined the outcomes achieved by substance abuse counselors or
alcohol workers intervening with problem drinkers. A brief
intervention in an emergency department by alcohol health workers
--
agreed to be in the program.21 A substance abuse consultation team
in a trauma center reported acceptance of referral for drug or
alcohol treatment in 62% of the 100 consecutive cases
--
specialists trained in alcohol or substance abuse counseling or in
motivational interviewing techniques. These interventionists met
with the patient, discussed drinking and substance use openly and
--
directly, and offered some advice and assistance. Substance abuse
counselors typically offered advice and referrals to treatment
facilities or self-help programs. Motivational interview counselors
--
avoid alcohol-related injuries in the future. Substance abuse
specialists of one type or another typically delivered drinking
interventions in emergency settings with a few exceptions.29,30 No
--
substance abuse interventions focus on motivation to enter
treatment because the patients are severely dependent, heavy
drinkers. Referral to "appropriate" treatment is the critical end
--
substance abuse counselors, only 5% used screening questionnaires
to identify patients with alcohol use problems.
Although we know of no studies assessing clinical practices
--
abuse/dependence is a "treatable disease," but more than 90%
indicated that there was a lack of time to perform interventions,
and only 51% supported
--
substance abuse counselors. However, it may be more a matter of
skill and ability to work in this setting and deliver the needed
type of intervention rather than of profession that should
--
been published that deal with alcohol dependence and abuse and
emergency medicine. The challenge now is to discover how government
agencies and professional organizations can promote adoption and
--
abuse/dependence in motor vehicle crash victims presenting to the
emergency department. Acad Emerg Med 1997;4:256-62.
5. Whiteman PJ, Hoffman RS, Goldfrank LR. Alcoholism in the
--
alcohol abuse in trauma patients. Arch Surg 1993;128:907-13.
7. Soderstrom CA, Smith GS, Dischinger PC, McDuff DR, Hebel JR,
Gorelick DA, et al. Psychoactive substance use disorders among
--
alcohol-related injuries. Substance abuse interventions in general
nursing practice. Nurs Clin North Am 1998;33(1):93-104
14. Longabaugh R, Minugh A, Nirenberg TD, Clifford PR, Becker
--
substance abuse.
Psychological Science 1999;10(3):209-13.

--
22. El-Guebaly N, Armstrong SJ, Hodgkins DC. Substance abuse
and the
emergency room: programmatic implications. J Addict Dis
--
abuse consultation team in a trauma center. J Stud Alcohol
1995;56:267-71.

--
preventive services, and the substance abuse treatment system. Ann
Emerg Med 1997;30(2):181-9.
30. Hungerford DW, Pollock DA, Todd KH. Acceptability of
--
attitudes concerning intervention for alcohol abuse/dependence in
the emergency department. J Addict Dis 2000;19:45-53.
44. Friedman PD, McCullough D, Chin MH, Saitz R. Screening and
--
services, and the substance abuse treatment system. Ann Emerg Med
1997;30:181-9.
6. Rhodes KV, Lauderdale DS, Stocking CB, Howes DS, Roizen MF,
--
clinicians in screening and brief intervention for substance abuse
problems: translating evidence into practice. J Subst Abuse
2000;21:21-31.
--
to alcohol misuse and abuse.
Patients in the emergency setting range from those with no
alcohol problems to those with severe dependence. In the next few
--
alcohol-related injuries. Substance abuse interventions in general
nursing practice. Nurs Clin North Am 1998;33(1):93-104.
9. Longabough R, Minugh PA, Nirenberg TD, Clifford PR, Becker
--
care, but of many systems. Her work has been in substance abuse
prevention in schools, where she encountered many social and legal
beliefs that ran counter to her prevention education efforts. She
~~~
The output consists of many lines that mention "abuse" in the Session 3 PDF text file and there are two other lines printed beneath each of these two lines (these are the TWO lines that follows the line that mentions "abuse"). Something interesting that came up with my input was that one section printed five lines instead of three. I realized this was because within the two lines that was printed after the line with the word "abuse" in it, another line with the word "abuse" came up, so two MORE lines that came after it were printed. By inputting the grep command, I can get a solid idea of what abuse was involved in this text with sufficient context.

3. This is a third command line input that I typed into the terminal:
~~~
grep -A5 awareness technical/government/Alcohol_Problems/Session3-PDF.txt 
~~~
I am searching for lines with the word "awareness" in it and FIVE lines after in the Session 3 PDF text file of the Alcohol Problems report in the government file. This is the command line output that resulted from my input:
~~~
Whether this awareness is viewed as a "hitting bottom"
phenomenon or in more traditional motivational terms, there does
seem to be a connection between readiness to change and recognition
that negative consequences can be directly linked to a behavior.17
Reports from emergency staff and anecdotal descriptions of some
interventions support the results of the above studies, indicating
~~~
The output consists of one line that mentions "awareness" in the Session 3 PDF text file and there are five other lines printed beneath it (these are the FIVE lines that follows the line that mentions "abuse"). The word "awareness" was only mentioned once in this file. By inputting the grep command, I can very quickly get an idea of what awareness there was regarding the study with neccessary context. 

# The End (Thank you for reading my Lab 3 Report!)