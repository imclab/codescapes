codescapes
==========

3D code base visualisation.

In this visualisation, a git repository can be loaded and is visualised as a grid of blocks.

Each block represents a file and its height represents the number of lines in the file.

# Installation
First of all, Docker needs to be installed. Check [the install docs](https://docs.docker.com/) for more.

You will also need node.js to run the Codescapes server.

## Getting the repository ready

```shell
  $ git clone https://github.com/AVGP/codescapes.git
  $ cd codescapes
  $ npm install
```

## Creating the Docker worker image

```shell
  $ docker build -t codescape-worker .
```

# Running the server

```shell
  $ node server.js
```

Then go to your server address on Port `8080`.

# Usage

To load one of the repositories, you just append `#brackets.json` and you're ready to go an explore!

A `POST` request to /analyse with a parameter `url` containing a git URL allows you to get additional repositories for visualisation.

# Keyboard / Mouse controls

Move with W/A/S/D and turn the camera up and down with the corresponding arrow keys.
Click on a block to see the file name it represents.
