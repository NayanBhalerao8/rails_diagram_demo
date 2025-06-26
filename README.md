# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
<pre> ## 🧭 Post Creation Flow ```mermaid sequenceDiagram participant U as User participant C as PostsController participant P as Post participant J as Job U->>C: Create new post (POST /posts) C->>P: Save post P->>J: Enqueue background job J-->>P: Process post (e.g., notify, index) ``` </pre>