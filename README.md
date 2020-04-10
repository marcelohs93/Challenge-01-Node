<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Challenge 01: Node.js Concepts
</h3>
&nbsp;


## 🚀 About this challenge

I created on this challenge an application to training what I have learned so far about Node.js.

This is an application to store repositories in my portfolio, it should be able to do creation, listing, update and delete of the repositories, and also allow the repositories to get "likes".

### 💻 Application routes

- **`POST /repositories`**: The route receive `title`,` url` and `techs` within the body of the request, the URL being the link to the github of this repository. When registering a new project, it is stored inside an object in the following format: `{id:" uuid ", title: 'Desafio Node.js', url: 'http: //github.com / ...' , techs: ["Node.js", "..."], likes: 0} `;

- **`GET /repositories`**: Route that lists all repositories;

- **`PUT /repositories/:id`**: The route  only change the `title`,` url` and `techs` of the repository that has the` id` equal to the `id` present in the parameters of the route;

- **`DELETE /repositories/:id`**: The route delete the repository with the `id` present in the route parameters;

- **`POST /repositories/:id/like`**: The route increase the number of likes from the specific repository chosen through the `id` present in the route parameters, at each call of this route, the number of likes is increased by 1;

### 🔎 Test specification

- **`should be able to create a new repository`**: For this test to pass, your application must allow a repository to be created, and return a json with the created project.

- **`should be able to list the repositories`**: For this test to pass, your application must allow an array to be returned with all the repositories that have been created so far.

- **`should be able to update repository`**: For this test to pass, your application must allow only the `url`,` title` and `techs` fields to be changed.

- **`should not be able to update a repository that does not exist`**: For this test to pass, you must validate in your update route whether the repository id sent by the url exists or not. If not, return an error with status `400`.

- **`should not be able to update repository likes manually`**: In order for this test to pass, you must not allow your update route to directly change the likes of this repository, maintaining the same number of likes that the repository already had before the update. That's because the only place that should update this information is the route responsible for increasing the number of likes.

- **`should be able to delete the repository`**: For this test to pass, you must allow your delete route to delete a project, and when deleting it, it returns an empty response, with status `204`.

- **`should not be able to delete a repository that does not exist`**: For this test to pass, you must validate on your delete route whether the repository id sent by the url exists or not. If not, return an error with status `400`.

- **`should be able to give a like to the repository`**: For this test to pass, your application must allow a repository with the given id to receive likes. The likes value must be increased by 1 for each request, and as a result, return a json containing the repository with the number of likes updated.

- **`should not be able to like a repository that does not exist`**: For this test to pass, you must validate on your like route whether the repository id sent by the url exists or not. If not, return an error with status `400`.


---

Feito com 💜 by Marcelohs93