/*
 * Abstraction in Java
 * --------------------
 * Abstraction is a core concept of OOP that allows us to hide implementation details
 * and show only the necessary features of an object.
 * We achieve abstraction in Java using abstract classes and interfaces.
 */

// Abstract class
abstract class Vehicle {
    String brand;
    
    // Constructor
    Vehicle(String brand) {
        this.brand = brand;
    }
    
    // Abstract method (must be implemented by subclasses)
    abstract void startEngine();
    
    // Concrete method (common functionality for all vehicles)
    void displayBrand() {
        System.out.println("Brand: " + brand);
    }
}

// Concrete subclass of Vehicle
class Car extends Vehicle {
    
    Car(String brand) {
        super(brand);
    }
    
    // Implementing abstract method
    @Override
    void startEngine() {
        System.out.println("Car engine started with a key.");
    }
}

// Another Concrete subclass of Vehicle
class Bike extends Vehicle {
    
    Bike(String brand) {
        super(brand);
    }
    
    // Implementing abstract method
    @Override
    void startEngine() {
        System.out.println("Bike engine started with a self-start button.");
    }
}

// Main class to test abstraction
public class AbstractionDemo {
    public static void main(String[] args) {
        Vehicle car = new Car("Toyota");
        car.displayBrand();
        car.startEngine();
        
        System.out.println();
        
        Vehicle bike = new Bike("Yamaha");
        bike.displayBrand();
        bike.startEngine();
    }
}
