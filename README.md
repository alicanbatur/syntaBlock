# Objective-C Block Syntax


### Basic

```objective-c
^{
	NSLog(@"This is a block");
}
```
### Create and use

```objective-c
void (^simpleBlock)(void) = ^{
        NSLog(@"This is a block");
};
...
simpleBlock();
```

### Defining via ```typedef```

```objective-c
typedef returnType (^blockName)(parameterTypes);
```

Example: Objective-C:
```objective-c
typedef int (^stringToIntBlock)(NSString *);
```

### Add returntype

```objective-c
returnType (^blockName)(parameterTypes) = ^returnType(parameters) {...};
```

##### Example

```objective-c
int (^calcSum)(int,int);
```
```objective-c
^(int value1, int value2) {
        return (value1 + value2);
}
```

### Basic Creation and use
```objective-c
int (^calcSum)(int, int) = ^(int value1, int value2) {
								return value1 + value2;
							};
int total = calcSum(2, 5);
// total = 5
``` 
