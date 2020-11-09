# Credit card fraud detection

![image-1](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-1.jpg)

1. What is Credit Card Fraud ?

  Credit card fraud is an inclusive term for fraud committed using a payment card, such as a credit card or debit card.[1] The purpose may be to obtain goods or services, or to make payment to another account which is controlled by a criminal. According to [2] Credit card fraud happens when someone — a fraudster or a thief — uses your stolen credit card or the information from that card to make unauthorized purchases in your name or take out cash advances using your account.

2. How does credit card fraud happen?

Here are some common ways fraudsters can get their hands on your credit card number.

    A thief digs through your trash, finds discarded receipts or credit card statements that include your account number, and uses that information to rack up fraudulent charges.
    An unscrupulous waiter steals your card number and uses it to finance, say, a Caribbean vacation.
    An identity thief lures you to a fraudulent website where you are tricked into providing your card number. The thief then uses your credit card information for fraudulent purchases.
    You swipe your card at your local ATM or at the gas pump. Later, you notice fraudulent purchases on your statement. What happened? Someone might have installed a credit card skimmer to steal your account information. A credit card skimmer is a small device that thieves can install anywhere you swipe your card. Skimming has proved to be an effective way for thieves to steal credit card information.
    Sometimes your credit card information is stolen through no fault of your own. Your credit card number might be exposed in a data breach that hits one of your favorite retailers. Thieves can then use this information to rack up online charges with your credit card account numbers.
    Thieves often buy stolen credit card numbers on the dark web, that part of the web that’s only accessed through special software. Credit card numbers are valuable to thieves, and they aren’t shy about visiting illegal dark web markets to get them.
    Someone in your home — a resident, guest, visitor, or service technician — might manage to access your credit cards. It’s possible the person could use your credit card information fraudulently.

3. 10 tips to help protect yourself from credit card fraud

Criminals have seized upon the credit card industry as a place to make a quick buck. Fortunately, you can help minimize your risk of becoming a victim of credit card fraud by taking steps to protect your credit card information. Here are 10 tips to help you do just that.

    Promptly and carefully review every credit card statement. When your bill arrives, don’t just make the payment. Review each transaction and, if any are unfamiliar, immediately call the card issuer. Even better, don’t wait for the statement. Regularly review your transactions online on the card issuer's website.
    Protect your account information. Don’t leave account information out in the open where others might see it.
    Destroy old statements. When you finish with the monthly statement, shred it before discarding it.
    Carry only the cards you need. If you have more than one credit card, do you need to have more than one when you’re out and about or traveling? Reduce your risk, by leaving unneeded cards at home.
    Don’t fall for phishing scams. You might receive emails in your inbox from what looks like your cable TV provider, internet service provider, or bank asking you to provide your credit card information, often to avoid losing your service. Don’t fall for these scams. They’re usually run by hackers looking to steal your information. Never send your credit card information to anyone who asks for it online. Call your service provider’s customer service number instead to make sure a request is legitimate.
    Check your credit reports: You can order one free copy of each of your three credit reports -- maintained by Experian, Equifax and TransUnion — once a year from AnnualCreditReport.com. Once you order these reports, look carefully for accounts or loans in your name that you don’t remember opening. New lines of credit may have been opened by thieves who have gained access to your personal information.
    Watch out for phone scams. Thieves don’t rely solely on the internet to steal your credit card information. They might also turn to the phone. They might call you, saying that they are from your credit card provider. They’ll then ask you to provide your credit card number so that they can “update” your account. Don’t fall for this. Your bank will never ask you to provide your credit card information over the phone.
    Go paperless. Sign up for online statements from your credit card provider and cancel any monthly paper statements. This lessens the chance that thieves will be able to gain access to papers that include your account information.
    Report lost cards or suspected fraud quickly. The faster you report suspected fraudulent purchases, the better. Your credit card provider can put a hold on your card or cancel your account if you suspect fraud.
    Access your credit card account online. You can spot potential fraud more quickly if you sign up with your credit card provider’s online portal. This way, you can check your credit card account daily, instead of waiting for your monthly statement to arrive.


This Work

Tried to predict Credit Card Fraud using Naive Bayesian classifier.

Variable Prediction:

V1 , V2 ,V3 , V4 , V5 , V6, V7 , V8, V9 , V10

V11, V12, V13, V14, V15, V16, V17,V18, V19, V20

V21, V22, V23, V24, V25, V26, V27, V28, Amount

Variable Target : Class

4. Naive Bayes classification

Naive Bayes is a classification technique based on Bayes’ Theorem with an assumption of independence among predictors. In simple terms, it assumes that the presence of a particular feature in a class is unrelated to the presence of any other feature.

For example, a fruit may be considered to be an apple if it is red, round, and about 3 inches in diameter. Even if these features depend on each other or upon the existence of the other features, all of these properties independently contribute to the probability that this fruit is an apple and that is why it is known as ‘Naive’.

Naive Bayes model is easy to build and particularly useful for very large data sets. Along with simplicity, Naive Bayes is known to outperform even highly sophisticated classification methods.

