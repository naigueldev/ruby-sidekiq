# Ruby Sidekiq

## Redis is needed

Linux installation:
```
sudo apt-get install redis
```

## Executing the process:

Terminal 1, run:
```
bundle exec sidekiq -r ./worker.rb
```

Terminal 2, run:
```
bundle exec irb -r ./worker.rb
```

and after run:

```
2.7.3 :001 > OurWorker.perform_async("easy")
```

```
2.7.3 :002 > OurWorker.perform_async("hard")
```

```
2.7.3 :003 > OurWorker.perform_async("super_hard")
```
