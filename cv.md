# Artyom Gorushkin

## Contacts

[gitHub](https://github.com/gorushkin) | [linkedin](https://www.linkedin.com/in/gorushkin/) | [telegram](http://t.me/artyomgorushkin)

## About Me

I like learning.

## Code samples

```javascript
    .get(
      '/tasks/:id/edit',
      { name: 'taskEdit', preValidation: app.authenticate },
      async (req, reply) => {
        const [task, users, statuses, labels] = await Promise.all([
          app.objection.models.task.query().findById(req.params.id).withGraphJoined('labels'),
          app.objection.models.user.query(),
          app.objection.models.status.query(),
          app.objection.models.label.query(),
        ]);
        reply.render('tasks/edit', {
          task,
          users,
          statuses,
          labels,
        });
        return reply;
      },
    )
```

## Portfolio

* Chat - [GitHub](https://github.com/gorushkin/frontend-project-lvl4), [web-project](https://polar-thicket-77600.herokuapp.com/)

* Task Manager - [GitHub](https://github.com/gorushkin/taskmanager), [web-project](https://taskmanager-gav.herokuapp.com/)

* Veles - [GitHub](https://github.com/gorushkin/veles), [web-project](https://gorushkin.github.io/veles/)

## My skills

* HTML5, CSS3, SCSS
* БЭМ
* JavaScript(ES6+)
* React, React (hooks);
* Redux, Redux Toolkit, Forms;
* Express
* Fastify
* TDD, JEST
* Git, Github, Github Action;
* Babel, Webpack, Gulp;
* Node.JS
* Figma, Photoshop, Avocode

## Experience

* 2019-2020 Верстальщик - кроссбраузерная, адаптивная верстка
* 2020 - настоящее время - frontend разрабтчик. Занимаюсь интерфейсами