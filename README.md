LangGraph built on the basis of Langchain's libraries that incorporates Gemini's generative AI to query and summarize the contents of a .PDF file

Utilises Langchain's PyPDF library to read given pdf, Text splitter to divide it into chunks of defined sizes and FAISS as the vectorstore to store the embeddings generated by Gemini so as to perform similarity search.

Language model used is Gemini's 1.5 flash pro, which we integrate into our environment using an API key. We invoke it to summarize as well as generate responses for the user's queries based on file context.

The LangGraph has a TypedDict state schema, with notable inputs context (type list of docs) and query (type str), whose values are overriden at each node. There are four nodes, expand, search, summarize and generate, which allow us to dictate the workflow of execution and run two tasks simultaneously (ie, summarization and query execution).


In this particular example I have set up on Jupyter Notebook, I have used my university's Exam Form with my own credentials and requested it to return them in an organized manner, as well as summarize the contents of the whole page intrinsically, which it returns flawlessly.
