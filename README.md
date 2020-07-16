# Detection-of-Propaganda-Techniques-in-News-Articles

Task Description:
    
Background: We refer to propaganda whenever information is purposefully shaped to foster a predetermined agenda. Propaganda uses psychological and rhetorical techniques to reach its purpose. Such techniques include the use of logical fallacies and appealing to the emotions of the audience. Logical fallacies are usually hard to spot since the argumentation, at first sight, might seem correct and objective. However, a careful analysis shows that the conclusion cannot be drawn from the premise without the misuse of logical rules. 
                Another set of techniques makes use of emotional language to induce the audience to agree with the speaker only on the basis of the emotional bond that is being created, provoking the suspension of any rational analysis of the argumentation. All of these techniques are intended to go unnoticed to achieve maximum effect.      

Technical Description: The overall goal of the shared task is to produce models capable of spotting text fragments in which propaganda techniques are used in a news article.
                                                We have compiled a corpus of about 550 news articles in which fragments containing one out of 18 propaganda techniques have been annotated. We split the overall task into two subtasks:

Task - 1:  Given a plain-text document, identify those specific fragments which contain at least one propaganda technique. This is a binary sequence tagging task. We refer to it as SI (Span Identification). 

Task - 2: Given a text fragment identified as propaganda and its document context, identify the applied propaganda technique in the fragment. Since there are overlapping spans, formally this is a multilabel multiclass classification problem. However, whenever a span is associated with multiple techniques, the input file will have multiple copies of such fragments, so the problem can be algorithmically treated as a multiclass classification problem. Although the data has been annotated with 18 techniques,given the relatively low frequency of some of them, we decided to merge similar underrepresented techniques into one superclass:                 

          1) Bandwagon and Reductio ad Hitlerum into "Bandwagon,Reductio ad Hitlerum"                     
          2) Straw Men, Red Herring and Whataboutism into "Whataboutism,Straw_Men,Red_Herring"
          
and to eliminate "Obfuscation,Intentional Vagueness,Confusion". Therefore this is a 14-classes classification task, which we refer to as TC (Technique Classification).                 
            
Reference: https://propaganda.qcri.org/semeval2020-task11/index.html
