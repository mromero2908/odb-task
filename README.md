# Oracle Database Tasks for VSC

## Overview

The goal of this extension is to simplify the ability to run scripts against your database connections. It works around the concept of having a config file in the root of your project with a list of all your connection details.

## Install

The extension is not currently published in the marketplace. To install, go to the releases within GitHub, and download the latest odb-task-*.vsix file. Then from the command line run the following:

```bash
code --install-extension odb-task-*.vsix
```

## Set up

1. Open your project
2. Create a file in your project root named `.build-oracle.json`
3. Update the contents per the below example
4. Reload Code just to make sure everything is detected

### Example config

```json
[
    {
        "targetName": "DEV",
        "connectionString": "user/password@XE"
    }
]
```

## Usage

Open the command palette and type `Compile with`. You will see two entries:

1. Compile with SQL*Plus
2. Compile with SQLcl

note: This extension doesn't ship with these binaries, so it assumes if you are running one or the other, the command is available on your system.

Choose the interpreter you wish to compile with.

You will prompted for which connection to compile against. Choose the connection name.


![image](https://user-images.githubusercontent.com/1747643/34592761-5ded2e9e-f194-11e7-9f70-fea9edfc5251.png)

![image](https://user-images.githubusercontent.com/1747643/34592822-bf594b86-f194-11e7-9671-66e38defcfe9.png)

## Configuration

As mentioned, this extension depends on the binaries for SQL*Plus or SQLcl being available on your system. These default to `sqlplus` and `sql` respectively. If these are not within your Path, or have been renamed to something else, you can set an alternative path/name within settings.

![image](https://user-images.githubusercontent.com/1747643/34592890-4d9e8e2e-f195-11e7-9426-a5198f74eeb0.png)


## Author

Trent Schafer

## LICENSE

MIT