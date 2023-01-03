+++
title = "Submit a Moliere Query"
date = "2019-07-15T21:14:35-04:00"
draft = false
aliases = [
  "/post/moliere-run-query/"
]
+++

Thanks for requesting a Moliere query!
By using this form you are requesting us to run your experiment on our supercomputing infrastructure.
Unfortunately, we have not been able to automate this process, so please allow for a little turn around time, and feel free to send us an email if you don't hear back soon.


<h1> Post Query </h1>

<form action="https://formspree.io/justin@sybrandt.com" 
      method="POST"
      id="query">
Query Terms <br />
<input type="text"
       name="keyword_1"
       id="keyword_1"
       placeholder="tobacco"
			 required>
<input type="text"
       name="keyword_2"
       id="keyword_2"
       placeholder="lung cancer"
			 required> <br /> <br />
Number of Topics (typically btwn. 10 - 100) <br />
<input type="number"
       name="num_topics" 
       id="num_topics"
       min=2 max=100 value=20
			 required><br /> <br />
Contact Email: <br />
<input type="email"
       name="contact_email"
			 id="contact_email"
			 pattern="^[a-z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,4}$"
			 required><br /> <br />
<input type="submit" value="Submit">
</form>

<hr>

