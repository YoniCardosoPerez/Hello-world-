# Hello-world-
This is my first line code in github
pip install ipywidgets
import ipywidgets as widgets

ignition = widgets.ToggleButton(
    value=False,
    description='Iniciar Launch',
    button_style='success',
    tooltip='Engage your Launch',
    icon='rocket'
)

output = widgets.Output()

display(ignition, output)

def on_value_change(change):
    with output:
        if change['new'] == True:
            print("Nave Iniciada!")
        else:   
            print("Nave Detenida")

ignition.observe(on_value_change, names='value')
