package com.glossary.app;

import java.util.Scanner;

public class GlossaryShop {
	static Scanner sc = new Scanner(System.in);
	static int qty;
	static String item;
	static int price;
	static String[] cart = new String[100];
	static int index;
	static int totalPrice;
	public static void main(String[] args) {
		GlossaryShop obj = new GlossaryShop();
		int shop;
		do {
			System.out.println("--------------------------------------------------");
			System.out.println("============ Welcome to Organic Store ============");
			System.out.println("--------------------------------------------------");
			System.out.println("Available product in the store");
			System.out.println("1) Fruits");
			System.out.println("2) Vegetables");
			System.out.println("3) Cosmetics");
			System.out.println("4) Masala Powders");
			System.out.println("--------------------------------------------------");
			System.out.println("Please Enter Your Choice ?");
			int choice = sc.nextInt();
			switch (choice) {
			case 1:
				obj.fruits();
				break;

			case 2:
				obj.vegetables();
				break;

			case 3:
				obj.cosmetics();
				break;

			case 4:
				obj.masala();
				break;

			default:
				System.out.println("You Have Entered A Wrong Choice Please Select Between 1 To 4 ");
				break;
			}
			System.out.println("If you want to Continue with Shopping Press 1");
			System.out.println("If you want to exit Press 2");
			shop = sc.nextInt();
		} while (shop == 1);
		new GlossaryShop().bill(item, qty, price);
	}

	int fruits() {
		System.out.println("--------------------------------------------------");
		System.out.println("============ welcome to fruits menu ============");
		System.out.println("--------------------------------------------------");
		System.out.println("Product code      Product Name       Product Price");
		System.out.println("--------------------------------------------------");
		System.out.println("  101             Mangoes            100/Kg");
		System.out.println("  102             Apples             70/Kg");
		System.out.println("  103             Bananans           40/Kg");
		System.out.println("  104             Papaya             60/Kg");
		System.out.println("  105             Grapes             80/Kg");
		System.out.println("  106             Oranges            90/Kg");
		System.out.println("--------------------------------------------------");
		System.out.println("Please Choose a Product Code ?");
		int choice = sc.nextInt();
		switch (choice) {
		case 101:
			item = "Mangoes";
			cart[index++] = "Mangoes";
			System.out.println("Mangoes is a good choice how many kgs you need ?");
			qty = sc.nextInt();
			cart[index++] = toString(qty);
			price = 100;
			totalPrice+=100*qty;
			cart[index++]=toString(qty*100);
			return qty;

		case 102:
			item = "Apples";
			System.out.println("Apples is a good choice how many kgs you need ?");
			qty = sc.nextInt();
			price = 70;
			return qty;

		case 103:
			item = "Bananas";
			System.out.println("Bananans is a good choice how many kgs you need ?");
			qty = sc.nextInt();
			price = 40;
			return qty;

		case 104:
			item = "Papaya";
			System.out.println("Papaya is a good choice how many kgs you need ?");
			qty = sc.nextInt();
			price = 60;
			return qty;

		case 105:
			item = "Grapes";
			System.out.println("Grapes is a good choice how many kgs you need ?");
			qty = sc.nextInt();
			price = 80;
			return qty;

		case 106:
			item = "Orange";
			System.out.println("Oranges is a good choice how many kgs you need ?");
			qty = sc.nextInt();
			price = 90;
			return qty;

		default:
			System.out.println("You Have Entered A Wrong Choice Please Select Between 101 To 106 ");
			new GlossaryShop().fruits();
			return 0;
		}
	}

	private String toString(int qty2) {

		return "" + qty2;
	}

	void vegetables() {
		System.out.println("vegetables");
	}

	void cosmetics() {
		System.out.println("cosmetics");
	}

	void masala() {
		System.out.println("masala");
	}

	void bill(String item, int qty, int price) {
		//int bill = (price * qty);
		int discount =  (int) (totalPrice * 0.05);
		System.out.println("Please Enter Your Name: ");
		String cname = sc.next();
		System.out.println("--------------------------------------------------");
		System.out.println("=========== Here is Your Bill " + cname + " ============");
		System.out.println("--------------------------------------------------");
		System.out.println("Your Purchased Items List :");
		System.out.println("--------------------------------------------------");
		System.out.println("Item                   Qty                   Price");
		System.out.println("--------------------------------------------------");
		for (int i=0; i<cart.length; ) {
			if(cart[i]==null) {
				break;
			}
			System.out.println(cart[i++] + "                " + cart[i++] + "                     " + cart[i++]);
		}
		System.out.println("--------------------------------------------------");
		System.out.println("Total Bill of Your Purchased Item is : " + totalPrice + " Rs");
		System.out.println("You Have Received Discount of 5% : " + discount + " Rs");
		System.out.println("Final Bill Amount : " + (totalPrice - discount) + " Rs");
		System.out.println("--------------------------------------------------");
		System.out.println("========== Thank You " + cname + " Visit Again =========");
		System.out.println("--------------------------------------------------");
	}
}
