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

