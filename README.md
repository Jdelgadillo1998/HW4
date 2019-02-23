# HW4
import java.util.*;

public class HW4 {
	static ArrayList<String> contacts = new ArrayList<String>();
	int menuOption;
	static int menu = 0;
	
		

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Scanner scan = new Scanner(System.in);

		menu();

	}

		public static void menu() {
		Scanner scan = new Scanner(System.in);
		System.out.println("Choose an option");
		System.out.println("1. Add a new contact");
		System.out.println("2. Update an existing contact");
		System.out.println("3. Delete a contact");
		System.out.println("4. List contacts in sorted order");
		System.out.println("5. Search for given contact by: first name, last name, or number");
		System.out.println("6. Quit");

		menu = scan.nextInt();
		do {
			switch (menu) {
			case 1:
				add();
				break;
			case 2:
				update();
				break;

			case 3:
				remove();
				break;

			case 4:
				sorted();
				break;

			case 5:
				search();
				break;

			case 6:
				menu = 6;
				break;

			default: menu();
			}

		}while (menu!=6);
	}
		
		
	public static void add() {
		Scanner scan = new Scanner(System.in);
		System.out.println("Please input new contact");
		contacts.add(scan.next());
		System.out.println("New contact added");
		System.out.println("Contact list now:");
		System.out.println(contacts);
		menu();
	}
	
	public static void update() {
		Scanner scan = new Scanner(System.in);
		System.out.println("Update contact:");
		//contacts.set
		System.out.println("Contact list now:");
		System.out.println(contacts);
		menu();
	}
	public static void remove() {

		Scanner scan = new Scanner(System.in);
		System.out.println("Choose contact to remove");
		contacts.remove(scan.next());
		System.out.println("New contact added");
		System.out.println("Contact list now:");
		System.out.println(contacts);
		menu();
	}
	public static void sorted() {
		Scanner scan = new Scanner(System.in);
		System.out.println("Contacts in sorted order");
		Collections.sort(contacts);
		System.out.println(contacts);
		menu();
	}
	
	public static void search() {
		
	}

}
