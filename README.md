# SearchToChart
Problem: User search keywords (search behavior), regardless of level of automation and supervising of search algorythm, needs to be analysed from time to time to know what content needs to be pushed (or may perform better), what is more accessible/interesing among users.
Monitoring of >100 keywords is too hard to do manually by just scrolling through the data table. This data needed to be presented in a more readable and transparent fashion, like a big word cloud. The main opportunity will be, that words that are similar by their context (ex. birthday <-> present) or meaning (marriage <-> wedding) may be situated close to each other in the visualization. 

Solution: There's a good NLP tool called word2vec, which also provides trained model (on a big sample of google news), where a word is represented by 300-dimension vector. While it'd be easy just to apply a clustering to the keywords, we cannot show 300 dimension data on a chart. t-SNE is the most common non-linear dimensionality reduction method, which suited the needs: the reduction can be approximate, must not be costly and the results must be interpretable. In the end, results are visualized by plotly, but there's a link to tableau online chart of the result 

Further Steps: The method works fine on 1 word searches. For 2 or more word combinations in a search query, additional tools must be used: doc2vec.

The code to make all this happen is presented in the ipynb notebook. You can also download and open the .html file to see the output chart.
