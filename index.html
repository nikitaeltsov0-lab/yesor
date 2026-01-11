import tkinter as tk
import random

root = tk.Tk()
root.title("Красивое меню с анимацией")
root.geometry("360x640")

canvas_width = 360
canvas_height = 640
canvas_size = 120  # размер кнопки

canvas = tk.Canvas(root, width=canvas_width, height=canvas_height, highlightthickness=0)
canvas.pack()

def рисовать_градиент(канвас, ширина, высота, цвет_начала, цвет_конца):
    r1, g1, b1 = root.winfo_rgb(цвет_начала)
    r2, g2, b2 = root.winfo_rgb(цвет_конца)
    r_ratio = (r2 - r1) / высота
    g_ratio = (g2 - g1) / высота
    b_ratio = (b2 - b1) / высота

    for i in range(высота):
        nr = int(r1 + (r_ratio * i))
        ng = int(g1 + (g_ratio * i))
        nb = int(b1 + (b_ratio * i))
        цвет = f'#{nr>>8:02x}{ng>>8:02x}{nb>>8:02x}'
        канвас.create_line(0, i, ширина, i, fill=цвет)

рисовать_градиент(canvas, canvas_width, canvas_height, "#1e3c72", "#2a5298")

цвет_по_умолчанию = "#4CAF50"
цвет_нажатия = "#E53935"

центр_x = canvas_width // 2
центр_y = int(canvas_height * 0.5)  # кнопка ниже центра

радиус = canvas_size // 2
круг = canvas.create_oval(центр_x - радиус, центр_y - радиус, центр_x + радиус, центр_y + радиус, fill=цвет_по_умолчанию, outline="")

текст_id = canvas.create_text(центр_x, int(canvas_height * 0.8), text="", font=("Arial", 28), fill="white")

можно_нажать = True

def плавное_появление(шаг=0, макс=10):
    if шаг > макс:
        return
    уровень_яркости = int(50 + (205 * шаг / макс))  # от тёмно-серого к белому
    цвет = f'#{уровень_яркости:02x}{уровень_яркости:02x}{уровень_яркости:02x}'
    canvas.itemconfig(текст_id, fill=цвет)
    root.after(50, плавное_появление, шаг + 1, макс)

def анимация_кнопки(шаг=0):
    global можно_нажать
    total_steps = 20
    mid = total_steps // 2

    if шаг == 0:
        canvas.itemconfig(круг, fill=цвет_нажатия)
        можно_нажать = False

    if шаг > total_steps:
        canvas.itemconfig(круг, fill=цвет_по_умолчанию)
        можно_нажать = True
        return

    if шаг <= mid:
        масштаб = 1 - 0.2 * (шаг / mid)
    else:
        масштаб = 0.8 + 0.2 * ((шаг - mid) / mid)

    размер = canvas_size * масштаб
    отступ = (canvas_size - размер) / 2
    canvas.coords(круг,
                  центр_x - радиус + отступ,
                  центр_y - радиус + отступ,
                  центр_x + радиус - отступ,
                  центр_y + радиус - отступ)

    root.after(25, анимация_кнопки, шаг + 1)

def нажать(event):
    global можно_нажать
    if not можно_нажать:
        return

    анимация_кнопки()
    ответ = random.choice(["Да", "Нет"])
    canvas.itemconfig(текст_id, text=ответ, fill="#323232")  # тёмно-серый (почти невидимый)
    плавное_появление()

canvas.tag_bind(круг, "<Button-1>", нажать)

root.mainloop()