Bayes theorem provides a way of calculating posterior probability P(c|x) from P(c), P(x) and P(x|c). Look at the equation below:

![image-2](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-2.jpg)

Above,

P(c|x) is the posterior probability of class (c, target) given predictor (x, attributes). P(c) is the prior probability of class. P(x|c) is the likelihood which is the probability of predictor given class. P(x) is the prior probability of predictor.

How Naive Bayes algorithm works? Let’s understand it using an example. Below I have a training data set of weather and corresponding target variable ‘Play’ (suggesting possibilities of playing). Now, we need to classify whether players will play or not based on weather condition. Let’s follow the below steps to perform it.

Step 1: Convert the data set into a frequency table

Step 2: Create Likelihood table by finding the probabilities like Overcast probability = 0.29 and probability of playing is 0.64.

![image-3](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-3.jpg)

Step 3: Now, use Naive Bayesian equation to calculate the posterior probability for each class. The class with the highest posterior probability is the outcome of prediction.

Problem: Players will play if weather is sunny. Is this statement is correct?

We can solve it using above discussed method of posterior probability.

P(Yes | Sunny) = P( Sunny | Yes) * P(Yes) / P (Sunny)

Here we have P (Sunny |Yes) = 3/9 = 0.33, P(Sunny) = 5/14 = 0.36, P( Yes)= 9/14 = 0.64

Now, P (Yes | Sunny) = 0.33 * 0.64 / 0.36 = 0.60, which has higher probability.

Naive Bayes uses a similar method to predict the probability of different class based on various attributes. This algorithm is mostly used in text classification and with problems having multiple classes.

* What are the Pros and Cons of Naive Bayes?

    Pros:

It is easy and fast to predict class of test data set. It also perform well in multi class prediction When assumption of independence holds, a Naive Bayes classifier performs better compare to other models like logistic regression and you need less training data. It perform well in case of categorical input variables compared to numerical variable(s). For numerical variable, normal distribution is assumed (bell curve, which is a strong assumption).

    Cons:

If categorical variable has a category (in test data set), which was not observed in training data set, then model will assign a 0 (zero) probability and will be unable to make a prediction. This is often known as “Zero Frequency”. To solve this, we can use the smoothing technique. One of the simplest smoothing techniques is called Laplace estimation. On the other side naive Bayes is also known as a bad estimator, so the probability outputs from predict_proba are not to be taken too seriously. Another limitation of Naive Bayes is the assumption of independent predictors. In real life, it is almost impossible that we get a set of predictors which are completely independent.

5.Practical example

![image-4](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-4.jpg)


Check missing data

Some might quibble over our usage of missing. By “missing” we simply mean NA (“not available”) or “not present for whatever reason”. Many data sets simply arrive with missing data, either because it exists and was not collected or it never existed.

![image-5](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-5.jpg)

VISUALIZING THE DATA

![image-6](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-6.jpg)
![image-7](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-7.jpg)


Plotting Heatmap

Heatmap can be defined as a method of graphically representing numerical data where individual data points contained in the matrix are represented using different colors. The colors in the heatmap can denote the frequency of an event, the performance of various metrics in the data set, and so on. Different color schemes are selected by varying businesses to present the data they want to be plotted on a heatmap [3].

![image-8](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-8.jpg)


SPLITING DATA

Data for training and testing To select a set of training data that will be input in the Machine Learning algorithm, to ensure that the classification algorithm training can be generalized well to new data. For this study using a sample size of 30%, assumed it ideal ratio between training and testing

![image-9](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-9.jpg)
![image-10](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-10.jpg)


Confusion Matrix

is commonly used for a summarization of prediction results on a classification problem.The number of correct and incorrect predictions is summarized with counting values and each value broken down for each class. Each of them is the key to the confusion matrix. It shows the classification model is confused when it makes predictions, at this point in here it gives us insight not only into the errors being made by a classifier but also show the types of errors that are being made [4].

![image-11](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-11.jpg)


Accuracy

is closeness of the measurements to a specific value. Accuracy has two definitions:

    More commonly, it is a description of systematic errors, a measure of statistical bias; low accuracy causes a difference between a result and a "true" value. ISO calls this trueness.
    Alternatively, ISO defines[1] accuracy as describing a combination of both types of observational error above (random and systematic), so high accuracy requires both high precision and high trueness.
    
![image-12](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-12.jpg) 


Precision and Recall

Precision is a description of random errors, a measure of statistical variability. In simpler terms, given a set of data points from repeated measurements of the same quantity, the set can be said to be accurate if their average is close to the true value of the quantity being measured, while the set can be said to be precise if the values are close to each other. While Recall is defined as the fraction of relevant documents retrieved compared to the total number of relevant documents (true positives divided by true positives+false negatives).

![image-13](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-13.jpg) 


ROC Curve

is a graphical plot that illustrates the diagnostic ability of a binary classifier system as its discrimination threshold is varied.

![image-14](https://github.com/hemangikinger/Fraud-Detection/blob/master/image-14.jpg) 


    




