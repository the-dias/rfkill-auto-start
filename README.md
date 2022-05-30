# rfkill-auto-start

## OS
 
 **Artix Linux ( no systemd )**

 **Use OpenRC**

 `sudo su`
 
 `cd /etc/init.d`
 
 `nvim unrfkill`
 
  ```
  #!/usr/bin/openrc-run

depend(){
        after bootmisc
}

start(){
        rfkill unblock all
}
  ```
  `:wq
  `
  
  
  Syntax may vary, you can check `nvim dbus`, but exit from nvim **only `:q!`**
  
  `rc-service unrfkill start` - for check working
  
  
  if working
  
  
  `rc-update add unrfkill start`
  
  
  `rc-status`
  
  `exit`
  
