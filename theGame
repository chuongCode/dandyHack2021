import java.util.Scanner;
import java.lang.Math;

public class theGame {
	public static int day = 0;
	
	//player
	public static String playerName;
	public static int playerHP = 10;
	public static int choice;
	public static int playerPhysical = 1;
	public static int playerMagical = 2;
	public static int savePlayerHP;
	public static int savePlayerPhysical;
	public static int savePlayerMagical;
	int engineerBoost = 2;
	public static boolean onFire = false;
	//enemy
	public static int enemyHP;
	public static int enemyAttack;
	
	public static void victory() {
		System.out.println("[Congratulations! You've defeated the enemy! Time to venture onwards.]");
	}
	
	public static void defeat() {
		System.out.println("[You've been defeated. Unfortunately, this is the end of your journey...]");
		System.out.println("|------------------------------------|\n"
				+ "				GAME OVER.");
	}
	
	public static void savePlayer() {
		savePlayerHP = playerHP;
		savePlayerPhysical = playerPhysical;
		savePlayerMagical = playerMagical;
	}
	
	public static void revive() {
		System.out.println("[You have been lifted up by the spirit of Meliora!]\n");
		playerHP = savePlayerHP;
		playerPhysical = savePlayerPhysical;
		playerMagical = savePlayerPhysical;
		
	}
	public static void displayPlayer() {
		System.out.println("~Your stats: " + playerHP + " HP, " + playerPhysical + " Physical Power, " + playerMagical + " Magical Power~");
	}
	public static void yellowjacketBattle() {
		do {
			displayYellowjacket();
			displayPlayer();
			battleChoices();
			if (choice == 1) {
			physicalAttackPrompt();
			yellowjacketStrike();
			}
			else if (choice == 2) {
				magicalAttackPrompt();
				yellowjacketStrike();
			}
			else if (choice == 3) {
			System.out.println("You can't run from this fight, it's the first one!");
			yellowjacketStrike();
			}	
		} while (enemyHP > 0 && playerHP > 0);
		if(enemyHP <= 0) {
			victory();
			userContinue();
		}
		else if(playerHP <= 0) {
			defeat();
			System.out.println("Sarah Mangelsdorf: This can't already be your end! Get up!");
			revive();
			yellowjacketBattle();
		}
	}
	
	public static void doctorBattle() {
		do {
			displayDoctor();
			displayPlayer();
			battleChoices();
			if (choice == 1) {
			physicalAttackPrompt();
			doctorStrike();
			}
			else if (choice == 2) {
				magicalAttackPrompt();
				doctorStrike();
			}
			else if (choice == 3) {
			System.out.println("You can't run from this fight, Dr. ChatBot will follow you everywhere!");
			doctorStrike();
			}	
		} while (enemyHP > 0 && playerHP > 0);
		if(enemyHP <= 0) {
			victory();
			userContinue();
		}
		else if(playerHP <= 0) {
			defeat();
			System.out.println(playerName + ": How could this be... I can't fall here...");
			System.out.println("[However, you remember that you ate an apple earlier today, keeping the doctor away!]");
			System.out.println("[With apple coursing through your veins, the Dr. fails to finish you off!] ");
			revive();
			doctorBattle();
		}
	}
	
