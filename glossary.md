# Glossary

Plain definitions, in alphabetical order.

**AI agent.** An AI that can take actions, such as searching or using tools, not
just reply.

**API (application programming interface).** A way for one program to ask another
to do something. On the web, that is usually a set of URLs your server answers.

**API key.** A secret password that lets your app use a service. Never share it or
put it in public code.

**Authentication.** Proving who someone is, usually by signing in.

**Authorization.** What a signed-in person is allowed to do.

**Backend.** The part of your app that runs on a server: the rules, the API, and
the database connection. Visitors do not download this code.

**Branch.** A separate copy of your project where you make changes without touching
the main version.

**CI (continuous integration).** Automatic checks that run on every change, such as
tests and builds.

**Client.** The program that asks, usually the person's browser.

**Commit.** A saved snapshot of your project with a note about what changed.

**Component.** A reusable piece of a page, such as a button, a form, or a card.

**Context.** The information an AI needs about your situation to give a good answer.

**Context window.** How much text an AI can read at once.

**Cookie.** A small value a site asks the browser to store and send back on later
visits. A session cookie is how a website remembers that you signed in.

**CORS (cross-origin resource sharing).** A browser rule about whether a page on
one site may call an API on another site. It is not a login system.

**CSS (cascading style sheets).** The language that controls how a page looks:
color, type, spacing, and layout.

**Database.** Where your app stores facts that must survive a refresh, such as
accounts and orders.

**Deploy.** Putting your app online.

**Endpoint.** One URL on your API that does one job, such as creating an order.

**Environment variable.** A setting, often a secret, stored outside your code. On
your computer they usually live in a `.env` file.

**Framework.** A kit of decisions and tools for building an app, so you are not
assembling every piece yourself.

**Frontend.** The part of your app that runs in the browser: what people see and
click.

**Full stack.** The frontend, the backend, and the database, treated as one
product.

**Git.** The tool that keeps your project's snapshots, so you can undo changes.

**Handler.** The function that runs when something happens. In the browser that
is a click or a submit. On the server it is one API request.

**HTML (hypertext markup language).** The language that marks up a page: headings,
paragraphs, links, forms, and buttons.

**HTTP (hypertext transfer protocol).** The rules a browser and a server use to
request and respond.

**HTTPS.** HTTP with encryption, so the trip between browser and server is not
readable on the network. The lock in the address bar.

**Index.** A searchable copy of your content, split into small pieces. In a
database, an index is also a shortcut that makes a lookup faster.

**JavaScript.** The language browsers run to make pages respond to people. With
Node.js, the same language can run on a server.

**JSON (JavaScript object notation).** A text format for structured data. APIs
usually send JSON back and forth.

**MCP (Model Context Protocol).** A standard way to plug outside information and
tools into AI apps. An *MCP server* provides them.

**Merge.** Accepting a pull request into the main version.

**Middleware.** A function that runs before a backend handler, such as checking
that the caller is signed in.

**Migration.** A saved change to the shape of a database, stored with the code so
every environment can apply the same change.

**n8n.** A visual tool for building automations and AI assistants by connecting
boxes.

**Node.js.** JavaScript running on a server, outside the browser.

**ORM (object-relational mapper).** A library that reads and writes database rows
from your programming language, with the SQL kept in one place.

**Persistent context.** Information your AI can reach every time, in every tool,
without you pasting it in.

**Preview.** A private online copy of your app for testing a change before it goes
live.

**Production.** The live version of your app that real people use.

**Pull request (PR).** A request to add a branch's changes to the main version,
showing exactly what changed.

**RAG (retrieval augmented generation).** Letting an AI look things up in your
content before it answers.

**REST.** A common API style: a URL names a thing, and the HTTP method says
whether you are reading it or changing it.

**Server.** A computer that stays on and answers requests. Your host runs yours.

**Session.** The server's record that a browser has already signed in.

**Skill.** An instruction file that teaches an AI coding tool how to do a task.

**SQL (structured query language).** The language used to read and write a
relational database such as Postgres.

**Test.** A small automatic check that your code still does what it should.

**TypeScript.** JavaScript with types that name the shape of your data. It
compiles to JavaScript before a browser runs it.
