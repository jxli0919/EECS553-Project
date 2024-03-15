# EECS 553_Project
Final project for EECS 553 Machine Learning, Fall 2022. 

Project: Reproducibility Study of ”Learning Fast, Learning Slow”

Reproduced from [Learning Fast, Learning Slow](https://github.com/NeurAI-Lab/CLS-ER), made some modifications. 

We ran their given code on the corresponding datasets and verified that the test accuracies 
were correct. We also searched for the optimal update rates and buffer size. We then constructed a sequential learning variation of the CIFAR‐100 dataset and compared
the CLS‐ER model with the best baseline model.

1.	To reproduce the results in the original paper run the following
python main.py --dataset <dataset> --model <model> --buffer_size <buffer_size> --load_best_args
Examples:
    python main.py --dataset seq-mnist --model clser --buffer_size 500 --load_best_args

    python main.py --dataset seq-mnist --model derpp --buffer_size 500 --load_best_args

    python main.py --dataset seq-cifar10 --model clser --buffer_size 500 --load_best_args

    python main.py --dataset rot-mnist --model clser --buffer_size 500 --load_best_args

    python main.py --dataset mnist-360 --model clser --buffer_size 500 --load_best_args

2.	To reproduce the additional results, 
a.	For additional results 1 and 2, we changed the parameters of update rates and buffer size in the “best_args.py” in the “utils” folder
b.	For additional result 3, we added “seq_cifar100.py” in the “datasets” folder, added a loading code for seq_cifar100 in the “__init__.py” in the “datasets” folder, and added parameters for seq_cifar100 in “best_args.py” in the “utils” folder
3.	The result and running process can be found in the “Reproduce Result Tables” and two google colab notebook.

