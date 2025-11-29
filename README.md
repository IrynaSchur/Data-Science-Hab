week2>>

XOR Neural Network Experiments (PyTorch)

This project demonstrates how a small neural network can learn the XOR logic function using PyTorch.
It compares:

Different activation functions:
✔ Sigmoid
✔ Tanh
✔ ReLU

Different learning rates

Different numbers of training epochs

The project also generates graphs (loss curves) to visualize how these choices affect training quality.

📌 What This Project Does

Builds three neural network variants for XOR

Trains them with different activation functions

Tests different learning rates (LR)

Tests different training durations (epochs)

Draws graphs showing:

How fast the model learns

How stable the learning is

Which parameters give the best results

Shows final predictions for each activation function

This is a great project for understanding the fundamentals of neural networks.

How to Run

Open terminal

Activate your environment:

conda activate forecast37


Run the script:

python xor_full_experiments.py


You will see multiple graphs and printed results.

📊 What You’ll See
1. Activation Function Comparison

A graph comparing:

Sigmoid

Tanh

ReLU

2. Learning Rate Comparison

You will see which LR learns fastest, and which ones fail.

3. Epoch Comparison

Shows how training length affects performance.

4. Final predictions

Example:

[0, 1] -> 0.98 -> rounded 1 (expected 1)

🏁 FINAL CONCLUSIONS (VERY IMPORTANT)

Based on all experiments (graphs + predictions), here are the main conclusions:

🔵 1. Tanh is the best activation function for XOR

tanh learns much faster

loss decreases smoothly

the network easily reaches correct predictions

it handles negative values well (important for XOR)

Conclusion:
➡️ Tanh is the most effective activation for XOR

🟠 2. Sigmoid works, but slowly

Loss decreases very slowly

Sometimes gets stuck

Often needs more epochs or higher learning rate

Conclusion:
➡️ Sigmoid can learn XOR but is less efficient than tanh

🔴 3. ReLU often fails on XOR

XOR needs negative activation values

ReLU “kills” negative numbers → sets them to 0

Because of this, the model sometimes NEVER learns XOR

Conclusion:
➡️ ReLU is NOT suitable for XOR

🟢 4. Learning rate strongly affects the results

Results from experiments:

Learning Rate	Behavior
0.01	Learns extremely slowly
0.1	Stable learning
0.5	Fastest convergence (best for XOR)
1.0	Unstable, jumps around

Conclusion:
➡️ LR = 0.5 works best for XOR in this project
➡️ Too small → slow
➡️ Too big → unstable

🟣 5. More epochs → better learning (up to a point)

Results:

500 epochs: Not enough

2000 epochs: Starts learning

8000 epochs: Nearly perfect XOR predictions

Conclusion:
➡️ You need several thousand epochs for XOR
➡️ 8000–10000 epochs gives the best performance

⭐ Summary of the Best Settings

✔ Activation: Tanh
✔ Hidden neurons: 8
✔ Learning rate: 0.5
✔ Epochs: 8000

With these settings, the model consistently learns XOR to near-perfect accuracy.
