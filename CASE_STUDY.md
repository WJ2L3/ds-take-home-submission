# Case Study

## What a good summary is for this team, and why
This team vets companies before picking them as suppliers or project partners, so a good summary should include the general information of the company, directors and shareholders information, financial condition especially revenue and profit, and the court cases.

More further, the summary should have highlight the important information for faster read through the summary, as well as give suggestion on the company suitability as suppliers or project partners.

## What have built
The model chosen is Gemini 3.5 Flash Lite, this model is suitable for large amount of repeatable process and fulfill the requirements of 2, 3 times of 100,000 tokens in free tier.

The system will read the line of companies.jsonl file and send the company record to the model for generate summary that include below information:

* General information of the company
* Directors, directors designation and shareholders information and shared capital
* Summary of financial condition on revenue and profit
* Summary of number of court cases with roles, types and status

**version 0.1**  
Test the generate summary system on individual company record.

**version 0.2**  
Test the system ability of running continuously on partial of company records.

**version 1.0**  
The system just use the model to generate general summary with the company record given.

**version 2.11, 2.12**  
Test the system with set the system instruction in the model configuration on individual company record.

**version 2.2, 2.3**  
The system set the system instruction in the model configuration to tell the model the information that must include in the summary. Tune the system instruction and prompt by the results, which generate different versions of summary. Tuning on version 2 is not done due to lack of time.

## How to know whether it's good

**Accuracy**  
Is the summary have the same information with the original record?

**Information Completeness**  
Does the important information include in the summary?

**Irrelevant information**  
Is the summary avoid unnecessary information?

**Readability**  
Is the summary too long for quick review?

## What would do next to keep improving it

**Continue tune the system**  
Continue tune the newest 2.3 version.  
Add more information that align to the team needs.  
Seperate into different paragraph for more readability.

**Add evaluation process when generating summary**  
Further version should use model to compare the summaries and the company records given.

If the summary have:  
* Omits required information and important details  
* Inaccurate information  
* Does not follow the format

Will resend the generate summary prompt to the model.

**Add highlight and suggestion**  
The summary have highlight or bold on important information.  
The summary will classify the company financial condition into different level  
The summary will give suggestion on company suitability as suppliers or project partners.
