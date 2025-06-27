---
title: "Program Java Menghitung Luas Lingkaran"
date: 2023-03-13
categories: 
  - "pemrograman"
tags: 
  - "java-2"
---

```
import java.util.Scanner;
class LuasLingkaran {
    public static void main(String args[]){
        System.out.println("Hitung Luas Lingkaran dengan Inputan");
        System.out.println("=================================");    

        Scanner input = new Scanner(System.in);

        double phi = 3.14;

        System.out.print("Masukkan jari jari : ");
        double jari = input.nextDouble();

        double luas = phi * jari * jari;
        System.out.println("Luas lingkaran adalah: " + luas);

        System.out.println("=================================");
    }
}
```
