# General Details
- Authors: Tibor Kiss, Alicia Katharina Börner, Jutta Pieper
- Affiliation: Linguistic Data Science Lab (LDSL), Ruhr-Universität Bochum, Germany
- Publication: Word order constraints on event-internal modifiers
- Date: 08.03.2023
- Abstract: 
> In this study, we have tested object-oriented comitative PPs (COM(O)), and subject-oriented instrumental PPs (INSTR) to the left and to the right of an object, which was realized either as a wh-indefinite or a regular NP (with an indefinite determiner). We predict that the two adverbials differ in their positional behavior. The reason is the orientation of the adverbials: object-related PPs should be realized below the object, while a realization of subject-related PPs could be possible at any position below the subject, including a position between the subject and the object. This hypothesis differs from Frey & Pittner’s (1998), who assume that COM(O) should be found to the right of the object, but INSTR to the immediate right of the subject. 


# Study Details
- Study Title: ExPrep Exp 2 (Instrumentals vs. Comitatives, wh-indefinite vs. NP)
- Date (conducted on):  2023-01-25
- Recruitment: Prolific (https://prolific.co)
- Prescreening: Native Speakers of German, monolingual
- Payment:   3.50£ (ca.  3.96€)
- Estimated Time Required: 20 minutes
- Used Software: 
	+ jspysch (https://www.jspsych.org)
 	+ jatos (https://www.jatos.org/Whats-JATOS.html - Version 3.5.11)	


# Survey Details

> Note: **column_names** are printed in boldface, *level_names* in italics

- Task: Two Alternative Forced Choice
- Design: **ANSWER** (*PP>OBJ*, *OBJ>PP*) ~ **TYPE** (*INSTR*,*COM(O)*) x **OBJform** (*wh*,*np*) 
- List length: 72
- **ITEM_GROUP**s:
	+ *test*: 24
	+ *filler*: 48
	+ thereof (**ITEM_FUNCTION**): 
		+ *calibration*: 6
		+ *control*: 16
			+ thereof (**ITEM_SUBGROUP**)
			+ *related*: 8 
			+ *unrelated*: 8
		+ *attention*: 12
		+ (other) *filler*: 14
- randomization
	- the presentation order of each stimulus-pair is randomized individually for each trial for each participant
	- each survey is randomized individually for each participant according to the following conditions: 
		+ the survey starts with calibration items in random order 
		+ control items are (otherwise) spread over the whole survey
		+ no test item should be adjacent to any other test item
		+ no control item should be adjacent to any other control item
		+ the survey ends with a filler 


# Participants
- Accepted: 31
	+ Gender: 16 male, 14 female, 1 diverse
	+ Age: 18 - 73 (Ø33,84)
- Rejected: 19
	+ Gender: 8 male, 9 female, 2 no specification
	+ Age: 19 - 67 (Ø29,23)
	+ Reasons:
		- highly distracted and/or failed on control items (i.e. picked the unacceptable option of at least *one* control item): 14
		- left before the survey started: 5


# VARIABLES: ForcedChoice (Experimental Eliciation, Survey)
- id columns:
	- **workerId**: id of participant
	- **ITEM_ID**: id of a minimal pair
	- **OPTION_[0|1]KEY_CONDITION**: Order variant of an individual test stimulus (provides unique identifier of an individual stimulus in combination with ITEM_ID)
   > Note: for *filler* items, conditions are coded as followed (**comment** gives further details): 
	acceptable
        * -> ungrammatical 
        ? -> odd / marked
- answer-related columns:
	- **rt**: reaction / response time: time (ms) needed to answer this trial (from appearance of trial till continue-button pressed)
	- **date_time_begin**:point in time presentation of a stimulus started
	- **date_time_end**:point in time presentation of a stimulus ended
	- **ANSWER**: KEY_CONDITION of the chosen option (i.e. OPTION_[0|1]_KEY_CONDITION of the stimulus)
- presentation-related columns:
	- **ANSWER_POSITION** (*above*/*below*): chosen answer has been presented above/below the other option
- survey-related columns:
	- **trial_index**: trial has been shown as the (trial_index+1)th trial of the survey (first trial has trial_index 0)


# Variables: Participants 	
## From our Demographic Questionnaire 
- **PROLIFIC_PID**: DELETED, required for Payment
- **AGE**: DropDown Menu: *18-75*,*75+*, no specification (*keine Angabe*)
- **GENDER**: *male*, *female*, *diverse*, *no specification* (*männlich*, *weiblich*, *divers*, *keine Angabe*)
- **EDUCATION**
	> "highest educational attainment" ("höchster schulischer Bildungsabschluss")
	- available options:
		+ *in education* (*noch in schulischer Ausbildung*),
		+ *lower secondary school graduation* (*Haupt-(Volks-)schulabschluss*),
		+ *secondary school graduation* (*Realschul- oder gleichwertiger Abschluss*),
		+ *(specialized) university-level graduation* (*Fachhochschul- oder Hochschulreife*), 
		+ *none* (*ohne allgemeinen Schulabschluss*),
		+ *no specification* (*keine Angabe*)
- **EDUCATION_PROFESSIONAL**
	> "highest professional attainment" ("höchster beruflicher Bildungsabschluss")
	- available options:
		+ *in training* (*noch in Ausbildung*),
		+ *apprenticeship (dual)* (*Lehre/Berufsausbildung im dualen System*),
		+ *technical degree* (*Fachschulabschluss*),
		+ *polytechnic degree* (*Fachhochschulabschluss*),
		+ *university degree* (*Hochschulabschluss*),
		+ *bachelor* (*Bachelor*),
		+ *master* (*Master*),
		+ *diploma* (*Diplom*),
		+ *doctorate* (*Promotion*),
		+ *none* (*ohne Ausbildung*),
		+ *no specification* (*keine Angabe*)
- miscellaneous
	> "Which of the following statements applies to you personally? Check all that apply." ("Welche der folgenden Aussagen trifft auf Sie zu?  Bitte kreuzen Sie zutreffende Aussagen an.")
	- multiple selections possible (except for *nothing applies* and *no specification*),
	stored in different boolean variables:
		+ **MISC_MULTILINGUAL**
			> "I have been brought up speaking more than one language." ("Ich bin mehrsprachig aufgewachsen."),
		+ **MISC_NON_NAIVE** 
			> "I have knowledge in linguistics." ("Ich verfüge über sprachwissenschaftliche Kenntnisse."),
		+ **MISC_ABROAD** 
			> "I currently reside in a non-german-speaking country." ("Ich halte mich zurzeit im nicht-deutschsprachigen Ausland auf."),
		+ **MISC_NONE**
			> "Nothing of the above applies." ("Nichts davon trifft zu."),
		+ **MISC_NO_SPEC** 
			> "I do not want to provide any information to this end." ("Ich möchte dazu keine Angaben machen.")
## from a questionnaire after the survey
- **DEVICE**  (optional)
	> "Which device did you use (predominantly) throughout the survey?" ("Welches Eingabegerät haben Sie während des Experiments (vorwiegend) verwendet?")
	- available options: 
		+ *touchscreen* (*Touchscreen*)
		+ *touchpad*  (*Touchpad*)
		+ *mouse* (*Maus*)
		+ *keyboard*  (*Tastatur*)
		+ *other*  (*andere*)
## Demographic Information received from Prolific 
- **Country.of.Birth**
- **Current.Country.of.Residence**
- **Nationality**
