\# SaaS products: a strained relationship + QuickBooks + Python/Flask



As a small, non-technical team, the search was on for a product to help them complete their accounting properly. Several critical factors determined what kind of app they needed for their expense tracking. It had to:

work with their specific accounting structure,

be easy to onboard new, non-technical users,

be fully accessible for the accountant

and finally, as a start-up, they needed it to be relatively inexpensive.

‍Sam started by trialing out-of-the-box receipt trackers and uploaders, but many of them only properly catered to the single company or businessperson and didn’t offer the functionality for splitting across LLCs, whilst also recording it to the umbrella company too. The ones that did were overladen with unnecessary, often costly, extra features, and required too much work to refine into an MVP that suited Red Roots’ needs.



They found solutions to some of their problems with Quickbooks, which had the added benefit of a web and mobile app, and offered the kind of data enrichment they were looking for. Once they onboarded some of their contractors, however, they found that the UX required these users to have detailed knowledge of Red Roots’ accounting system in order to input those receipts correctly. This made the margin for error too large for an app that would have many non-technical users, who were unfamiliar with the company’s complex expenses system.

‍This time they were wasting adjusting an already expensive product - or even training non-technical construction contractors in their accounting structure - was much better spent working from scratch to build their own.

“Premade receipt trackers just weren’t cutting it, they were either crazy expensive, overloaded with unnecessary features, or would require way too much time to adjust to our needs” - Sam Stewart, Red Roots

‍

The Build: Retool Mobile Receipt Tracking App

The final mobile app is streamlined and simple to use: a single screen with text inputs, several dropdowns, and an image uploader. The app contains only the specific fields needed for Red Roots accounting system, with appropriate data validation to reduce margins for error.

(https://github.com/realdev71/Webapp-Quickbooks-Flask-React/blob/master/images/1.jpg?raw=true)

When the user opens the app (which can be saved to the phone home screen), they are guided through various data input steps. Retool allowed them to create an app optimized for user experience as well as accounting organization:‍

Cascading logic helps to organize the receipts and their corresponding data. Each selection determines the dropdown options for the next: meaning that users no longer need to understand the inner workings of Red Roots’ accounting to process the receipt correctly.

These form options are generated from their main property database, so the app options will dynamically change based on database schema changes.

Once the form is filled, the user is invited to upload an image or take the photo directly from the camera. The upload process is seamless and has no superfluous or unnecessary features.

The components’ preconfigured data validation options, such as currencies, dates and more, are used to ensure accurate data is filled.

Finally, default values also make form filling as streamlined and user-friendly as possible: the ‘User entering receipt’ field is populated by default with the Retool global current\_user.fullName, the date defaults to the present day using the built-in ‘Moment’ library, and placeholder texts guide the user with expected data types. These were all simple to program in Retool in the right-hand inspector column.

(https://github.com/realdev71/Webapp-Quickbooks-Flask-React/blob/master/images/2.jpg?raw=true)

Internal apps with growth and flexibility potential

‍Sam was chuffed to find that Retool allowed extra flexibility with storage and subsequent platform costs, since it can integrate natively with a number of resources, APIs and databases. A real perk for Sam is that, should they decide to switch to another storage option, their receipt tracker app could migrate with them, and would just require reconnecting the queries to the new database.

“A key part of our decision to use Retool was the knowledge that any time and money invested in their internal infrastructure didn’t create any lock-in to a specific backend, and could adjust to our scaling needs.”

‍(https://github.com/realdev71/Webapp-Quickbooks-Flask-React/blob/master/images/3.jpg?raw=true)

Once the databases for their mobile app were set up and connected in Retool, it was quick and easy to develop a second read-only, web-based app that retrieved this data from both AirTable and the S3 bucket and presented it clearly, useful for business intelligence on expenses for the stakeholders. Here, the manager can drill down into expenses by category, and see exactly how a rental property is performing. With Sam, the Bold Tech team are currently developing a further tool to present this information with charts and analytics, to create a long-term, business intelligence infrastructure.

