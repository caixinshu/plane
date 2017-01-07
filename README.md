# plane
import pygame
from sys import exit
from pygame import *
pygame.init()

screen = pygame.display.set_mode((390,400),0,32)

pygame.display.set_caption('Hello,World')

# backgroud = pygame.image.load('C:\Users\XM\Desktop\\bg.jpg').convert()
bg1=image.load('C:\Users\XM\Desktop\\bg.jpg').convert()
bg2=image.load('C:\Users\XM\Desktop\\bg2.jpg').convert()
target=True
bg=bg1
while True:
    for event in pygame.event.get():
        if event.type==pygame.MOUSEBUTTONDOWN:
            # backgroud=pygame.image.load('C:\Users\XM\Desktop\\bg2.jpg').convert()
            if target:
                target= not target
                bg=bg2
            else:
                target=not target
                bg=bg1

        if event.type == pygame.QUIT:
            pygame.quit()
            exit()

    screen.blit(bg,(0,0))
    pygame.display.update()
