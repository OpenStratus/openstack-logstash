
The files in this repo help use [logstash](http://logstash.net/) to aggregate and process OpenStack logs. 

In the example below, `agent.conf` is copied to `/etc/logstash` and `patterns` dir is copied to `/etc/logstash`.
You must include the default [grok-patterns](https://github.com/logstash/logstash/blob/master/patterns/grok-patterns)
in the same directory. Here is an example to start logstash with these patterns on each OpenStack node.

    java -Djava.library.path=/usr/share/logstash -jar /usr/share/logstash/logstash-1.1.5-monolithic.jar agent 
        -f /etc/logstash/agent.conf 
        --grok-patterns-path /etc/logstash/patterns


