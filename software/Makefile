MINICHLINK=~/github/ch32v003fun/minichlink/minichlink
FW=~/github/CH32V003-GameConsole/software

# calibrator  tiny_arkanoid  tiny_invaders  tiny_lander  tiny_pacman  tiny_tris

invaders:
	make prog LOC=tiny_invaders

tetris:
	make prog LOC=tiny_tris

arkanoid:
	make prog LOC=tiny_arkanoid

pacman:
	make prog LOC=tiny_pacman

lander:
	make prog LOC=tiny_lander

conway:
	make prog LOC=tiny_conway

prog:
	make compile LOC=${LOC}
	${MINICHLINK} -w ./build_target/${LOC}.bin flash -b

build:
	docker compose build --progress plain --parallel=1

compile:
	LOC=${LOC} docker compose up
