Hi Tarak,
I've taken a pass through the first draft of your blog post and here are my comments by document section.

##Last Paragraph of "Sample, review, label" section.
##==================================================
I can tell from the way your code is structured that feature creation was an iterative process similar to the one described in https://humanloop.com/blog/why-you-should-be-using-active-learning/. I think a very short example of the difference between a "representative sample", "informative targeted records" and "minority class" would tie together the project goals and  the methodology.

##Creating an Index
##=================
It would be good to include a verbal example of how the index/metadata is used downstream in the process. I haven't bumped into the code that uses it yet but I haven't finished converting the bpd pipeline to python.

##A Basic page sampler
##====================
Just for context it would be good to know if this code is for the Chicago project or the University of Washington project. I haven't bumped into it yet but I haven't converted the R code upstream of classify-pages yet.a

##Modeling tools for sequence labeling
##====================================
It would be very useful to understand how you arrived at some of the features in segments-boxy/features/src/feats.R.

I understand that this is part of the "art" of the project and the actual code is the "mechanics" so it may be difficult to describe. For example, feats contins conj_braxht. I understand what re_brax and bin_ht1 are. I'm not sure how you determined that re_brax was a useful feature and even more mysterious, I don't understand how you decided combining the two was useful.  

As I mentioned earlier, it looks like conj_braxht was created iteratively and I'd be real interested to hear about the development loop. What told you that more features were needed? What clues led you to this feature? How did you know it was a good one?

It's a great article and I understood everything you wrote. I appreciate that it is mostly about the "art" of the task and I think your target audience will too. I'll be happy to read another draft, if you'd like.

best,
aaron


=================================================================
07/09/21
Hi Tarak,

I just read your blogpost and I have only one general comment.

In lines 161-170 of the rmd file, it may be obvious to your audience why varied samples could be more useful than statistically accurate ones but I had to think about about it. I think it is because documenting human rights violations may be what I would call a "needle in the haystack" problem. They may be low frequency events in the document set but their importance is much greater than their frequency so they can be missed by a process that strives to be statistically accurate. It may be useful to point this out.

Great article. I understood everything you were explaining.
thanks,
aaron




