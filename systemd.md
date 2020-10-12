1. Put your application binary to /usr/bin
2.  Add your service file (see template below) in /usr/lib/systemd/system
```
    [Unit]
    Description=mytest Application
    
    [Service]
    Type=notify
    User=nobody
    Group=nobody
    ExecStart=/usr/bin/mytest.app
    
    [Install]
    WantedBy=multi-user.target
```
3. Activate your service: 
```
    [jack@m3:~]# systemctl enable mytest.app
```

Typically you use this directly in your main function:
```
    #include <daemone/daemonize.hpp>
    int main(int argc, char *argv[])
    {
    tsd::common::daemon::IDaemon *daemon = common::daemon::daemonize(argc, argv);
    // initialize application, start application threads
    // Signal that your application is ready. Will return when you have to shut down.
    int ret = daemon->exec();
    // shutdown application
    return ret;
    }
```
