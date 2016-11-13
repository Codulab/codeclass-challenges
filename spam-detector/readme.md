# SPAM DETECTOR

Not long ago, a spam campaign originated on some of the major social networks, and has started affecting Codeclass users as well. Most of the spam comes from a limited number of highly-motivated individuals, possibly from a single group, who constantly update their spam software. What started off as simple messages-sending bots now evolved into something that requires a large team of engineers to fight against it.

At the very beginning, the bots were not that clever. The spam detection could essentially be narrowed down to checking several simple criteria. For the given user's stream of messages over a given time period, the spammer could be identified if any of the following rules are broken:

### Rules
1. more than 90 % of all messages had fewer than 5 words (here, a word is defined as a sequence of consecutive Latin letters which is neither preceded nor followed by a Latin letter);
2. more than 50 % of messages to any one user had the same content, assuming that there were at least 2 messages to that user;
3. more than 50 % of all messages had the same content, assuming that there were at least 2 messages;
4. more than 50 % of all messages contained at least one of the words from the given list of spamSignals (the letters' case doesn't matter).

Since you are applying for the Anti-Spam team at Codeclass, you want to make sure you understand how the basic spam detection programs worked. Implement a function that, given a stream of messages and a list of spamSignals checks if it is possible that the user is a spammer by checking the criteria above.

### Example 1:
    For

    messages = [["Sale today!", "2837273"],
                ["Unique offer!", "3873827"],
                ["Only today and only for you!", "2837273"],
                ["Sale today!", "2837273"],
                ["Unique offer!", "3873827"]]

    and spamSignals = ["sale", "discount", "offer"], the output should be

    spamDetection(messages, spamSignals) = [
      "passed",
      "failed: 2837273 3873827",
      "passed",
      "failed: offer sale"
    ]

    Here are the results of the checks per criterion:
        4 out of 5 (80 %) messages have fewer than five words, which is fine;
        2 out of 3 messages to user 2837273 are the same, which is a good spam indicator; also, both messages to user 3873827 are the same;
        2 out of 5 (40 %) messages have the same content, which is fine;
        4 out of 5 (80 %) messages contain spam signals "offer" or "sale".

### Example 2:
    For

    messages = [["Check CodeClass out", "7284736"],
                ["Check CodeClass out", "7462832"],
                ["Check CodeClass out", "3625374"],
                ["Check CodeClass out", "7264762"]]

    and spamSignals = ["sale", "discount", "offer"], the output should be

    spamDetection(messages, spamSignals) = [
      "failed: 1/1",
      "passed",
      "failed: Check CodeClass out",
      "passed"
    ]

    Since all users in messages received only one message each, it's impossible to check the second criterion. The fourth criterion doesn't match: there are no spam signals in the messages. However, the first and the third criteria failed, since all the messages contain 4 words and have the same content.

### Returning Your Result:
    Your function should return an Array of 4 strings, the results of checks per criterion. The results for each criterion should be given in the following format:

*	"passed" if the check doesn't suggest that the user is a spammer, otherwise:
    1.   for the first criterion: "failed: <failed_ratio>", where <failed_ratio> is the ratio of messages with fewer than 5 words as a reduced fraction;
    *   for the second criterion: "failed: <recipient_1> <recipient_2> ...", where <recipient_i> is id of the spammed user. Recipients should be sorted in ascending order of their ids;
    *   for the third criterion: "failed: <message>", where <message> is the message sent to more than 50 % of recipients;
    *   for the fourth criterion: "failed: <spamSignal_1> <spamSignal_2> ...", where <spamSignal_i> is the spam signal that appeared in at least one message. Spam signals should be sorted Alphabtically.



##### Specification
You can build your solution using PHP, Javascript(jQuery) or NodeJS. If you're using python ensure you host your solution on Heroku - https://www.heroku.com/

#### REWARD
* N3,000 Cash Reward
* Career & Professional Mentorship
* Heroku T-shirt + Stickers

![Heroku T-Shirt](http://i.picresize.com/images/2016/08/01/IupJg.jpg)


#### SUBMISSION INSTRUCTION 
* Click the registration button at the top of this page.
* Once registered, come back to this page with a participate button.
* Click the participate button at the top of the page.
* Upload your zipped code


#### SELECTION CRITERIA
All entries will be judged using the following criteria:
* Code cleanness.
* Code efficiency (less lines of code do more)
* Validation for numbers / strings
* Handling of exceptions
* Handling of special cases


#### ELIGIBILITY CRITERIA
Candidate must be a student of either a university or polytechnic in Nigeria. A proof of identification will be requested to redeem prize.

#### WINNER SELECTION
Winners are selected by Codulab team and are chosen solely at the Codulab's discretion. 

#### PAYMENTS
Codulab will compensate members in accordance with the payment structure of this challenge. The payment will be made when the eligible winner has been announced.