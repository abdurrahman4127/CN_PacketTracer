# <!-- diagram pic -->
# **Network Diagram** 
![Alt Text](network_diagram.png)


# <!-- the task i'm given -->
# **Task**
the task is to assign IP address to the hosts manually. 

**requirements:** 
- `router 0` and `router 1` share `10.0.0.0/8` ip address atboth their `se0/1/0` interface 
- at `gig0/0/0` interface of `router 0`, the network ishaving `11.0.0.1/8` ip address
- and at `gig0/0/0` interface of `router 1`, the network is having `12.0.0.1/8` ip address




# <!-- steps to follow -->
# **Steps**
## for both routers, 
1. go to the `configuration mode`
2. select the `interface`
3. provide `ip` and `subnet mask`
4. exit



#  <!-- commands for packettracer cli -->
# **Commands**:

## commands for Router 0:

### 1. go to the **configuration mode**:
- to go to the `configuration mode`, 
    - (i) we must go to the `user EXEC(ution) mode` 
    - (ii) then to the `privileged EXEC(ution) mode`
    - (iii) and then finally to the `configuration mode`


- (i) go to the **user EXEC(ution) mode**:

        --- System Configuration Dialog ---

        Would you like to enter the initial configuration dialog? [yes/no]:
    unless you wanna enter the initial configuration dialog, type ```no```; and then if you see router interface like this, then you're in the **user EXEC mode**:

        Router>	
    


- (ii) go to the **Privileged EXEC mode**:

    type ```enable``` to go to the Privileged EXEC mode. if you're in the Privileged EXEC mode, you should see `#` after your router's name:
        
        Router> enable
        Router#	

`
Router>	- User EXEC mode
Router#	- Privileged EXEC mode
Router(config)#	- Configuration mode (notice the # sign indicates this is accessible only at privileged EXEC mode)
Router(config-if)#	- Interface level within configuration mode
Router(config-router)#	- Routing engine level within configuration mode
Router(config-line)#	- Line level (vty, tty, async) within configuration mode
`