	public static void doctorStrike() {
		double promptChance;
		promptChance = (int)(Math.random() * 10);
		if(promptChance >= 0 && promptChance <= 2) {
			System.out.println("Dr. ChatBot sends a reminder notification text and email, bothering you and dealing " + enemyAttack + " damage!");
			System.out.println("Dr. ChatBot: REMINDER! You must complete your Dr. Chat Bot today because you live on campus!");
			playerHP -= enemyAttack;
		}
		else if(promptChance >= 3 && promptChance <= 5) {
			System.out.println("Dr. ChatBot slips past another one of your created filters, buffing her damage by 3!");
			System.out.println("Dr. Chatbot: Would you like to receive Dr. Chat Bot text messages?!! ");
			enemyAttack += 3;
		}
		else if(promptChance >= 6 && promptChance < 9) {
			System.out.println("Dr. ChatBot enters your End User Digest, finding another way to spam you, dealing 1 damage, and repeating its own turn!");
			System.out.println("\"[EXT] DrChatBot - Reminder Notification issued at NOW AM\"");
			playerHP--; 
			doctorStrike();
		}
		else if(promptChance == 9) {
			System.out.println("Dr. ChatBot has falsely deemed you potentially contagious! You've been quarantined, halving your health! Critical Strike!");
			System.out.println("Dr. ChatBot: Looks like you've been travelling outside the US within the last 10 days!");
			playerHP /= 2;
		}
		System.out.println("");
	}
	
	public static void displayDoctor() {
		System.out.println("~Dr. ChatBot stats: " + enemyHP + " HP, " + enemyAttack + " Power~");
	}
	
	public static void displayYellowjacket() {
		System.out.println("~Yellowjacket stats: " + enemyHP + " HP, " + enemyAttack + " Power~");
	}
	
	public static void battleChoices() {
		Scanner scnr = new Scanner(System.in);
		System.out.println("|------------------------------------|");
		System.out.println("[Select your integer choice.]");
		System.out.println("1.) Physical Attack");
		System.out.println("2.) Magical Attack");
		System.out.println("3.) Run away!");
		System.out.println("|------------------------------------|");
		choice = scnr.nextInt();
	}
	
	public static void wifiBattle() {
		do {
			displayWifi();
			displayPlayer();
			battleChoices();
			if (choice == 1) {
			physicalAttackPrompt();
			wifiStrike();
			}
			else if (choice == 2) {
				magicalAttackPrompt();
				wifiStrike();
			}
			else if (choice == 3) {
			System.out.println("You can't run from this fight, you're stuck in the virtual world!");
			wifiStrike();
			}	
		} while (enemyHP > 0 && playerHP > 0);
		if(enemyHP <= 0) {
			victory();
			userContinue();
		}
		else if(playerHP <= 0) {
			defeat();
			System.out.println("UR_Connected: ...Rebooting... Rebooting...");
			System.out.println("[It seems like you're getting a second chance! UR_Connected's crappy connection is finally coming in handy!]");
			revive();
			wifiBattle();
		}
	}
	
	public static void demonBattle() {
		do {
			displayDemon();
			displayPlayer();
			battleChoices();
			if (choice == 1) {
			physicalAttackPrompt();
			demonStrike();
			}
			else if (choice == 2) {
				magicalAttackPrompt();
				demonStrike();
			}
			else if (choice == 3) {
			System.out.println("You can't run from the IRS!");
			demonStrike();
			}	
		} while (enemyHP > 0 && playerHP > 0);
		if(enemyHP <= 0) {
			victory();
			userContinue();
		}
		else if(playerHP <= 0) {
			defeat();
			System.out.println("Out of nowhere though, The Debt Demon spares your pitiful life for you to fight again!");
			System.out.println("\"Your insignificant life is puny, but it is fun to watch you squirm. Stand! Face me again!\"");
			revive();
			demonBattle();
		}
	}
	public static void displayDemon() {
		System.out.println("<Overlord Debt Demon's stats: " + enemyHP + " HP, " + enemyAttack + " Power>");
	}
	
