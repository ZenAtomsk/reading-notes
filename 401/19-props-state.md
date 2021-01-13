# Props and State

## Review, Research, and Discussion

**Does a deployed React application require a server?**

- Yes.

**Why do we prefer to test a React application at the behavior rather than the unit level?**

- To make sure things work individually as without a scaffold holding up a problem function.

**What does npm run build do?**

- runs the "build" specified in json package

**Describe the actual composition / architecture of a React application** [Source](https://saurabhshah23.medium.com/react-js-architecture-features-folder-structure-design-pattern-70b7b9103f22)

1. App title + Favicon
2. Router (navigation)
3. Material UI
4. Backend — Data connectivity (AXIOS for REST API, SDK integration)
5. Redux + Thunk
6. Multi-environment setup (create deployable builds pointing to specific Database environments using environment variables, without having all environment config bundled in code.)
7. Internationalization
8. Unit testing.
9. Deployment and hosting (Firebase hosting)
10. ES Lint
11. Design Pattern (Container-View)
12. CI for continuous integration.

## Vocabulary

- [BDD](https://www.agilealliance.org/glossary/bdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'bdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1)) -Behavior Driven Development - is a synthesis and refinement of practices stemming from Test Driven Development and Acceptance Test Driven Development

- [Acceptance Tests](https://www.agilealliance.org/glossary/atdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'acceptance*20test~'atdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1)) involves team members with different perspectives collaborating to write acceptance tests in advance of implementing the corresponding functionality.

- [mounting](https://en.wikipedia.org/wiki/Mount_(computing)) - Mounting is a process by which the operating system makes files and directories on a storage device (such as hard drive, CD-ROM, or network share) available for users to access via the computer's file system

- [build](https://reactjs.org/docs/create-a-new-react-app.html) - lets you take advantage of a vast ecosystem of third-party packages, and easily install or update them.
