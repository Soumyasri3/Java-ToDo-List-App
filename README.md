# Java-ToDo-List-App
A simple Java console-based To-Do List application using ArrayList and file handling.



package com.todo.app;

import java.util.ArrayList;
import java.util.Scanner;

public class TodoApp {
    public static void main(String[] args) {

        ArrayList<String> tasks = new ArrayList<>();
        Scanner sc = new Scanner(System.in);

        while (true) {
            System.out.println("\n1. Add Task  "
            		+ "2. View Tasks  "
            		+ "3. Delete Task  "
            		+ "4. Exit");
            System.out.print("Enter choice: ");
            int choice = sc.nextInt();
            sc.nextLine();

            if (choice == 1) {
                System.out.print("Enter task: ");
                tasks.add(sc.nextLine());

            } else if (choice == 2) {
                System.out.println("\nTask List:");
                for (int i = 0; i < tasks.size(); i++) {
                    System.out.println((i + 1) + ". " + tasks.get(i));
                }

            } else if (choice == 3) {
                System.out.print("Enter task number to delete: ");
                int index = sc.nextInt();
                tasks.remove(index - 1);

            } else {
                break;
            }
        }

        sc.close();
        System.out.println("Goodbye!");
    }
}

