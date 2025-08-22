
<engineersIntroduction>
Hi, I am Nikolaj Farbod and i build end-end Full Stack GenAI applications with the most up to date methodologies of using these amazing invention in a Softare environment!

I was overwhelemed of reading many websites on a research project i was doing so i decided to build my Own FullStack Researcher companion, and below is a brief explanation. 
</engineersIntroduction>

<ProjectOutline>
The User Story: When a user discovers an interesting article online, they copy the URL and paste it
  into the dashboard. The FastAPI backend uses BeautifulSoup to scrape the webpage, extracting the title
   and main content while filtering out navigation, ads, and other non-essential elements. This clean
  content is saved to SQLite via SQLAlchemy ORM with user association through JWT authentication, while
  simultaneously being processed by the embedding service that chunks the text into 800-character
  overlapping segments and converts each chunk into vector embeddings using OpenAI's
  text-embedding-3-small model, storing them in ChromaDB with metadata linking back to the original
  article.

  The RAG Magic: When users search or ask questions, their query is embedded using the same model and
  compared against all their article chunks using cosine similarity in ChromaDB. The system retrieves
  the most relevant chunks, deduplicates by article ID, and for Q&A functionality, uses an adaptive
  threshold system to ensure quality context. The selected content chunks are assembled into a
  comprehensive context and fed to an OpenAI Foundation model along with the user's question, generating detailed
  answers that cite specific source articles. The frontend displays these responses with similarity
  scores and source references, creating a personalized AI research assistant that learns from the
  user's curated knowledge base. This seamless integration of web scraping, vector search, and
  generative AI transforms a simple URL submission into a queryable, intelligent knowledge repository.

Backend

* FastAPI: Python web framework
* SQLite: Database for user accounts and article metadata
* SQLAlchemy: ORM for database operations
* JWT: Authentication using JSON Web Tokens with python-jose
* OpenAI API: For question-answering functionality
* ChromaDB: Vector database for embeddings storage and similarity search
* Scikit-learn: For machine learning utilities
* BeautifulSoup: For web scraping and content extraction
Frontend

* Next.js 15: React framework with App Router and Turbopack
* NextAuth.js: Authentication
* Tailwind CSS 4: Styling
* TypeScript: Type safety
* Axios: HTTP client for API requests



Link to the source code : https://github.com/FarbodDadkhah/DumpedKnowledge
</ProjectOutline>
