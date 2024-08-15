## GamePad Software

This directory contains a Dockerized build system for the game pad programs. The programs themselves are located as part of the original gamepad repository.

To programme the game pad. Have a look at Dockerfile, docker-compose.yml and Makefile. These do all the work. 

  make tetris

Will build the tetris code and programme the Ch32V003 processor.
