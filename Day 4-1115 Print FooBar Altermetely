class FooBar {
    private int n;
    private Semaphore fooSem =new Semaphore (1);
    private Semaphore barSem=new Semaphore(0);

    public FooBar(int n) {
        this.n = n;
    }

    public void foo(Runnable printFoo) throws InterruptedException {
        
        for (int i = 0; i < n; i++) {
            fooSem.acquire();
            printFoo.run();
            barSem.release();
            
        	// printFoo.run() outputs "foo". Do not change or remove this line.
        }
    }
