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