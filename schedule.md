# Schedule

It happens a lot that you want to run a task every few minutes/days or on a specific time of the day. For this purpose, you can use `bot.schedule` which is an instance of [`node-schedule`](https://github.com/node-schedule/node-schedule).

Example:

```javascript
  // run the job at 9:30 everyday
  bot.schedule.scheduleJob('0 30 9 * * *', (job, done) => {
    unirest.get('http://api.theysaidso.com/qod.json').end(response => {
      if (!response.body.contents) {
        bot.log.error('[quote]', response.body);
        return;
      }

      let quote = response.body.contents.quotes[0];
      let message = `*Quote of the day*: ${quote.quote} _–${quote.author}_`;
      bot.sendMessage(channel, message);

      done();
    });
  });
```

This is [`dude-quote`](https://github.com/dudeee/dude-quote), a plugin for sending quotes to your Slack team.