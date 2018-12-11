import java.util.Scanner;

public class battle 
{
	public static void main(String args[])
	{
		
	}
	
	public static void battleTrainer(Character player, Character trainer)
	{
		Scanner input = new Scanner(System.in);
		
		while(player.getPokemon().getCurrentHP() > 0 && trainer.getPokemon().getCurrentHP() > 0)
		{
			Pokemon p = player.getPokemon();
			Pokemon t = trainer.getPokemon();
			
			System.out.println(p.getName() + " HP: " + p.getCurrentHP() + " / " + p.getTotalHP());
			System.out.println("/n/n/n/n/n/n" + t.getName() + " HP: " + t.getCurrentHP() + " / " + t.getTotalHP());
			
			System.out.println("1. Attack");
			System.out.println("2. Potion");
			
			int userChoice = input.nextInt();
			if(userChoice == 1)
			{
				System.out.println("1. fast attack");
				System.out.println("2. heavy attack");
				int moveChoice = input.nextInt();
				
				if(moveChoice == 1)
				{
					int enemyMove = (int)(Math.random() * 2 + 1);
					if(moveChoice == enemyMove)
					{
						if(p.getSpeed() >= t.getSpeed())
						{
							p.fast(t);
							t.fast(p);
						}
						else
						{
							t.fast(p);
							p.fast(t);
						}
					}
					else
					{
						p.fast(t);
						t.heavy(p);	
					}
				}
				else
				{
					int enemyMove = (int)(Math.random() * 2 + 1);
					if(moveChoice == enemyMove)
					{
						if(p.getSpeed() >= t.getSpeed())
						{
							p.heavy(t);
							t.heavy(p);
						}
						else
						{
							t.heavy(p);
							p.heavy(t);
						}
					}
					else
					{
						t.fast(p);
						p.heavy(t);	
					}
				}
			}
			else if(userChoice == 2)
			{
				System.out.println("You used one potion, you have " + player.getNumPotions() - 1 + " left");
				player.setNumPotions(player.getNumPotions() - 1);
				p.setCurrentHP(p.getCurrentHP() + 20);
			}
		}
	}
}
