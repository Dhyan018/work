# work
import tkinter as tk
import time

def update_time():
    current_time = time.strftime("%H:%M:%S")
    label.config(text=current_time)
    label.after(1000, update_time)

# Create the main window
root = tk.Tk()
root.title("Digital Clock")
root.geometry("300x100")
root.configure(bg="black")

# Create and style the clock label
label = tk.Label(root, font=("Arial", 48), fg="cyan", bg="black")
label.pack(expand=True)

# Start the clock
update_time()

# Run the app
root.mainloop()