	public static void demonStrike() {
		double promptChance;
		promptChance = (int)(Math.random() * 10);
		if(promptChance >= 0 && promptChance <= 2) {
			System.out.println("The Debt Demon charges you interest, dealing " + enemyAttack + " damage!");
			System.out.println("Overlord Debt Demon: Submit.");
			playerHP -= enemyAttack;
			if(onFire == true) {
				System.out.println("The fire burns you! 1 damage!");
				playerHP--;
			}
		}
		else if(promptChance >= 3 && promptChance <= 5) {
			System.out.println("The Debt Demon sends fireballs of tax notices, striking you for 3 damage and setting you on fire!");
			System.out.println("Overlord Debt Demon: All will fall.");
			if(onFire == true) {
				System.out.println("The fire burns you! 1 damage!");
				playerHP--;
			}
			onFire = true;
			playerHP -= 3;
			
		}
		else if(promptChance >= 6 && promptChance < 9) {
			System.out.println("The Debt Demon investigates any fallacies in your records, lowering your stats by 2!");
			System.out.println("Overlord Debt Demon: The end draws near.");
			playerPhysical -= 2;
			playerMagical -= 2;
			if(onFire == true) {
				System.out.println("The fire burns you! 1 damage!");
				playerHP--;
			}
		}
		else if(promptChance == 9) {
			System.out.println("The Debt Demon sends unreasonable repayment plans to your mailbox. They take a toll on your mental state, HALVING your stats!");
			playerPhysical /= 2;
			playerMagical /= 2;
			if(onFire == true) {
				System.out.println("The fire burns you! 1 damage!");
				playerHP--;
			}
		}
		System.out.println("");
	}
	
	public static void displayWifi() {
		System.out.println("~UR_Connected stats: " + enemyHP + " HP, " + enemyAttack + " Power~");
	}
	
	public static void wifiStrike() {
		double promptChance;
		promptChance = (int)(Math.random() * 10);
		if(promptChance >= 0 && promptChance <= 2) {
			System.out.println("UR_Connected sends a denial of service attack, dealing " + enemyAttack + " damage!");
			System.out.println("UR_Connected: U r NoT cOnNeCtEd!");
			playerHP -= enemyAttack;
		}
		else if(promptChance >= 3 && promptChance <= 5) {
			System.out.println("UR_Connected slows down your connection, dealing no damage, but decreasing your physical & magical stats! -1 for both!");
			System.out.println("UR_Connected: FeElInG a LiTtLe SlOw?");
			playerPhysical--;
			playerMagical--;
		}
		else if(promptChance >= 6 && promptChance < 9) {
			System.out.println("UR_Connected freezes up, doing literally nothing. Classic.");
			System.out.println("UR_Connected: HaVe YoU tRiEd ThE oThEr NeTwOrKs YeT?");
		}
		else if(promptChance == 9) {
			System.out.println("UR_Connected lags, preventing you from sending an email saying \"I would like an extension on the project, as my pet goldfish Goku drowned\"");
			System.out.println("This deals critical damage for some reason, dealing " + enemyAttack * 2 + " damage!");
			System.out.println("UR_Connected: I'M sOrRy FoR yOuR lOsS... nOt!");
			playerHP -= enemyAttack * 2;
		}
		System.out.println("");
	}
	public static void yellowjacketStrike() {
		double promptChance;
		promptChance = (int)(Math.random() * 10);
		if(promptChance >= 0 && promptChance <= 2) {
			System.out.println("The yellowjacket stings you, dealing " + enemyAttack + " damage!");
			playerHP -= enemyAttack;
		}
		else if(promptChance >= 3 && promptChance <= 5) {
			System.out.println("The yellowjacket buzzes in your ear, dealing no damage, but annoying the heck out of you!");
		}
		else if(promptChance >= 6 && promptChance <= 9) {
			System.out.println("The yellowjacket sharpens their stringer, dealing no damage, but strengthening his power!");
			enemyAttack++;
		}
		System.out.println("");
	}
	
