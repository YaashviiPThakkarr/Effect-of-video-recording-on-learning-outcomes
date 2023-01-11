# Effect-of-video-recording-on-learning-outcomes

- We analyzed the effect of video recording on the learning outcomes of students by conducting a A/B Testing experiment.

- The data for this experiment was collected through a survey which asked the respondents about their existing knowledge of A/B testing. The survey was open to anyone who was provided the link through social media, messages or emails. It was open from 15th Nov - 12th December, 2022. The survey started with a short pre-quiz (2 questions) to test the pre-existing knowledge of the participants.  

- It had general questions such as ‘What do you think A/B testing is?’.  It then showed a random 5-minute educational video about A/B testing. Before the video, half of the participants were randomly asked if they wanted to turn their recording on when they watched the video. The facial expressions of those who complied (they could choose not to) were recorded in a number of facial feature categories. They were then given a quiz (8 questions) testing their new knowledge on A/B testing. The post-video questions were multiple choice questions related to the content of the video. Pre and post quiz responses were one of the aspects of data collected. They were then asked demographic questions based on gender, age, employment, race and industry, as well as about their emotions while watching the video and solving the quiz. Data of 254 people who were able to complete the survey was collected in a time span of 4 weeks and it was then made available in a CSV format file for us to run experiments.

- We ran an A/B test to understand whether being recorded while watching an educational video has an impact on the learning outcomes (in the form of quiz scores). We also checked whether this impact was different for different genders. Since we randomized the treatment - recording a participant - we have a causal framework to solve this problem. Therefore, we needed to run an A/B testing experiment. This is different from an observational study since we were able to manipulate/intervene by randomizing treatment, instead of simply observing and recording the behavior or characteristics of a group of subjects over time. 

- Additionally, since we are testing a specific hypothesis and the effect of a specific treatment, our experiment design follows an A/B test, and not an observational study. The people in the control group were those who were not asked to turn their video on and the treatment group comprised people who were asked whether they want to be recorded while they are watching the video. The people for both groups were chosen randomly and they had a 50% selection rate of being in the treatment group. 141 people were part of the control group and 113 people in the treatment group were the ones who had the option of turning their camera on while watching the video. Both groups attempted the pre-video and post-video quiz. 

## Design: 
For each subject, we computed the % of correct answers in the pre-quiz and post-quiz. We then regressed the post-quiz % score on whether the subject was recorded while watching the educational video. This regression will allow us to determine whether being recorded makes a significant difference on the post-quiz score i.e the learning curve. This is simply the Intention to Treat. We then find the Local Average Treatment Effect by restricting the analysis to only the compliers in the treatment group. We have further also studied whether being recorded has a different effect on the learning outcome (post-quiz score) based on the gender through heterogenous Intention to Treat(ITT) and Local Average Treatment effect (LATE).

### Our hypothesis is that being recorded while watching an educational video could be distracting (as it makes one more self-conscious) and might have a negative impact on the learning curve/educational outcomes. Running these tests will help us prove/disprove this hypothesis.

1. Unit of analysis (i) : 1 participant (Total participants: 254)
2. Treatment Assignment (T=0/1): prompted to keep recording on (this was randomized)
3. Compliance (X=0/1): what i selects
4. Moderator Variable (Z=0/1): whether participant is male/female. 1 if male, 0 if female
5. Outcome (y): % on post-quiz
6. Goal: 
 ##     y= alpha + beta*T + e (Find ITT), y=lambda + delta*X + e (Find LATE) and find heterogeneous effects.


Our study will help the educational institutes in knowing whether mandating video-on mode during remote classes is beneficial for learning outcomes of the students or not. An example of the problem this A/B testing is trying to study is that people who watch the video, and have their cameras recording on, might focus less on the content of the educational video and they might  look momentarily at their own selves due to self-consciousness. This can impact their learning and in our study affect the number of correct quiz answers that they give. Whereas someone who is solely focused on one part of the screen which is the video, and can’t view his or her own camera recording, will be able to concentrate better on the content of the video. This could be the other way round too. Through our study, we will be able to comment on learning outcomes when being recorded and how these are different based on genders.
 
 
Here's the code of our analysis: [Code] (A_B_Testing_Project.ipynb)
Presentation: [Presentation]
Report: [Report] 
