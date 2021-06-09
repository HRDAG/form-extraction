-- in your initial description of the use of admin docs, you might also 
cite our work in Chad. I think this is the best explanation: 
https://hrdag.org/wp-content/uploads/2013/02/State-Violence-in-Chad.pdf

-- "You’ll still want to sample and label some examples..." I think 
you might want to include an example of what you mean by an example. 
Along with the regex you might use to find them.

-- I think the pipe creating the index in "creating an index" might 
check for uniqueness in the `fileid`. I'm not suggesting that an 8 
character random id is likely to have collisions in any reasonable 
number of files, but I think checking for uniqueness is a good way to 
signal that you mean it to be a key to the files. Do I understand this 
correctly?

-- the first paragraph under "page classification" seems to belong to 
the previous section?

-- "That makes collecting ground-truth data about page types a breeze" I 
_think_ I follow what you're suggesting here, but it could really 
benefit from an example. The layout data example in the appendix is 
fantastic, more of these would be really helpful. Esp for training data, 
which I take as the central theme of this post.

-- in "modeling tools for sequence labeling" do you still think that 
HMMs or RNNs are the right models? LSTMs are maybe just a subclass of 
RNNs, but I wonder if you want to call them out specifically? And do you 
trust HMMs at all? Lastly, I thought you'd shifted from CRFs to LSTMs 
mostly, but this seems to suggest the other way. Any chance you could 
explain why you prefer CRFs?

Patrick and Tarak both note that this could be more of a small handbook, 
and I love that idea as one output. I know Tarak has also been 
developing a number of training materials for the reviewers at II, so we 
could ultimately have a whole collection of handbooks for folks doing 
(or thinking about) this work.

I think creating it as an evolving handbook somewhere doesn’t preclude 
also publishing this content as a technical blogpost. Which brings me to 
my first question - historically, we have broken up pieces this long 
into multiple parts. As I was reading, I could imagine some natural 
places to break and say we’ll cover this next topic in part 2! But I 
also wonder what the general style is these days for these kinds of 
technical essays. If someone is going to click through all the parts in 
one reading anyway, is there any functional difference for a reader 
whether it’s broken into parts or whether they scroll through one 
well-organized longer piece? Personally, I don’t have an opinion on 
which of those we do, just flagging that we have those options and have 
used the former (multi-parts) in the past.

I really like the examples woven throughout. I suggest bringing a few 
sentences about those examples and their corresponding substantive 
questions up to the intro and background section. I think some readers 
might not necessarily link the general description of a paper trail and 
a document collection to their work, and therefore might miss that this 
blogpost is for them. A few more details earlier will help hook those 
folks, I think.

Alternatively or additionally, the first examples section could be the 
blurb that displays initially with the option to click to read the full 
post.

I wondered if the “project structure” section might make more sense 
earlier, right after the intro and background and before “sample, 
review, label”?

I think the end of the first paragraph of “sample, review, label” 
could use one more sentence providing an example of what “this is the 
labeling step” means/looks like.

I would also move up this sentence “Each data processing step is 
framed as a classification problem, and the classification tasks are 
well-suited to machine learning solutions.” Which I think provides a 
really clear framing for the rest of the post. In particular, I think 
readers should get to that sentence before “ by sampling just records 
for which our ML classifier scores between .4 and .6.”

And lastly, I think the Boston PD example in the section “Data 
extraction from segmented documents” could benefit from an image of a 
doc (perhaps annotated to really highlight the point you’re making 
about how many places in the doc you had to look for the right content).


In the “Introduction and background” section, I might suggest including a
screenshot of a document with information we’d like to extract and classify.
Maybe it’s a side-by-side spread: the document in its original form and then
the same document with some rectangles showing where information of interest is
on the page? I realize that this might be difficult given
privacy/confidentiality concerns and document content

In the “Designing a classifier: labels” section, I might suggest including a
screenshot of an example spreadsheet, like you suggest in the first paragraph.
Doing this would probably be most useful to someone who has limited experience
hand labeling data or prepping data for someone else to hand label

I love all of the images with the bounding boxes drawn on them! They are so
wonderful and helpful!

This is not important and please feel free to ignore it, but sometimes there is
whitespace around “=“ sometimes there is not. I also note that “=“ is used for
assignment in the x_overlap function, but <- is used everywhere else

suggested wording for the UW-CHR description:

At the other end of the spectrum, the University of Washington Center for
> Human Rights had sued under the FOIA
> <https://jsis.washington.edu/humanrights/2018/09/21/uwchr-sues-dhs-ice-cbp/>
> for every form I-213 (recording apprehensions of people) produced by ICE or
> CBP in the Washington area for a number of years as part of the Center's Human
> Rights at Home
> <https://jsis.washington.edu/humanrights/projects/human-rights-at-home/>
> research regarding immigrant rights.
>

