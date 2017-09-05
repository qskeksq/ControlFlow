# Control flow 이용해서 도형 그리기

- []()

``` java
public void drawLeftTriangle(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner=0; inner<outer+1; inner++) {
				System.out.print(mark);
			}
			System.out.println("");
		}
		System.out.println(" ");
	}
```

```java
public void drawRightTriangle(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner1=limit-(outer+1); inner1>0; inner1--) {
				System.out.print(" ");
			}
			for(int inner2=0; inner2<outer+1; inner2++) {
				System.out.print(mark);
			}
			System.out.println(" ");
		}
		System.out.println(" ");
	}
```
```java
public void drawTriangle(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner1=limit-(outer+1); inner1>0; inner1--) {
				System.out.print(" ");
			}
			for(int inner2=0; inner2<(2*outer+1); inner2++) {
				System.out.print(mark);
			}
			System.out.println(" ");
		}
		System.out.println(" ");
	}
```

```java
public void drawEmptyTriangle1(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner1=limit-(outer+1); inner1>0; inner1--) {
				System.out.print(" ");
			}
			for(int inner2=0; inner2<(2*outer+1); inner2++) {
				if(inner2==0 || inner2==(2*outer)) {
					System.out.print(mark);
				} else {
					System.out.print(" ");
				}
			}
			System.out.println(" ");
		}
		System.out.println("");
	}
```


- []()

```java
public void drawEmptyTriangle2(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner1=limit-(outer+1); inner1>0; inner1--) {
				System.out.print(" ");
			}
			for(int inner2=0; inner2<(2*outer+1); inner2++) {
				if(inner2==0 || inner2==(2*outer)) {
					System.out.print(mark);
				} else {
					if(outer == limit-1) {
						System.out.print(mark);
					} else {
						System.out.print(" ");
					}
				}
			}
			System.out.println(" ");
		}
		System.out.println("");
	}
```

```java
public void drawLosange1(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner1=limit-(outer+1); inner1>0; inner1--) {
				System.out.print(" ");
			}
			for(int inner2=0; inner2<(2*outer+1); inner2++) {
				System.out.print(mark);
			}
			System.out.println(" ");
		}
		for(int outer=0; outer<limit-1; outer++) {
			for(int inner=0; inner<outer+1; inner++) {
				System.out.print(" ");
			}
			for(int inner=2*limit-3; inner>2*outer; inner--) {
				System.out.print(mark);
			}
			System.out.println(" ");
		}
		System.out.println(" ");
	}
```


- []()

```java
public void drawLosange2(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner1=limit-(outer+1); inner1>0; inner1--) {
				System.out.print(" ");
			}
			for(int inner2=0; inner2<(2*outer+1); inner2++) {
				if(inner2%2==0) {
					System.out.print(mark);
				} else {
					System.out.print(" ");
				}
			}
			System.out.println(" ");
		}
		for(int outer=0; outer<limit-1; outer++) {
			for(int inner=0; inner<outer+1; inner++) {
				System.out.print(" ");
			}
			for(int inner=2*limit-3; inner>2*outer; inner--) {
				System.out.print(mark);
			}
			System.out.println(" ");
		}
		System.out.println(" ");
	}
```
```java
public void drawLosange3(String mark, int limit) {
		for(int outer=0; outer<limit; outer++) {
			for(int inner1=limit-(outer+1); inner1>0; inner1--) {
				System.out.print(" ");
			}
			for(int inner2=0; inner2<(2*outer+1); inner2++) {
				if(inner2==0 ||inner2==2*outer) {
					System.out.print(mark);
				} else {
					System.out.print(" ");
				}
			}
			System.out.println(" ");
		}
		for(int outer=0; outer<limit-1; outer++) {
			for(int inner=0; inner<outer+1; inner++) {
				System.out.print(" ");
			}
			for(int inner=2*limit-3; inner>2*outer; inner--) {
				if(inner==2*limit-3 || inner==2*outer+1) {
					System.out.print(mark);
				} else {
					System.out.print(" ");
				}
			}
			System.out.println(" ");
		}
		System.out.println(" ");
	}
```

- []()

```java
public void drawX(String mark, int limit) {
		for(int outer=0; outer<2*limit-1; outer++) {
			if(outer<limit-1) {
				for(int inner=0; inner<outer; inner++) {
					System.out.print(" ");
				}
				for(int inner2=2*limit-1; inner2>2*outer; inner2--) {
					if(inner2==2*outer+1||inner2==2*limit-1) {
						System.out.print(mark);
					} else {
						System.out.print(" ");
					}
				}
			} else if(outer==limit-1||outer>2*limit-1) {
				for(int inner=0; inner<limit; inner++) {
					for(int inner2=limit-1; inner2>inner; inner2--) {
						System.out.print(" ");
					}
					for(int inner2=0; inner2<2*inner+1; inner2++) {
						if(inner2==0||inner2==2*inner) {
							System.out.print(mark);
						} else {
							System.out.print(" ");
						}
					}
					System.out.println("");
				}
			}
			System.out.println("");
		}
		System.out.println("");
	}
```
```java
public void drawEmptyBox(String mark, int limit) {
		for(int outer=0; outer<limit*2-1; outer++) {
			if(outer==0 || outer==2*limit-2) {
				for(int inner=0; inner<2*limit-1; inner++) {
					System.out.print(mark);
				}
			} else {
				for(int inner=0; inner<2*limit-1; inner++) {
					if(inner==0 || inner==2*limit-2) {
						System.out.print(mark);
					} else {
						System.out.print(" ");
					}
				}
			}
			System.out.println(" ");
		}
		System.out.println(" ");
	}

	public void drawFan(String mark, int limit) {

		for(int outer=0; outer<limit; outer++) {

			int space = ((limit)*(limit)-(limit+-outer)*(limit-outer))/2;

			for(int inner=0; inner<space; inner++) {
				System.out.print(" ");
			}

			for(int inner=0; inner<(limit-outer)*(limit-outer); inner++) {

				if(inner%(limit-outer)==0) {
					System.out.print(mark);
				} else {
					System.out.print(" ");
				}
			}
			System.out.println("");
		}
	}
```