	public static void physicalAttackPrompt() {
		double promptChance;
		promptChance = (int)(Math.random() * 10);
		if(promptChance >= 0 && promptChance <= 1) {
			System.out.println("You bonk the enemy on the head with your meaty claws, dealing " + playerPhysical + " damage!");
			enemyHP -= playerPhysical;
		}
		else if(promptChance == 2) {
			System.out.println("You poke the enemy as hard as you can, inconveniencing them, but only dealing 1 damage!");
			enemyHP--;
		}
		else if(promptChance >= 3 && promptChance <= 4) {
			System.out.println("You kick the enemy in the butt, dealing " + playerPhysical + " damage!");
			enemyHP -= playerPhysical;
		}
		else if(promptChance == 5) {
			System.out.println("You hit them with the ol' banana swirl one two, dealing " + playerPhysical + " damage!");
			enemyHP -= playerPhysical;
		}
		else if(promptChance >= 6 && promptChance <= 7) {
			System.out.println("You yell as loud as you can at the enemy, dealing " + playerPhysical + " damage!");
			enemyHP -= playerPhysical;
		}
		else if(promptChance == 8) {
			System.out.println("You throw a chair at the enemy, dealing " + playerPhysical + " damage!");
			enemyHP -= playerPhysical;
		}
		else if(promptChance == 9) {
			System.out.println("CRITICAL STRIKE! You do a backflip and perfectly land it. The sheer epicness of it causes the enemy to spontaneously combust, dealing " + (playerPhysical * 2) + " damage!");
			enemyHP -= playerPhysical * 2;
		}
	}
	public static void marketChoices() {
		System.out.println("");
		Scanner scnr = new Scanner(System.in);
		System.out.println("1.) Milk +20 Physical Strength");
		System.out.println("2.) Chili Mac +10 Health");
		System.out.println("3.) Pickle Juice +30 Magical Capacity");
		System.out.println("4.) Questionable Corndog +20% Chance of Food Poisoning");
		choice = scnr.nextInt();
		while(choice != 4) {
			System.out.println("You can't afford that.");
			marketChoices();
		}
	}
	public static void hillsideMarket() {
		System.out.println("[You arrive at Hillside Market.]");
		System.out.println(playerName + ": Man. My wallet sure does feel fat. I can't wait to see what I can buy at Hillside.");
		System.out.println("[You look at the options and survey what you may want to buy.]");
		marketChoices();
	}
	public static void travelCampusCenter() {
		Scanner scnr = new Scanner(System.in);
		System.out.println("[Select a place to travel from Eastman Quad]");
		System.out.println("1.) Danforth Dining Hall");
		System.out.println("2.) Flag Lounge");
		System.out.println("3.) Hillside Market");
		choice = scnr.nextInt();
		if (choice == 1) {
			System.out.println("[Danforth has been abandoned for centuries. There is nothing but cobwebs and tumbleweeds. Let's find somewhere else to go.]");
			travelCampusCenter();
		}
		else if (choice == 2) {
			System.out.println("[What flags? There were flags? Never heard of 'em. Find somewhere else to travel.]");
			travelCampusCenter();
		}
		else if (choice == 3) {
			hillsideMarket();
		}
		else {
			System.out.println("That wasn't a choice ding dong. You're going to Hillside Market.");
		}
	}
	public static void magicalAttackPrompt() {
		double promptChance;
		promptChance = (int)(Math.random() * 10);
		if(promptChance == 0) {
			System.out.println("You throw a bunsen burner and blast the enemy, dealing " + playerMagical + " damage!");
			enemyHP -= playerMagical;
		}
		else if(promptChance == 1) {
			System.out.println("You force the enemy to eat the Eastman Dining Hall moldy chicken, dealing " + playerMagical + 1 + " damage!");
			enemyHP -= playerMagical + 1;
		}
		else if(promptChance >= 2 && promptChance <= 4) {
			System.out.println("You toss a beaker of dilluted acid at the enemy, dealing " + (playerMagical - 1) + " damage!");
			enemyHP -= playerMagical - 1;
		}
		else if(promptChance == 5) {
			System.out.println("You electrify the enemy with a Tesla coil, dealing " + playerMagical + 2 + " damage!");
			enemyHP -= playerMagical + 2;
		}
		else if(promptChance >= 6 && promptChance <= 7) {
			System.out.println("You shoot a laser pointer at the enemy, dealing " + (playerMagical - 2) + " damage!");
			enemyHP -= playerMagical - 2;
		}
		else if(promptChance == 8) {
			System.out.println("You stare at the enemy really hard... dealing like 1 damage!");
			enemyHP--;
		}
		else if(promptChance == 9) {
			System.out.println("CRITICAL STRIKE! You read out a calculus textbook, boring the enemy to death, dealing " + playerMagical * 2 + " damage!");
			enemyHP -= playerMagical * 2;
		}
	}
	
