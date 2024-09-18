This project give an introduction into Openlane flow where each step is excecuted in an interactive way using the already existing design of RISC-V 32bit processor named "picorv32a". The open source eda flow involves may steps such as run_synthesis, run_floorplan, run_placement etc. Some of the intances of the outputs obtained from these steps are shown below.

![Screenshot_02 synthesis statics report](https://github.com/user-attachments/assets/4ea65e30-d4db-4435-91ca-b9aef1b93985) 
![Screenshot_03 STA timing report](https://github.com/user-attachments/assets/927ba54b-84db-4997-a4b3-2f5970ac7754) 
![Screenshot_04 floorplan_run](https://github.com/user-attachments/assets/955e0ea9-236e-4278-bebf-26ff4d61b990) 
![Screenshot_05 magic_floorplan](https://github.com/user-attachments/assets/01e2bca5-49c5-4aac-b809-01663ed6ae7f)
![Screenshot_06 placement_run](https://github.com/user-attachments/assets/e4e6f42a-6f58-4363-a6d3-a988c94fd2f6)
![Screenshot_07 magic_placement](https://github.com/user-attachments/assets/e80f7816-94d3-4614-95fb-f1fb067d3544)



Additionally, a standard cell for inverter (sky130_vsdinv) was custom desgined using magic and then it was chracterized using ngspice. 

![Screenshot_08 inv layout using sky130A tech](https://github.com/user-attachments/assets/0e3fab3d-d3bf-4889-bf2e-07fb723a017b)
![Screenshot_09 parasitic extraction](https://github.com/user-attachments/assets/7b9c52e9-e47c-4f8f-b078-fcd5fef78f92)
![Screenshot_10 inv dynamic chara](https://github.com/user-attachments/assets/59c0d38f-7c7d-4f3d-a5ba-0db069f4c28c)



The lef file of the "sky130_vsdinv" was written and it was introduced into the picorv32a design flow. The files describing the extensive characteristics of the inverter were also added into the flow. The results obtained after run_synthesis command ensured that sky130_vsdinv was utilized in the automated net generation.

![Screenshot11 vsdinv introduced](https://github.com/user-attachments/assets/c00dffae-5fd7-490a-92d1-47200bf2b8fe)

The netlist obtained after floorplan and placement was opened in magic to confirm the presence of "sky130_vsdinv" with in the "picorv32a" design.

![Screenshot12 sky130_vsdinv placed](https://github.com/user-attachments/assets/843af244-7416-4b11-927c-b4f9453d09b3)


