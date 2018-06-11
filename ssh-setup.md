In root folder, there needs to be a folder that stores all the ssh keys. By default it is invisible - hence the dot before the name.

Check if the folder exists: ``cd .ssh``

If you get a message "No such file or directory", run ``mkdir .ssh`` and go inside the folder you just made.

Create a file that will store the config ``touch config``

Create an SSH key ``ssh-keygen`` Set file name to the service name (eg github). You can ignore the passphrase options.

Your key will be saved in service-name.pub file.

Access the generated key ``cat service-name.pub``, copy the content and supply it to the service.

You now need to edit the config file. Open the file using your favourite editor (``nano config``) and add the service:

```
Host service-name.com
    IdentityFile ~/.ssh/service-name
```

(When you go to Service, use settings stored in file)