	public static void userContinue() {
		Scanner scnr2 = new Scanner(System.in);
		System.out.println("Press 0 to continue.");
		int userInput;
		userInput = scnr2.nextInt();
		while(userInput != 0) {
			userInput = scnr2.nextInt();
		}
		System.out.println("");
		
	}
	
	
	public static void nextDay() {
		
		System.out.println("[Day " + day + "]");
		day++;
	}
	
	//MAIN EXECUTE GAME
	public static void main(String[] args) {
		
		System.out.println("Enter your name:");
		Scanner scnr = new Scanner(System.in);
		playerName = scnr.nextLine();
		
		//Introduction
		System.out.println("Dear " + playerName + ",\n\n"
				+ "Congratulations! On behalf of the Office of Admissions, it is my honor to offer you admission to the Fall 2021 semester at the University of Rochester. But this acceptance is no ordinary admissions letter. "
				+ "\nYour acceptance is a testament to your divine might, magical affinity, and commitment to employing the gallantry reminiscent of the heroes of old against evil. \nAs a result, we feel you are an excellent match for our campus mission and have been tasked with the Eastman Initiative. \n\n"
				+ "The Eastman initiative is our institution’s mission to vanquish the darkness that is ignorance. Your assignment to this mission represents our trust in your potential to save our campus." 
				+ "\nIn order to train you for the hard journey that lies ahead, our war-hardened faculty will instruct you in the art of combat.\n\n"
				+ "Again, congratulations on your acceptance. I look forward to welcoming you on campus this fall as a part of University of Rochester’s 171st class!\n");
		
		//User confirmation to continue
		userContinue();
		
		//Player Customization
		System.out.println("[Welcome " + playerName + ".]");
		System.out.println("[It's time to select your major! Enter your integer choice:]");
		System.out.println("1.) Computer Science [Master of Spaghetti Code. You gain a suit of armor made of curly brackets: {} +5 Health]\n"
				+ "2.) Engineering [Tinkerer of Toys. You gain a makeshift sword: 0//[===> +2 Physical Attack]\n"
				+ "3.) Chemistry [Wizard of the Elements. You gain a flask to hold chemicals: ( )=o +3 Magical Attack]\n"
				+ "4.) Undecided [Mysterious as heck. You literally gain nothing. +0 Everything]");
		choice = scnr.nextInt();
		if (choice == 1) {
			playerHP += 5;
			System.out.println("Beep Boop Bop. You are a robot.");
		}
		else if (choice == 2) {
			playerPhysical += 2;
			System.out.println("You're an engineer. You solve problems.");
		}
		else if (choice == 3) {
			playerMagical += 3;
			System.out.println("Yeesh. I would not want be the one having to take O-Chem.");
		}
		else if (choice == 4) {
			System.out.println("Truly, you are the bravest of them all.");
		}
		else {
			System.out.println("That wasn't a choice, numbnut. You're getting undecided.");
		}
		userContinue();
			
		//Tutorial
		nextDay();
		System.out.println("*You awaken in front of Rush Rhees Library on the Eastman Quad*\n"
				+ "[It's time for Orientation...]\n");
		userContinue();
		
		System.out.println("Sarah Mangelsdorf: \"You're finally awake, huh.\n"
				+ "You're shorter than I expected.\" \n");
		userContinue();
		
		System.out.println("Sarah Mangelsdorf: It's time to learn the basics of battle. Prepare yourself!");
		userContinue();
		
		System.out.println("[You are attacked by a yellowjacket!]");
		enemyHP = 10;
		enemyAttack = 2;
		savePlayer();
		yellowjacketBattle();
		//End of Yellowjacket Battle Introduction

		//Level Up!
		System.out.println("[You've grown as a warrior. +5 Health, +2 Physical Strength, +1 Magical Capacity.]");
		playerHP += 5;
		playerPhysical += 2;
		playerMagical++;
		
		System.out.println("[You've gained a yellowjacket stinger! Your physical strength grows by 1.]");
		playerPhysical++;
		System.out.println("Sarah Mangelsdorf: Took you long enough. You still have a lot to learn...");
		System.out.println("Sarah Mangelsdorf: I'll be having you explore the campus in order for you to grow your experience as a person. Good luck to you.");
		userContinue();
		travelCampusCenter();
		//The player finally tries buying a corndog
		System.out.println("Aw man. I still can't buy this cheap corn dog. I'm so hungry after fighting...");
		System.out.println("\n[A mysterious figure walks up to the register]");
		System.out.println("Mysterious Figure: I'll be paying for them. *They say while pointing at you.*");
		userContinue();
		
		System.out.println(playerName + ": Who are you? Why are you being so generous?");
		userContinue();
		
		System.out.println("Mysterious Figure: I am your roommate! My name is Djimbieculus Brown. But people call me Sussus Amogus!\n");
		System.out.println(playerName + ": I'll call you Jim.");
		userContinue();
		
		System.out.println(playerName+ ": Well Jim, thank you for buying me this VERY questionable corn dog. I'll be happily enjoying this outside.");
		System.out.println("[You look down at your hand to prepare to bite your delicious dog.]");
		System.out.println("[But something's not right...]");
		userContinue();
		
		System.out.println("[Your corndog is gone! And not only that, your attention gets drawn to someone eating something loudly!]");
		System.out.println(playerName + ": Hey! A yellowjacket just stole my corndog! Give that back you fiend!");
		System.out.println("[You prepare for battle against a yellowjacket once again.]");
		userContinue();
		enemyHP = 10;
		enemyAttack = 2;
		savePlayer();
		yellowjacketBattle();
		//End of Yellowjacket Battle #2
		
		//Level up!
		System.out.println("[You've grown as a warrior once again. +4 Health, +2 Physical Strength, +1 Magical Capacity]");
		playerHP += 4;
		playerPhysical += 2;
		playerMagical++;
		userContinue(); 
		
		System.out.println(playerName + ": Man. I'm getting sick of getting attacked by Yellowjackets! And I can't believe I'm already behind on work on the first day of school!");
		System.out.println(playerName + ": I'm going to the library to study for my next exam!");
		userContinue();
		
		System.out.println("[You pull out your laptop to begin preparing for your exam.]");
		System.out.println("[But something isn't quite right...]");
		userContinue();
		
		System.out.println(playerName + ": My laptop isn't connecting to the wifi... Why is the WiFi so terrible!");
		System.out.println(playerName + ": It's time to put an end to this buffoonery. It's time for me to step in...");
		userContinue();
		
		System.out.println("[You leap into the technological realm that lies in the 1's and 0's of your laptop, landing yourself in a world unknown.]");
		System.out.println("[And there in front of you stands the virtual manifestation of UR_Connected.]");
		userContinue();
		
		System.out.println("UR_Connected: No OnE hAs EvEr MaDe OuT oF hErE aLiVe, FoOl. PrEpArE fOr YoUr DeMiSe.");
		System.out.println("[It's time to put an end to the madness that is the school WiFi.]");
		userContinue();
		enemyHP = 17;
		enemyAttack = 3;
		savePlayer();
		wifiBattle();
		//End of UR_Connected Battle
		
		//Level Up!
		System.out.println("[You feel courage pumping through you. +6 Health, +2 Physical Strength, +2 Magical Capacity]");
		playerHP += 6;
		playerPhysical += 2;
		playerMagical += 2;
		userContinue(); 
		
		System.out.println(playerName + ": Looks like I'll be sticking to using Ethernet cables from here on out...");
		userContinue();
		
		System.out.println("[You exit the library content with your victory over UR_Connected]");
		System.out.println("[You head to your assigned dormitory to finally rest for the day.]");
		userContinue();
		
		nextDay();
		System.out.println("[Waking up in the morning, you remember that you were expecting a package in the mail center.]");
		System.out.println("[You check your email in order to see if you can find a package notification. But something doesn't seem right...]");
		userContinue();
		
		System.out.println("[Scouring through the sea of Dr.Chatbot emails prompting you to fill out the health survey, you cannot seem to locate your mail confirmation for twenty-seven Lightning Mcqueen Action Figures!]");
		System.out.println(playerName + ": This is ridiculous! I've already filled out the survey multiple times! Why do they need to keep prompting me several times a day?");
		System.out.println("[Fueled with mild annoyance bordering on pure rage, you decide to take matters into your own hand...]");
		userContinue();
		
		System.out.println("[You track down Dr. ChatBot throughout UHS' entire faculty directory and managed to locate an office belonging to one Chattimus Bothalamew...]");
		System.out.println("0.) It's time to end this...");
		userContinue();
		
		System.out.println("[You burst into the office! Dr. ChatBot is sitting in her seat, seemingly having expected your arrival.]");
		System.out.println("Dr. ChatBot: In the past 24 hours, have you had any of the symptoms below that are new or unusual for you?");
		System.out.println("[It's time to battle...] * EPIC MUSIC ENSUES *");
		userContinue();
		
		enemyHP = 20; 
		enemyAttack = 5;
		savePlayer();
		doctorBattle();
		
		//Level Up!
		System.out.println("[You feel like you embody the school's motto. You feel Ever Better! +15 Health, +4 Physical Strength, +4 Magical Capacity]");
		playerHP += 15;
		playerPhysical += 4;
		playerMagical += 4;
		userContinue(); 
		
		System.out.println("FOUR YEARS LATER");
		userContinue();
		System.out.println("[You have graduated, Congratulations! You are now ready to enter the real world! But don't forget, you have student debt! You gotta pay that off eventually!]");
		userContinue();
		System.out.println("FOUR MORE YEARS LATER");
		userContinue();
		System.out.println("[You have a job, You are married, and you are establish a museum of fine culinary arts in Cheboygan, Michigan, so you go to take out a loan. The loan is denied! How could this be!]");
		System.out.println("[You get reminded! You are in crippling student debt!]");
		userContinue();
		System.out.println("[Literally too angry to take no as an answer, you decide to physically manifest Student Debt itself and settle the score]");
		System.out.println("[You gather the necessary ingredients: the hair of a first gen student, the eyeball of a Wilson Quad groundhog, and 3 grams of whey protein. The ritual to summon the demon of Student Debt is about to begin]");
		userContinue();
		
		System.out.println("[A streak of thunder flashes through the sky, and suddenly, the demon of Student Debt appears before you]");
		enemyHP = 25;
		enemyAttack = 7;
		savePlayer();
		demonBattle();
		
		System.out.println("[As the demon of all your debts falls to the ground, you feel a sense of relief wash over you.]");
		System.out.println("[The culmination of all your efforts, your experiences, your learning here at Rochester.]");
		System.out.println("[And yet, you finally realize something at the end of all of your tribulations...]");
		userContinue();
		
		System.out.println("Sometimes, it's about the friends we made along the way.");
		System.out.println("   ++ *\r\n"
				+ "  +  +*	*\r\n"
				+ " +    +*	* *\r\n"
				+ "+xxxxxx+	* * *\r\n"
				+ "|      | * *  *Congratulations " + playerName + "!\r\n"
				+ "|      | *	You've won the game! The End.\r\n"
				+ "|      |\r\n"
				+ "xxxxxxxx");
	}

}
