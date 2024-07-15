# name
import tkinter as tk
from random import choice

# List of South African male names
south_african_names = [
    "Thabiso", "Siyabonga", "Mandlenkosi", "Mpho", "Thandiso",
    "Sibusiso", "Lungile", "Luthando", "Nkosi", "Sipho"
]

def generate_name():
    name = choice(south_african_names)
    name_label.config(text=name)

# Create the main window
root = tk.Tk()
root.title("South African Male Name Generator")
root.geometry("400x200")

# Button to generate a name
generate_button = tk.Button(root, text="Generate Name", command=generate_name)
generate_button.pack(pady=20)

# Label to display the generated name
name_label = tk.Label(root, text="", font=("Helvetica", 18))
name_label.pack(pady=20)

# Run the main event loop
root.mainloop()
