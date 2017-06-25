# Code Samples - 1. Jump

```python
# Jump.py

import mcpi.minecraft as minecraft

mc = minecraft.Minecraft.create()

mc.postToChat("Jump")
x, y, z = mc.player.getPos() # Get players position
mc.player.setPos(x, y+50, z)
```

# Code Samples - 2. Teleport Tour

```python
# TeleportTour.py

import mcpi.minecraft as minecraft
import time

mc = minecraft.Minecraft.create()

mc.postToChat("Boing")
x, y, z = mc.player.getPos() # Get the players position
mc.player.setPos(x, y+10, z+10)
time.sleep (1)

mc.postToChat("Boing")
x, y, z = mc.player.getPos() # Get the players position
mc.player.setPos(x, y+10, z+10)
time.sleep (1)

mc.postToChat("Boing")
x, y, z = mc.player.getPos() # Get the players position
mc.player.setPos(x, y+10, z+10)
time.sleep (1)
```

# Code Samples - 3. Mushroom Trail

```python
# MushroomTrail.py

import mcpi.minecraft as minecraft
from time import sleep

mc = minecraft.Minecraft.create()

mc.postToChat ("Let's build!")
blockType = 40 # Mushroom

while True:
	x, y, z = mc.player.getPos() # Get player position
	mc.setBlock(x, y, z, blockType)
	sleep(0.1)
  ```

# Code Samples - 4. Build A house

```python
# BuildHouse.py

import mcpi.minecraft as minecraft
from time import sleep

mc = minecraft.Minecraft.create()

length = 6
width = 6
height = 6
blockType = 4
air = 0

mc.postToChat("Build a house")

x, y, z = mc.player.getPos()
mc.setBlocks(x+1, y, z, x+width+1, y+height, z+length, blockType)

# Hollow out the inside
mc.setBlocks(x+2, y, z+1, x+width-1, y+height-1, z+length-1, air)

# Make a door
mc.setBlocks(x+1, y, z+3, x+1, y+2, z+4, air)
```

# Code Samples - 5. Let It Snow

```python
# LetItSnow.py

import mcpi.minecraft as minecraft

mc = minecraft.Minecraft.create()

playerPos = mc.player.getPos()
for x in range (pos.x, pos.x+10):
	for z in range (pos.z, pos.z+10):
		y = mc.getHeight(x, z)
		mc.setBlock(x, y, z, 78) # 78 = Snow
```

# Code Samples - 6. Block Fighter

```python
# BlockFighter.py

import mcpi.minecraft as minecraft
from time import sleep

mc = minecraft.Minecraft.create()

mc.postToChat("Use the right button to hit blocks and score")
score = 0
sleep (60)

hits = mc.events.pollBlockHits()

for hit in hits:
	# score +=1 and 1 point per hit
	x = hit.pos.x
	y = hit.pos.y
	z = hit.pos.z
	score = score + mc.getBlock(x, y, z)
	print (mc.getBlock(x, y, z))
mc.postToChat("You got " + str(score) + " points!")
```

# Code Samples - 7. Burried Treasure

```python
# BuriedTreasure.py

import mcpi.minecraft as minecraft
from time import sleep

mc = minecraft.Minecraft.create()

treasure = 16 # coal
#treasure = int(input("What treasure do ye seek matey:"))

while True:
	x, y, z = mc.player.getPos()
	z -=1
	for i in range (1,60): # look 50 blocks down
		if mc.getBlock(x, y, z) == treasure:
			mc.postToChat("There be treasure " + str(i) + "space below you!")
			break
		else:
			y -=1
			mc.postToChat("Sorry matey, nothing here!")
	sleep (0.2)
```

# Code Samples - 8. Flat land

```python
# FlatLand.py

import mcpi.minecraft as minecraft
import mcpi.block as block
from time import sleep

mc = minecraft.Minecraft.create()

mc.postToChat("Flattening land")
mc.setBlocks(-128, 0, -128, 128, 64, 128, 0)
mc.setBlocks(-128, 0, -128, 128, 64, 128, 24)
```

# Code Samples - 9. Hide and seek

```python
# HideAndSeek.py

import mcpi.minecraft as minecraft
from time import sleep
import math
import random

mc = minecraft.Minecraft.create()

targetBlock = 41 # gold
destX = random.randint(-127, 127)
destZ = random.randint(-127, 127)
destY = mc.getHeight(destX, destZ) # ground level
print (destZ)
mc.setBlock(destX, destY, destZ, targetBlock)

mc.postToChat("Block hidden - go find it!")
print ("x: " + str(destX) + " y: " + str(destY) + " z:" + str(destZ))

while True:
	pos = mc.player.getPos()
	distance = math.sqrt((pos.x-destX)**2 + (pos.z-destZ)**2)
	if distance > 100:
		mc.postToChat("Freezing!")
	elif distance > 50:
		mc.postToChat("Cold!")
	elif distance > 25:
		mc.postToChat("Warm!")
	elif distance > 15:
		mc.postToChat("Hot!")
	elif distance < 2:
		mc.postToChat("Found it!")
	sleep(0.2)
```
