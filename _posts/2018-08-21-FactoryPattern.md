---
layout: post
title: Factory Pattern
tags: [TIL]
---
### Factory Pattern

#### Purpose(사용 목적)
Encapsulating Object creation
1. 객체 생성을 캡슐화한다.
2. 구상 클래스에 대한 의존성을 줄인다. 

#### Classification(분류)
1. Factory Method Pattern
2. Abstract Factory Pattern

#### Factory Method Pattern
하위 클래스가 어떤 객체를 생성할지 결정한다.

1. Pizza Class (abstract class)
``` 
public abstract class Pizza
{
    public abstract decimal GetPrice();

    public enum PizzaType{
        HamMushroom, Deluxe, Seafood
    }

    public static Pizza PizzaFactory(PizzaType pizzaType){
        switch(pizzaType){
            case PizzaType.HamMushroom:
                return new HamAndMushroomPizza();

            case PizzaType.Deluxe:
                return new DeluxePizza();

            case PizzaType.Seafood:
                return new SeafoodPizza();

            throw new System.NotSupportedException("The pizza type is not recognized.");
        }
    }       
}
```

2. Child Classes
```
public class HamAndMushroomPizza : Pizza
{
    private decimal price = 8.5m;
    public override decimal GetPrice(){ return price; }
}

public class DeluxePizza : Pizza
{
    private decimal price = 10.5m;
    public override decimal GetPrice(){ return price; }
}

public class SeafoodPizza : Pizza
{
    private decimal price = 11.5m;
    public override decimal GetPrice(){ return price; }
}
```

3. Main Method

```
static void Main(string[] args)
{
    // if pizza type change
    // you change only Pizza.PizzaType part
    Pizza pizza = Pizza.PizzaFactory(Pizza.PizzaType.Seafood);
    Console.WriteLine(pizza.GetPrice().ToString("C2"));
    // 11.5
}
```


