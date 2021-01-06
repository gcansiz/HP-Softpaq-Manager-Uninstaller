import os
import subprocess
import time
import wmi

HP_programs = ["HP SoftPaq Download Manager"]

def main():
    HP_uninstall()

def HP_uninstall():
    for program in HP_programs:
        print(f"Uninstalling {program}...")
        subprocess.call(f"wmic product where name='{program}' call uninstall /nointeractive", shell=True)
    print("HP SoftPaq Download Manager software have been uninstalled.")

#def HP_install():

if __name__ == "__main__":
    main()
