## Overview
**Search UI**, [Attivio's](http://www.attivio.com/) out-of-the-box search interface, provides an interactive learning tool for exploring your Attivio index and client API functionality. **Search UI**, and it's underlying library, [SUIT](https://github.com/attivio/suit), can also be used to rapidly prototype an Attivio Search Application on top of any data set. 

## Installation and Deployment
Search UI has two deployment options:
* [Embedded](https://answers.attivio.com/display/extranet55/Search+UI+Download) - deploy as a module making it available from the Attivio Admin UI
* [Stand-alone](https://answers.attivio.com/display/extranet55/Search+UI+-+Deploying+to+Tomcat)  - deploy to an external web server such as Tomcat

## Security
Search UI can be configured to require users to log in. The options vary depending on your deployment type.

| Deployment Type | Security Options |
| --------------- | ---------------- |
| Embedded (within Attivio) | <ul><li>[Active Directory](https://answers.attivio.com/display/extranet55/Active+Directory+Authentication+Provider)</li><li>[XML](https://answers.attivio.com/display/extranet55/XML+Authentication+Provider)</li></ul> |
| Stand-alone (i.e. Tomcat)	 | <ul><li>[SSO](https://answers.attivio.com/display/extranet55/Search+UI+-+Configuring+SSO)</li><li>XML</li></ul> |

Depending on the security option, users will either be presented with Attivio login form or one presented by the Identity Provider.

<img src="https://github.com/attivio/search-ui/blob/master/images/login-attivio.png?raw=true" alt="Attivio Login Form" width="45%" /> <img src="https://github.com/attivio/search-ui/blob/master/images/login-okta.png?raw=true" alt="Okta Login Form" width="45%" />

## Cognitive Search
After logging in, if required, Search UI opens to its "Landing Page." The landing page provides a clean UI to start your search investigation.

<img src="https://github.com/attivio/search-ui/blob/master/images/landing-page.png?raw=true" alt="Landing Page" width="100%" />

**On this page you can:**
* [Ask a question](#question)
* Click on [Insights](#insights) to better understand your data

<a name="question"></a>
## Ask a Question

Whether you want to ask a free-form question or use our [Advanced Query Language (AQL)](https://answers.attivio.com/display/extranet55/Advanced+Query+Language) in this page you can get to the information you need. Hit **ENTER** or click **Go** to see the results.

<img src="https://github.com/attivio/search-ui/blob/master/images/italy.png?raw=true" alt="Results" width="100%" />

Following are some features of the results page:

| Feature | Description |
| ------- | ----------- |
| Logged-in user (Attivio Administrator in our case) <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/username.png?raw=true" alt="Username" align="center" /> | The name of the logged-in user appears in the upper right corner, if available. Otherwise, the username is displayed with an option to log out. |
| Simple or Advanced Query Language <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/query-language.png?raw=true" alt="Query Language" align="center" /> | Select between Attivio's [Simple Query Language\(https://answers.attivio.com/display/extranet55/Simple+Query+Language) or the [Advanced Query Language](https://answers.attivio.com/display/extranet55/Advanced+Query+Language). |
| Search Box <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/search box.png?raw=true" alt="Search Box" align="center" />| Enter the text of your query.  For the [Simple Query Language](https://answers.attivio.com/display/extranet55/Simple+Query+Language), enter a keyword or a field:keyword pair.  The string \*:\* retrieves all documents in all tables.  You can paste in more complex queries written in the [Advanced Query Language](https://answers.attivio.com/display/extranet55/Advanced+Query+Language), such as those demonstrated in the [Quick Start Tutorial](https://answers.attivio.com/display/extranet55/Quick+Start+Tutorial). |
| Facet Filters <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/facets.png?raw=true" alt="Facets" align="center" /> | The left column of the display is devoted to facet controls.  Each one summarizes opportunities to "drill down" on the set of current results to narrow the search. |
| Applied Facets <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/applied-facet.png?raw=true" alt="Applied Facet" align="center" /> | Under the header, the facet filters that have been applied to the search are displayed. Each item can be individually removed to widen the result set as needed. |
| Sort Control <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/sort-by.png?raw=true" alt="Sort By" align="center" /> | The sort control reorders the result items. You can sort by relevancy and select which [relevancy model](https://answers.attivio.com/display/extranet55/Machine+Learning+Relevancy) to use, or by any sortable field in the schema. See [Sorting Results](https://answers.attivio.com/display/extranet55/Sorting+Results) for more information. |
| Relevancy Model <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/relevancy.png?raw=true" alt="Relevancy" align="center" /> | If you choose Relevancy in the Sort Control, you can choose the Relevancy Model to use. See [Machine Learning Relevancy](https://answers.attivio.com/display/extranettrunk/Machine+Learning+Relevancy) for more information. |
| Paging Controls <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/pagination.png?raw=true" alt="Pagination" align="center" /> | The paging controls let you page through the search results conveniently. |
| Matching Documents | The right column of this page is devoted to the display of matching documents. <ul><li>If there is a [Thumbnail Image](https://answers.attivio.com/display/extranet55/Thumbnail+and+Preview+Images) available, it will be displayed to the left of the document (like the flag images in the Quick Start Tutorial.)</li><li>The title of the document is often a hyperlink to the actual document or web page.</li><li>Search UI is preconfigured to show the **table** value of each matching document next to the result number.</li><li>By default, Search UI displays the document teaser, with matching terms [highlighted](https://answers.attivio.com/display/extranet55/Field+Expressions).<ul><li>Items that matched the query are shown in **bold** face.</li><li>[Scoped entities](https://answers.attivio.com/display/extranet55/Scope+Search) are color-coded:<ul><li>People: Yellow</li><li>Locations: Blue</li><li>Companies: Red</li></ul></li><li>[Key phrases](https://answers.attivio.com/display/extranet55/Key-Phrase+Extraction): Green</li><li>[Entity Sentiment](https://answers.attivio.com/display/extranet55/Using+Entity+Sentiment) is indicated by red and green plus or minus icons.</li></ul></li><li>Document Details consist of fields and values. Note that you can temporarily display all fields by setting the **Details** button next to the Sort Control to **On**.</li><li>The **Tags** field is a [Real Time Field](https://answers.attivio.com/display/extranet55/Real-Time+Updates) configured in the [Schema](https://answers.attivio.com/display/extranet55/Configure+the+Attivio+Schema). It lets you add labels to each document directly from the Results Page. These labels can then be collected into a new facet to assist in subsequent searches.</li></ul> |  
| User Rating <br/> <img src="https://github.com/attivio/search-ui/blob/master/images/stars.png?raw=true" alt="Rating" align="center" /> | A user can provide a rating for a document that can be used as a signal when using Machine Learning to create a relevancy model. See [Machine Learning Relevancy](https://answers.attivio.com/display/extranet55/Machine+Learning+Relevancy) for more information. |
| Show 360&deg; View | You can choose to see a  360&deg; view of a document to better understand the document and how it relates to other documents using our Insights Graph. |
