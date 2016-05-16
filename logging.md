# Logging

You need logging to be able to debug/monitor your process later. We use [`winston`](https://github.com/winstonjs/winston) for that, pre-configured and ready to use!

Example:

```javascript
bot.log.info('[quote] requesting quote from API');
bot.log.error('[quote] API is not responding!');
bot.log.error('[quote] API rate limit reached!');
bot.log.warn('[permissions]', `Did not allow ${user} to do ${action}`);
bot.log.silly('[permissions]', `Checking ${user} for eligibility to issue command ${command}`);
```

It's a good practice to tag your plugin/task name before the log to increase readability