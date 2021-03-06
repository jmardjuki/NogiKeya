# Serving the project "idol"  
Some one-key tools for saving time

## 1.Get official portraits  
***keyakizaka46⊿***  
`python get-keyaki-members-official-portraits.py`  

***nogizaka46⊿***  
`python get-nogi-members-official-portraits.py`  

Coding with python 2.7, standard library only, no additional module required.

## 2.Get member's blog list 
***nogizaka46⊿***  
`python get-nogi-members-all-blog-list.py`  

You can set the time limit, default is getting from the earlist blog.  
You can also set the specific member, just change the dict's key.  
List is stored with json format like the sample [nanami.json](https://github.com/nondanee/NogiKeya/blob/master/nanami.json) in this repo.  

Coding with python 2.7, standard library only, no additional module required.  

## 3.Download blog pages (async)
***nogizaka46⊿***  
`python3 force-get-blog-raw-page.py`  
Relying on the blog list gotten by prev script.  
Storing file structure is based on official website's php url definition,  
The directory named [hashimoto.nanami/](https://github.com/nondanee/NogiKeya/tree/master/nanami.hashimoto) in this repo is a sample.  

*BTW: I use these offline pages (after processing) to build a small blog-storing site by Github Pages in the other repo named [nondanee / onemoretime](https://github.com/nondanee/onemoretime).*   

Coding with python 3.4, upwards compatible, required "asyncio" and "aiohttp".  
**Using async to make requests, care with your ip address because of concurrent access**

## 4.Get all members' info (async)
***nogizaka46⊿***  
`python3 get-nogi-members-info.py`  
Get data from nogizaka members' introduction pages and generate a json file.  
*BTW: Urllist is now written in the script. It can also be created by function getlist()*  

Coding with python 3.4, upwards compatible, required "asyncio" and "aiohttp".  
**Using async to make requests, care with your ip address because of concurrent access**

Running-time test: 2.283793ms