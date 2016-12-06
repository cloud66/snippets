## weave_scope

If you want to install weavescope on your Docker stack use the following last_thing hook.

production: # Environment or your choice
  last_thing: # Importent to run the weavescope hook as the last thing during server deployment
    - snippet: cloud66/weave_scope # our weavescope snippet
      target: docker
      sudo: true
      execute: true
      run_on: all_servers #make sure weave scope is running on all servers and communicate to each other
  
Warning: Weavescope will run on port 4040 which is not exposed to the outside world. If you want to access the UI change your firewall settings allowing traffic to port 4040. Make sure only you can access weavescope from your ip-address. With weavescope you can control all your running process and excute inside running containers. Take good care of those powers!
