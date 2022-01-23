<div align=center>
  <h1>Permissions</h1>
</div>

# Permissions


## Read

- The user can only read the file.
- The code is 4.

## Write

- The user can only write to the file.
- The code is 2.

## Execute

- The user can only execute the file.
- The code is 1.

- The code for no permissions is 0.

## Groups


- There are three groups
              - User
              - Group
              - Others


## User

- To change the user of the file, we can use command `chown` which means change owner.
- This command needs root priviledges.
- To change the owner to root for a file, run

```zsh
$   sudo chown root <file-name>
```
