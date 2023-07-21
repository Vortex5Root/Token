# Documentation

## Introduction

This documentation provides an overview of the Python code for the Token Manager. The Token Manager is responsible for managing user permissions and access rights based on the provided tokens. The code includes classes for Regedit, Group, LoginException, and Token, each serving a specific purpose in the Token management process.

## Installation
```bash
poetry add git+https://github.com/Vortex5Root/Token.git
```

## How to use

### Regedit 

- The Regedit class is responsible for building the registry configuration based on the provided parameters.

```python
reg_manager = Regedit()
reg_config = reg_manager.build_regconfig(dir, action, id_)
```

### Group

- The Group class allows you to load and manage user groups from the configuration file.

```python
group = Group("group_name")
group.load()
```

### LoginException

- The LoginException class is used to raise exceptions related to login errors.

```python
try:
   user = login("<token>")
except LoginException as e:
    print(e.message)
```

### Token

- The Token class represents a user token and provides methods to check user permissions and access rights.

```python
user = Token("<token>")
user.login()
```

- Check if a user is allowed to perform a certain action on a specific directory with the provided ID.

```python
if user.is_allow(dir, action, id) -> bool:
    print("user allowed")
else:
    print("user not allowed") 
```

## Conclusion

This Python code for the Token Manager provides a flexible and efficient way to manage user permissions and access rights. By using the Token Manager, you can easily control user access to specific resources within your system. The code is well-structured and customizable, allowing you to integrate it seamlessly into your existing applications or projects.
