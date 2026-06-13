An librarie to manage data files.
It's can use, today, only JSON but, protected for KeyErrors!
It's have only class "JSONPremium", this class is usable on with blocks!
Example:
"from filedata import *
 
 with json.JSONPremium(file="MyJSONExample.json", mode="rb+", encode="utf-8") as f: # Yea, it's can manage encodingsin binary
     print(f.getObject("user")) # f.read()["user"], vicete
     f.write("patata", 67) # still not saved... now you see
     f.save() # Now it's saved
     print(f.getAll()) # all, in dict, { "user": "vicete", "patata": 67, # here is we write }
     print(f.getObject("messi")) # with json.load() included, this launch an KeyError. Here, only return None
     "
MyJSONExample:
"{
    "user": "vicete",
    "patata": 67, # here is we write
}"
It's incredible, yes?

