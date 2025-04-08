# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author: ANJISHNU BOSE

```
The given code in whitby_covid_tracing.py tries to implement a function to simulate the model outlined in the blogpost. However, it is different in quite a few implementations.

We start with defining the two events : wedding and brunch. The original blogpost outlined a scenario where we have a small number of wedding with a large number of attendees each (eg. 2 weddings with 100 attendees each), and a large number of brunches with a small number of attendees (eq. 80 different brunches with 10 attendees each). This simple toy model attempts to simulate a real world scenario in a population of N=1000. However, the code immediately deviates by just having two event classification : one wedding with 200 people, and one brunch with 800 people!

Next, the blogpost assumes a 10% (ATTACK_RATE variable) infection chance for each person independently. This is again different than the implementation in the code where a numpy sampling function np.random.choice() is used to randomly select 10% of the total population (100) without replacement. This is different cause in the former 10$ of the sample on average would get infected, not always. The latter is not assuming infections to be independent from each other. 

We then assume a uniform probability of being able to trace an infected person with probability 20% (TRACE_SUCCESS variable). We randomly sample 100 uniformly distributed random variables using np.random.rand() corresponding to each infected person. Whenever these variables are less than 0.2, the corresponding infected person is succesfully traced. This is followed by counting the total succesful traces per event category. If any event is found to have more than 2 (SECONDARY_TRACE_THRESHOLD) traces, all the infected people in that category are assumed to be traced succesfully.

Its evident that this is not the original model given in the blogpost. the entire point of that model is to highlight that since the number of attendees in small social gathering is generally much smaller than large events like weddings, the chance of having two independent (primary and secondary) traces into the same event like a brunch is highly unlikely. Hence in the total traced cases, small social gatherings will be underrepresented, or equivalently large gatherings like a wedding will be overrepresented. This is NOT the case with the current implementation since we have two large events with 200 and 800 people. In fact, we actually recover the true distribution with a high level of accuracy.

Since the code involves sampling 100 people out of 1000 to get infected, along with randomly selecting succesfull traces, it involves some randomness. Therefore, in general the plots are not reproducible. They can be made reproducible by fixing a random seed in numpy.

In my version of the simulation, I follow the blogpost more closely and define events w_i. i={1, 2}, and b_i, i={1, 2, ..., 80} to represent the different weddings and brunches (the code is more general but I am sticking with the numbers in the blogpost for simplicity). We then infect people independently by sampling 1000 uniformly distributed random variables such that whenever the random number is < 0.1, the person is infected. Everything else stays the same and now we see that our plots reproduce the blogpost. Lastly, to make things reproducible we set the seed to be equal to the simulation index each time. The simulation is run multiple times, each run with a fixed seed and hence is totally reproducible for a fixed number of runs (n_runs). 

```


## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 09/04/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
