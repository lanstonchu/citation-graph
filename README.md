Project Title: **Automatic Generation of Academic Citation Graph**

Also on: [WordPress][1]

Source Code and Data: [GitHub repository][2]

In certain fields of academic studies (e.g. Deep Learning), academic papers are released in a much faster speed than people in the field read them (although it is certainly true in all fields). As researchers, we know that we want to know how the papers fit into the whole academic conversation, so it would be nice if we can automatically generate an academic paper citation graph, and immediately tell which one cites which.

I created a tool for you *homo academicus* to automatically create the said citation graph for any paper. This should be helpful for researchers to catch up on the trend of a rapidly changing field.

First, if you are using Mendeley (or any other Reference Management Software), export your papers as a **.bib** file which should include the arXiv ID and issue year information. Then, use Mathematica to run the code. It will take you to the [Astrophysics Data System of Harvard][3] and find out the list of reference for each paper. Finally, a citation graph will be drawn with the help of Wolfram Language.

See the below example. Here, I’ve selected a list of papers in Mendeley about adversarial examples (published in the past five years), and I want to know how they are related to each other (“citationally”).

![Image 1 - Mendeley][4]

Click **File->Export** and then save the papers’ metadata as **My Collection.bib**.

Use Mathematica to run the code in **1 – arxivID extraction from bib.nb**, and the code will execute the saving of a new file **arXivIDandYearLists.mx** which stores the respective arXiv ID and issue year of the papers. Then run **2 – Citation Graph.nb** in Mathematica again. This is the end product:

![Image 2 - Citation Tree][5]

You can see that *Transferability in Machine Learning: from Phenomena to Black-Box Attacks using Adversarial Samples (Papernot et. al. 2016)* and *Explaining and harnessing adversarial examples (Goodfellow et. al. 2014)* are the most influential nodes among those selected papers (i.e. most cited).

If you want to add more information (say author) to the vertex labels, you can modify **1 – arxivID extraction from bib.nb** or **2 – Citation Graph.nb** to do that. You just need to change a few lines so I am not going to be verbose here.

Enjoy.

[1]: https://lanstonchu.wordpress.com/2019/08/20/automatic-generation-of-academic-citation-graph/
[2]: https://github.com/lanstonchu/citation-graph
[3]: https://ui.adsabs.harvard.edu/
[4]: https://raw.githubusercontent.com/lanstonchu/citation-graph/master/Mendeley.png
[5]: https://raw.githubusercontent.com/lanstonchu/citation-graph/master/citation%20graph.jpg
