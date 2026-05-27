# Series Queues with infinite capacity - Open Jackson Network

## Aim :
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival  of materials follow Poisson process with the mean interval time 12 seconds, service time of  lathe machine in series follow exponential distribution  with service time  1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.

## Software required :
Visual components and Python

## Theory

![image](https://user-images.githubusercontent.com/103921593/203239736-7b81f599-71a8-4ae7-b63e-5d98acd9ea54.png)


## Procedure :

![image](https://user-images.githubusercontent.com/103921593/203239789-bc870dce-6727-487b-a0e2-4fc3f5114889.png)


## Experiment:


## Program

~~~~
lam = 1 / 12

service_times = [1, 1.5, 1.3, 7]

machines = ["Lathe 1", "Lathe 2", "Lathe 3", "Robot"]

total_L = 0
total_Lq = 0
total_W = 0
total_Wq = 0

for i in range(len(service_times)):

    mu = 1 / service_times[i]

    rho = lam / mu

    Lq = (rho ** 2) / (1 - rho)

    L = rho / (1 - rho)

    Wq = Lq / lam
    W = L / lam

    total_L += L
    total_Lq += Lq
    total_W += W
    total_Wq += Wq
print("\nTOTAL SYSTEM VALUES")
print("Average number in total system =", round(total_L, 4))
print("Average number in all conveyors =", round(total_Lq, 4))
print("Total waiting time in system =", round(total_W, 4), "sec")
print("Total waiting time in conveyors =", round(total_Wq, 4), "sec")
~~~~


## Output
<img width="388" height="170" alt="image" src="https://github.com/user-attachments/assets/d8d4cae1-193d-4991-8a15-b6950186f22f" />

## Result
Thus given experiment is done successfully.
