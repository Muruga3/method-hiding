# method-hiding
package com.test;
 
class Parent {
 
    public static void foo() {
        System.out.println("Inside foo method in parent class");
    }
 
    public void bar() {
        System.out.println("Inside bar method in parent class");
    }
}
 
class Child extends Parent {
    // Hiding
    public static void foo() {
        System.out.println("Inside foo method in child class");
    }
 
    // Overriding
    public void bar() {
        System.out.println("Inside bar method in child class");
    }
}
 
public class Code {
 
    public static void main(String[] args) {
        Parent p = new Parent();
        Parent c = new Child();
        System.out.println("****************Method Hiding*******************");
        p.foo(); // This will call method in parent class
        c.foo(); // This will call method in parent class
        System.out.println("****************Method overriding*******************");
        p.bar(); // This will call method in parent class
        c.bar(); // This will call method in child class
 
    }
}
