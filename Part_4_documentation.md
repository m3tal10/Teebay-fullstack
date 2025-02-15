## Below are the main GitHub repositories of the Frontend and the Backend:
- **FRONTEND:** https://github.com/m3tal10/teebay-fe
- **BACKEND:** https://github.com/m3tal10/teebay


## Challenges Faced and Solutions Implemented

1.  **Tech Stack:**

- **Issue:** The tech stack was totally unfamiliar to me. I have used GraphQl for the first time in my life. As the whole assignment was GraphQl related it was very difficult for me to complete within the given timeframe.
- **Solution:** With prior experience in NodeJs and ReactJs, I was initially inclined towards it. However, since GraphQl and Apollo server were specified, I explored their documentation and some YouTube videos. The documentation was really fine, though I was a beginner it took me very little time to start understanding the workflow.

2.  **Time management:**
- **Issue:** Since I have a 9-6 job and an unfamiliar tech stack. I needed to allocate my time to the Job, Studies, new stack learning, and coding the project.  It was really difficult for me to make time for this.
- **Solution:** It looked so tough to me in the beginning but I spend the whole Friday (14hrs) giving my time to the project. As I'm a fast learner, this helped me to adapt to the new stack quickly and in a day I've completed most of the coding task.

3.  **Implementing Database Design:**

- **Issue:** The business logic seemed simple to me as I can handle relational logic pretty well. So, I faced no issue.
- **Solution:** Leveraging my prior database design experience. I formulated a structured schema encompassing four crucial tables: User, Product, ProductRent, and ProductBuy. As this is a complex design, like users can have one-to-many relationships with products and products can also be bought/rent by multiple users. So, this complexity was needed to be addressed. That is why I created two join table named ProductRent and ProductBuy. These tables tracked the product-user buy/rent relationships. A product can be rent multiple times but not while it is on rent. So, I implemented a logic where I create a ProductRent entry each time a user rents a product. And everytime, before creating the entry, I check if the product is already booked for rent for the given time and revoke the entry. As for the product buy also, If a product is up for rent in a future time, I've revoked the buy functionality for that specific product.
- For the dashboard, I've listed some queries where a user can see the products they have purchased and the history of the products they have rented/lent.

4.  **Understanding Workflow:**

- **Issue:** Grasping the workflows of GraphQL, and Apollo Server.
- **Solution:** As a newcomer to GraphQL, I embarked on a thorough learning journey. I extensively relied on tutorials, documentation, and online resources to comprehend the synergy among Node.js, Prisma, GraphQL, and Apollo Server. This self-directed learning approach allowed me to understand how these technologies collaborate seamlessly and enabled me to implement them effectively in the project.

5.  **Implementing Apollo Cache:**
- **Issue**: Optimizing data retrieval and UI updates using Apollo Client's cache.
- **Solution:** Leveraging Apollo Client's cache mechanism, I optimized data retrieval and UI updates. I employed various strategies to handle UI state updates. I used cache modification once a user added or deleted a product. At firs,t I was re-fetching everytime, but this seemed inefficient to me and I incorporated cache modification once users delete/add a product.
- though there was a lot of scopes to apply this technique(such as, on product rent, on product buy, etc), due to time constraints I could not implement it everywhere. I've only implemented this in the add/delete product.

6.  **Implementation of error handling:**

- **Issue**: As I've experienced in REST architecture, I was really accustomed to handling errors via HTTP error codes and global error handling. However, Graphql had some limitations regarding error handling like REST architecture.
- **Solution:** Initially, I faced confusion regarding implementing error handling. Relying on the GraphQl documentation, I initially used send errors as a data technique but soon I came to know about its limitations. Then I found out about global error formatting and then I've implemented error handling using in build apollo errorFromatting. However I am still not happy with the error handling in GraphQl.

This was a great learning journey and after this journey, I became more confident in my adaptability skills. I think I can solve any problem regarding anything.
