<h2> Udacity-Data-Scientist-Nanodegree-Capstone-Project</h2>
<hr>
<h3> Starbuck's Capstone Challenge</h3>
<p>This is the Udacity Data Science Nanodegree Capstone Project. In this project i have done Starbucks project.</p>
<h3>Introduction</h3>
<p>This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.</p> 

<p>Not all users receive the same offer, and that is the challenge to solve with this data set.</p>

<p>Your task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.</p>

<p>Every offer has a validity period before the offer expires. As an example, a BOGO offer might be valid for only 5 days. You'll see in the data set that informational offers have a validity period even though these ads are merely providing information about a product; for example, if an informational offer has 7 days of validity, you can assume the customer is feeling the influence of the offer for 7 days after receiving the advertisement.</p>

<p>You'll be given transactional data showing user purchases made on the app including the timestamp of purchase and the amount of money spent on a purchase. This transactional data also has a record for each offer that a user receives as well as a record for when a user actually views the offer. There are also records for when a user completes an offer.</p> 

<p>Keep in mind as well that someone using the app might make a purchase through the app without having received an offer or seen an offer.</p>

<h4> Dataset overview</h4>
<ul><li>The program used to create the data simulates how people make purchasing decisions and how those decisions are influenced by promotional offers.</li>
<li>Each person in the simulation has some hidden traits that influence their purchasing patterns and are associated with their observable traits. People produce various events, including receiving offers, opening offers, and making purchases.
<li>As a simplification, there are no explicit products to track. Only the amounts of each transaction or offer are recorded.
<li>There are three types of offers that can be sent: buy-one-get-one (BOGO), discount, and informational. In a BOGO offer, a user needs to spend a certain amount to get a reward equal to that threshold amount. In a discount, a user gains a reward equal to a fraction of the amount spent. In an informational offer, there is no reward, but neither is there a requisite amount that the user is expected to spend. Offers can be delivered via multiple channels.
<li>The basic task is to use the data to identify which groups of people are most responsive to each type of offer, and how best to present each type of offer.
</ul>
<h4>Data Dictionary</h4>
<h5>profile.json</h5>
Rewards program users (17000 users x 5 fields)
<ul>
<li>gender: (categorical) M, F, O, or null</li>
<li>age: (numeric) missing value encoded as 118</li>
<li>id: (string/hash)</li>
<li>became_member_on: (date) format YYYYMMDD</li>
<li>income: (numeric)</li>
 </ul>
<h5>portfolio.json</h5>
Offers sent during 30-day test period (10 offers x 6 fields)
<ul>
<li>reward: (numeric) money awarded for the amount spent</li>
<li>channels: (list) web, email, mobile, social</li>
<li>difficulty: (numeric) money required to be spent to receive reward</li>
<li>duration: (numeric) time for offer to be open, in days</li>
<li>offer_type: (string) bogo, discount, informational</li>
<li>id: (string/hash)</li>
  </ul>
<h5>transcript.json</h5>
Event log (306648 events x 4 fields)
<ul>
<li>person: (string/hash)</li>
<li>event: (string) offer received, offer viewed, transaction, offer completed</li>
<li>value: (dictionary) different values depending on event type</li>
<li>offer id: (string/hash) not associated with any "transaction"</li>
<li>amount: (numeric) money spent in "transaction"</li>
<li>reward: (numeric) money gained from "offer completed"</li>
<li>time: (numeric) hours after start of test</li>
  </ul>
<hr>
<h3>Installation</h3>
This project is done in Jupyter Notebook, so all packages al already downloaded in Anaconda. There are several packages we reqired in this project.
<ul>
<li>pandas</li>
<li>numpy as np</li>
<li>math</li>
<li>json</li>
<li>time</li>
<li>matplotlib</li>
<li>sklearn.model_selection</li>
<li>sklearn.preprocessing</li>
<li>sklearn.tree</li>
<li>sklearn.ensemble</li>
<li>sklearn.metrics</li>
<li>sklearn.linear_model</li>
</ul>
<hr>
<h3> File Description</h3>
<ul>
<li>transcript.json</li>
<li>profile.json</li>
<li>portfolio.json</li>
<li>Starbucks_Capstone_notebook.ipynb</li>
</ul>
<hr>
<h3>Project Motivation</h3>
<p>This project is the Capstone project of my Data Scientist nanodegree with Udacity. As students in the nanodegree, we have the option to take part in the Starbucks Capstone Challenge. For the challenge, Udacity provided simulated data that mimics customer behavior on the Starbucks rewards mobile app.</p>

In this project, I use the data to answer 2 business questions:
<pre>
a. What are the main drivers of an effective offer on the Starbucks app?
b. Could the data provided, namely offer characteristics and user demographics, predict whether a user would take up an offer?
</pre>
<p>To answer the above 2 questions, I created 3 models for the data on the 3 offer types provided. The three offers are: Buy One Get One Free (BOGO), Discount (discount with purchase), and Informational (provides information about products).</p>
<br>
As a brief summary of my findings:
<br>
<p>For Question 1, the feature importance given by all 3 models were that the tenure of a member is the biggest predictor of the effectiveness of an offer. Further study would be able to indicate what average tenure days would result in an effective BOGO offer.</p>

<p>For Question 2,my decision to use 3 separate models to predict the effectiveness of each offer type ended up with good accuracy for the 2 of the models (82.83% for BOGO and 87.35% for discount), while slightly less accurate performance for another informational offers (75.3%). However, I would regard 75% as acceptable in a business setting, as for informational offers, there is no cost involved to inform users of a product. Meanwhile, an 80% and above accuracy in a business setting would be acceptable to show offers to people, even if the model misclassifies a few, the overall revenue increase might justify the few mistakes.</p>
<hr>
<h3> Results </h3>
  All the finding and conclusion can be check in the ```Starbucks_Capstone_notebook.ipynb``` file.
<hr>
<h3>Licensing, Acknowledgement</h3>
<p>All the data is provided by Udacity. All the credit i will to Udacity and Startbucks. Check the licensing information on the udacity website</p>
