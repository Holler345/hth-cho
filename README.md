import pygame


pygame.init()

screen_width = 800
screen_height = 600

screen = pygame.display.set_mode((screen_width, screen_height))

font = pygame.font.SysFont("Kristen ITC", 50)
font2 = pygame.font.SysFont("Kristen ITC", 30)

main_ohmygad = pygame.image.load("img/choblayt.jpg")
main_ohmygad = pygame.transform.scale(main_ohmygad, (54,70))
main_kofsj879 = pygame.image.load("img/jjhgfdr23453.jpeg")
main_kofsj879 = pygame.transform.scale(main_kofsj879, (54,123))

x,y = 140, 40
x1,y1 = 350, 212
x2,y2 = 545, 500
speed = 0.05
x_cat, y_cat, h_cat, k_cat, j_cat, o_cat, p_cat, n_cat = 10, 88, 55, 90, 40, 123, 48, 150


while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            quit()


    screen.blit(main_ohmygad, (350,350))


    text = font.render("Welcome to game!!", True, (0, 0, 100))
    screen.blit(text, (x, y))
    text2 = font2.render("start game!!", True, (132, 56, 150))
    screen.blit(text2, (x1, y1))
    textadsf = font.render("seetings", True, (110, 110, 100))
    screen.blit(textadsf, (x2, y2))

    keys = pygame.key.get_pressed()
    if keys[pygame.K_w]:
        x_cat += speed
    if keys[pygame.K_d]:
        y_cat += speed
    if keys[pygame.K_s]:
        h_cat += speed
    if keys[pygame.K_a]:
        k_cat += speed

    screen.blit(main_kofsj879, (o_cat, j_cat))
    screen.blit(main_ohmygad, (p_cat, n_cat))

    pygame.display.update()
