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
`grep -A[number] "string-you-are-searching-for" file-name`. You can use the same syntax but with the `B` letter to reveal the searched string and n lines before the result. You can use the `C` letter to reveal the searched string and n lines before AND after the result. I will only be going over the letter `A`.

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
The output consists of four lines - there are two lines that mention "rationale" in the Session 3 PDF text file and there is one other line printed beneath each of these two lines (this is the ONE line that follows the line that mentions "rationale"). Each of these two sections are separated by two dashes which make it easier for users to see which line is associated with what. By inputting the grep command, I can get an idea of what the rationale was in this text with more context. If I wanted to get even more context, I can increase the number after the letter `A` to see more lines that proceed the line that mentions "rationale".'

2. This is a second command line input that I typed into the terminal:
~~~
grep -A2 studies technical/government/Alcohol_Problems/Session3-PDF.txt
~~~
I am searching for lines with the word "studies" in it and TWO lines after in the Session 3 PDF text file of the Alcohol Problems report in the government file. This is the command line output that resulted from my input:
~~~
to emergency departments and trauma centers. Many studies have
documented the presence of alcohol among patients admitted to
emergency depart-ment1-5 and trauma center6,7 settings. Other
--
studies have demonstrated that even blood alcohol concentration
(BAC) determinations under-estimate the extent of alcohol problems
among the patients who are triaged and treated in emergency
--
studies and a few controlled trials indicate that interventions
focused on patients' drinking can reduce the amount of drinking as
well as injury episodes, including repeat re-admission for injury
--
interventions support the results of the above studies, indicating
heightened motivation in the initial period of time in the
emergency setting. However, it is not clear how long this initial
--
drinkers after their visit to an emergency setting. Several studies
have documented consumption changes not only in the intervention
condition but also in the minimal intervention control groups.18,19
--
resources or insurance.21 This and other seminal studies encouraged
many professionals to call for some type of consultation service or
brief intervention to be employed with patients in emergency rooms
--
Many of the early studies that documented the efficacy of
interventions with problem drinkers in emergency settings were
evaluations and not controlled studies. Nevertheless, the
documented outcomes have been impressive. Several studies have
examined the outcomes achieved by substance abuse counselors or
alcohol workers intervening with problem drinkers. A brief
--
colleagues identified 19 studies that measured injury outcomes
among participants in a variety of settings. They reported that
reductions in a variety of injuries, injury hospitalizations, and
--
individuals who had legal charges pending. Most of the studies
reviewed were not well controlled and the numbers of participants
and effect sizes reported in these studies were modest.
Until recently, no well-controlled intervention studies have
addressed whether interventions in emergency settings would reduce
alcohol consumption and consequences. Several current publications
--
studies have compared different types of intervention providers in
these settings.
In contrast, physicians or nurses in a variety of primary care
--
alcohol intervention.9,26,35,36 However, few studies of
physician-delivered interventions in an emergency setting exist.
Clearly, none of the extant studies could be done without the
support and involvement of emergency medicine physicians and trauma
surgeons. However, it may be difficult to get physicians to deliver
--
studies that have demonstrated effects either with volunteer or
randomized participants is modest but increasing, and the effects
range from minimal to very sizeable reduction in risks that have
--
large in some studies. However, when the intervention was delivered
to patients in emergency settings and compared with standard or
minimal interventions, intervention patients had significantly
--
Although we know of no studies assessing clinical practices
regarding alcohol problems in emergency departments, a survey of
1,055 emergency medicine physicians by Chang and colleagues found
--
effectiveness studies. Feasibility and successful dissemination
must be demonstrated. Prototype interventions that can reach the
majority of problem drinkers, motivate them to change drinking
--
effectiveness studies can then be used to promote change in
standard practice in all emergency settings.
What we have learned from the research to date gives us some
--
studies indicate that facilitating the referral and making the
connections increase compliance, the intervention ideally should
have a component of compliance enhancement if it includes referral
--
evaluation studies, and policy and procedure evaluations are needed
to resolve the issues outlined previously. Twenty years ago, Joseph
Zuska, a surgeon with an interest in alcohol problems among injured
--
39 studies (30 randomized controlled and 9 cohort) with a positive
effect demonstrated in 32 of these studies.1 We also know that the
ED visit offers a potential "teachable moment" due to the possible
negative consequences surrounding it and that in essence we, as
--
All of these questions need to be answered in future studies if
we are to prove that SBI is effective in the ED setting. It is
crucial that researchers are clear on all aspects of their research
--
are endless, allowing for multiple studies and a great deal of
creativity on the part of the researchers.
References
--
studies. In addition, the target of the intervention (at-risk
drinkers, problem drinkers, alcohol-dependent drinkers) and the
mechanism of intervention (physician, nursing staff, social
--
(effect sizes of ~30% to 40%). The intervention studies based on
provider feedback and advice to the patient have had mixed results
in the ED. In addition, it remains difficult to engage health care
--
In addition, because of the effect sizes shown by the studies to
date, there is also a need to target responses and elements of the
brief intervention to the problems specific to each individual
--
Kristen Barry noted that in primary care studies, one session
seems to be enough to foster change. However, she found it
interesting that booster sessions worked in this setting. Even
--
will see if other studies confirm that.
Herman Diesenhaus added that there must be some type of
maintenance activity if we are dealing with a chronic, relapsing
--
describes how studies at Brown evaluate fidelity. He also noted
that none of the three clinical trials (Gentillelo's with trauma
patients, his own with adolescents, and Longabaugh's in the ED)
--
his studies, he remarked that it is irresponsible for interventions
not to focus on drinking as well as harm.
Gail D'Onofrio noted that her planned study will use physicians,
--
important. She noted that research studies often attempt to control
so many variables and follow up with patients so frequently that
control groups receive so much attention focused on alcohol that it
--
in studies. This can make it difficult to standardize
interventions. She hypothesized that under-standing the patient's
perception of the interventionist's capabilities might be as
--
smaller, targeted research studies could address that question. He
cautioned that not every study has to be a clinical trial focused
on outcomes. To examine the issue of gender, patients could be
--
studies or pooling of control group data might better identify
predictors. More data on this issue could help us plan better
controlled trials-who to target, when to follow up, and when to
--
more smoothly. He noted that most brief intervention studies in EDs
have focused on injured patients, but that 70% to 80% of ED
patients do not present with an injury. He wondered how much of
--
non-injured patients. She noted that primary care studies and Ed
Bernstein's ED project do give us experience with non-injured
patients.
--
most primary care studies involve non-injured patients. He thought
their findings help support work with non-injured patients in the
emergency department setting as well.
--
believed studies from England and New Zealand should be viewed very
critically because access to health care is easier than in the
United States. He believed that
--
studies in American emergency settings have provided
inconclusive evidence that brief intervention works. He cautioned
that literature reviews generally do not include all relevant
--
studies because studies with negative results are seldom
published.
DiClemente agreed that efficacy in the ED setting had not been
--
efficacy or effectiveness studies behind them are adopted and
become guidelines for standard practice. Once that happens, it is
very difficult to get support to re-evaluate them, so it is true we
~~~
The output consists of many lines that mention "studies" in the Session 3 PDF text file and there are two other lines printed beneath each of these two lines (these are the TWO lines that follows the line that mentions "abuse"). Something interesting that came up with my input was that some sections printed five or six lines instead of three. I realized this was because within the two lines that were printed after the line with the word "studies" in it, another line with the word "studies" came up, so another lines that came after it were printed; This continued if more lines with the word "studies" came up. It is good to note that these additional lines typically increment by the number n (2 in this case). However, it is two lines before the last line that has the word ("studies" in this case). If Lines 1, 3, and 4 have the word "studies" in it, there will be six lines because there should be two additional lines printed after line 4. By inputting the grep command, I can get a solid idea of what studies were involved in this text with sufficient context.

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