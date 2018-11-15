# SeleniumGridSetUpUsingDocker
Grid setup using docker
Command to start hub
docker run -d -p 4444:4444 --name selenium-hub selenium/hub
Command to start firefox node
docker run -d -p 5555:5555 --name firefox-node --link selenium-hub:hub selenium/node-firefox
Command to start chrome node
docker run -d -p 5556:5555 --name chrome-node --link selenium-hub:hub selenium/node-chrome
Command to start firefox node in debug mode
docker run -d -p 5900:5900 --name firefox-node-debug --link selenium-hub:hub selenium/node-firefox-debug
Command to start chrome node in debug mode
docker run -d -p 5900:5900 --name chrome-node-debug --link selenium-hub:hub selenium/node-chrome-debug