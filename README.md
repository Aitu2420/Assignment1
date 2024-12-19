import javax.swing.*;
import java.awt.*;
import java.awt.image.BufferedImage;
import java.util.Scanner;
import java.lang.String;
import java.text.DecimalFormat;
public class ACMPFILE {
    static class Animal {
        String name;
        String diet;
        int age;
        public Animal(String name, String diet, int age) {
            this.name = name;
            this.diet = diet;
            this.age = age;
        }
        public void showOff() {
            System.out.println("Animal's Name  = " + name + ", Diet = " + diet + ", Age  = " + age + "");
        }
        public void getName() {
            System.out.println(name);
        }

        public void setName(String name) {
            this.name = name;
        }
        public void getDiet() {
            System.out.println(diet);
        }
        public void setDiet(String diet) {
            this.diet = diet;
        }
        public void getAge() {
            System.out.println(age);
        }

        public void setAge(int age) {
            this.age = age;
        }
    }
    ////////////////////////////////////////////////////
    static class Zookeeper {
        String name;
        int age;
        int yearsOfExperience;

        public Zookeeper(String name, int age, int yearsOfExperience) {
            this.name = name;
            this.age = age;
            this.yearsOfExperience = yearsOfExperience;
        }

        // Getters and setters
        public void getName() {
            System.out.println(name);
        }
        public void setName(String name) {
            this.name = name;
        }

        public void getAge() {
            System.out.println(age);
        }

        public void setAge(int age) {
            this.age = age;
        }

        public void getYearsOfExperience() {
            System.out.println(yearsOfExperience);
        }

        public void setYearsOfExperience(int yearsOfExperience) {
            this.yearsOfExperience = yearsOfExperience;
        }
        public void showOff() {
            System.out.println("Zookeeper Name = " + name + ", Age = " + age + ", Years of Experience = " + yearsOfExperience + "");
        }
    }
    //////////////////////////////////////////////////////////////////////////////
    static class Zoo {
        String name;
        String address;
        ACMPFILE.Animal[] animals;
        int animalCount;

        public Zoo(String name, String address, int capacity) {
            this.name = name;
            this.address = address;
            this.animals = new ACMPFILE.Animal[capacity];
            this.animalCount = 0;
        }

        // Getters and setters
        public void getName() {
            System.out.println(name);
        }

        public void setName(String name) {
            this.name = name;
        }

        public void getAddress() {
            System.out.println(address);
        }

        public void setAddress(String address) {
            this.address = address;
        }

        public void getAnimalCount() {
            System.out.println(animalCount);
        }
        public void addAnimal(ACMPFILE.Animal animal) {
            if (animalCount < animals.length) {
                animals[animalCount++] = animal;
            } else {
                System.out.println("Zoo is at full capacity!");
            }
        }
        public void showOff() {
            System.out.println("Zoo Name = " + name + ", Address = " + address + ", Animals Count = " + animalCount + "");
        }
    }
    public static void main(String[] poop) {
        Animal zebra = new Animal("John", "Plants", 2);
        Animal lion = new Animal("Bishop", "Meat", 5);
        Animal elephant = new Animal("kyle", "Anything", 21);
        zebra.showOff();
        lion.showOff();
        elephant.showOff();
        Zoo zoo = new Zoo("Russia", "Russia Federation", 2);
        zoo.addAnimal(zebra);
        zoo.addAnimal(lion);
        zoo.addAnimal(elephant);


    }
}
