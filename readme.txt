import numpy as py
import matplotlib.pyplot as plt

def euler_method(f,y0,x0,x1,n):
    h=(x1-x0) / n
    x2=[x0]
    y2=[y0]
    x=x0
    y=y0
    
    for i in range(n):
        x=x+h
        y=y+h*f(x,y)
        x2.append(x)
        y2.append(y)
        
    return x2,y2
    
def f(x,y):
    return py.cos(x)
    
def plot(f,y0,x0,x1,n):
    x2,y2=euler_method(f,x0,y0,x1,n)
    plt.plot(x2,y2,marker='o')
    plt.xlabel('x')
    plt.ylabel('y')
    plt.title('Euler Method Solution')
    plt.grid(True)
    plt.savefig('myplot5.png')
    
    x0=0
    x1=5
    n=100
    y0=1
    
    plot(f,y0,x0,x1,n)  



