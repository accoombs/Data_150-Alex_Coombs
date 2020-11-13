Alex Coombs

DATA 150

10/30/20

Word Count: 1208

Assignment 3


Introduction:

As a continent, Africa has the highest mortality rate and is the only continent with more deaths attributed to infectious disease than chronic illness (1). Healthcare greatly contributes to overall wellbeing and achieving an objectively good life, so it must be a priority when increasing the overall wellbeing of Sub-Saharan Africa. Even though factors such as economic output and corruption limit sub-Saharan African development, developing an effective healthcare system is integral to the future of the region. Some of the limitations to achieving effective healthcare in sub-Saharan Africa reside in its lack of adequate census data and lack of access to health centers/health professionals. Even with the aggregate health data in the region indicating that it is the worst in the world, different countries vary in healthcare quality, and sub-populations within the Sub-Saharan countries do as well. For example, according to a Gallup world poll conducted in 2012, only 17% of respondents in Madagascar and Tanzania reported being in perfect health, while 50% of respondents in Ethiopia and Somaliland reported being in perfect health. This trend of inequality does not apply solely to general health, but also contact with health professionals, with less than 50% of respondents in Ghana reporting ever being in contact with a health official, and less than 10% in Sudan (1). Data science methods that implement user-generated data such as CDR and search query data have the potential to greatly mitigate the spread of infectious disease in sub-Saharan Africa, and one such method is predicting the spread of infectious disease by. This approach is evaluative since it aims to describe the potential benefits of using this data and is looking more at the potential use of specific methods rather than explaining a trend. This type of inquiry is uniquely appropriate for this topic since the methods used will be at the forefront of this question’s focus. Within this question, there exists the questions of: What is the nature of this user-generated data, and why is that useful for mitigating the spread of infectious disease? What data science methods are useful for mitigating the spread of infectious disease? What are the limitations of using methods that implement this data, and how can this be addressed? All these questions relate to specific steps in evaluating the usefulness of these data methods and will contribute to a nuanced understanding of their advantages and disadvantages. 


Methods:

DNN and LSTM models implement deep learning algorithms to more generate more accurate predictions regarding the spread of infectious disease than previous statistical models that did not implement AI. This was shown to be true in a study where internet search query data, weather and climate data, and social media big data was used to accurately predict the spread of chicken pox, scarlet fever, and malaria in South Korea. The search query data was taken from the search engine “Naver,” and was comprised on searches that involved key terms or phrases such as “chicken pox” or “chicken pox symptoms”. The weather and climate data were daily averages and were taken from the Korean Meteorological Administration(2). 

![alt text](https://github.com/accoombs/Data_150-Alex_Coombs/blob/master/Screenshot%202020-11-09%20155755.png)

Figure describes the variables used for the predictive models (DNN, LSTM, ARIMA, OLS)


1.	DNN:
 
![alt text](https://github.com/accoombs/Data_150-Alex_Coombs/blob/master/Screenshot%202020-11-09%201456451.png)

Figure is a visual representation of a neuron used in the DNN models.

The DNN models use 3 or more node layers, the first layer being the input node, and the other layers for non-linear algorithms. The equation used for each of the neurons in the DNN models used is the following: σ :Sum = w · x + b, y :f(σ) = f(w · x + b). The variables used are b: Bias, x: input, y: output, w: weight, σ: calculation function, f(σ): activation function. The DNN model implements the “Dense Layer” option of Keras package in python 3.5.3 for analysis. All the ten parameters in the “Dense Layer” were used in their default setting except for the units, activation, and dropout(2). 

2.	LSTM:

This model is termed Long-Short Term Memory. In each layer the model establishes what information should be remembered and forgotten from the input. This is a recurrent neural network and each iteration it refines what to forget and renew from each input. The equations used for the LSTM model are the following:

![alt text](https://github.com/accoombs/Data_150-Alex_Coombs/blob/master/Screenshot%202020-11-09%20153210.png)

The input for the function is represented by xt.  ft  determines what information to be saved is created by it and C˜t, Ct, the cell layer, is renewed by ft, it, and C˜t. The layer finally receives a value from -1 to 1 as represented by the output ht. The LSTM layer is used from the Keras package of Python 3.5.3. All the 23 parameters were set to their default value except for the units, activation function, return sequence, and dropout(2). 


Results: 

The DNN model had a significant performance increase over two statistical models, OLS and ARIMA models, displaying a 24.45% improvement according to an RSME test. The LSTM also showed a significant improvement over the other statistical models with a performance increase of 18.75%. In addition, the DNN and LSTM models displayed unique strengths. The DNN model was the most accurate when a disease is consistently prevalent, and was most accurate overall, but the LSTM model was the most accurate for rapidly spreading diseases as indicated by rapidly increasing occurrences. Also, the LSTM model is better for predicting a maximum number of infections while the DNN model was better for predicting the minimum(2). 



Discussion:

The user-generated data in this study were the search query data and social media big data. As a data set, they have advantages such as being accurate temporally, since each search or post has a time stamp, but they do not provide any spatial data. However, since people are constantly generating the data it is always relevant and recent, which makes it a good option for a constantly evolving problem such as the spread of infectious disease. As for what data science methods are useful for mitigating the spread of infectious disease, methods such as DNN and LSTM have shown themselves to be effective due to their flexibility that inherently comes with their use of AI. Also, CDR data, even though no methods using it are presented, is an effective way to gather temporal, but more importantly spatial data, and the methods that implement it reflect this. The main limitation of all user generated data, such as search queries, social media, and CDR data is that people must have the technology necessary to generate it. This places a positive bias on wealthier populations, and in the context of sub-Saharan Africa, this places a positive bias on urban areas, and a bias against rural or poorer areas. There is no real way to remedy this from the ground up besides giving people the tools needed to generate the data, modern technology, but that comes with a host of issues such as access to electricity and general maintenance. These populations can be included when addressing a country to some, if they are included in population numbers, but the problem of data generation remains. This is the major limitation in the data science methods I have researched, and somehow including rural and poorer populations in data science methods where they produce no data is the next step in creating a holistic solution for addressing the spread of infectious disease in sub-Saharan Africa.


References: 

1.	Deaton, Angus S., and Robert Tortora. “People In Sub-Saharan Africa Rate Their Health And Health Care Among The Lowest In The World.” Health Affairs, vol. 34, no. 3, 2015, pp. 519–527., doi:10.1377/hlthaff.2014.0798

2.	Chae S, Kwon S, Lee D. Predicting Infectious Disease Using Deep Learning and Big Data. Int J Environ Res Public Health. 2018;15(8):1596. Published 2018 Jul 27. doi:10.3390/ijerph15081596.                                                                                               
