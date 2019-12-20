//variables
int introans;
int roadMap;
string_t name;
string_t brotherName;
string_t fatherName;
int optionOne = 1;
int optionTwo = 2;
int optionThree = 3;
int optionOneAns;
int command;
int commandSpell;
int fight = randint(5, 10);
int heal = randint(15, 20);
int magicPoints = 32;
int health = 50;
int medicalHerb = randint(20, 25);
int herbCount = 3;
int wizardHealth = 60;
int wizardAttack = randint(10, 15);
int dwarfHealth = 150;
int dwarfAttack = randint(15, 20);
int dragonHealth = 70;
int dragonAttack = randint(20, 30);
//Fight Sequences
void wizardFight(){
    do{
        do{
            printf ("Command?\n");
            printf ("HP:%d  MP:%d\n", health, magicPoints);
            printf ("\
            1 - Fight\n\
            2 - Heal\n\
            3 - Medical Herb\n\n");
            scanf ("%d", &command);
        }while(command != 1 && command != 2 && command != 3);
        if(command==1){
            printf ("%s attacks!\n", name);
            printf ("The Wizard's health has been reduced by %d.\n\n", fight);
            wizardHealth=wizardHealth-fight;
            fight = randint(5, 10);
        }
        if(command==2){
            if(magicPoints>0){
                printf ("%s uses Heal!\n", name);
                printf ("You have recovered by %d Hit Points.\n", heal);
                health=health+heal;
                heal = randint (15, 20);
                printf ("%d", wizardHealth);
                magicPoints=magicPoints-4;
            }else{
                printf("You attempt to use Heal, but you are all out of\n\
magic points. Without any time to recover, ");
            }
        }
        if(command==3){
            if(herbCount>0){
            printf ("%s uses the medical herb.\n", name);
            printf ("You have recovered by %d Hit Points.\n", medicalHerb);
            health=health+medicalHerb;
            herbCount=herbCount-1;
            medicalHerb = randint (20, 25);
            }else{
                printf("You searched your bag for a medical herb...");
                printf("but you are all\nout of medical herbs. Without any time to recover, ");
             }
        }
    if(wizardHealth>0){
        printf ("The Wizard Attacks!\n");
        printf ("Your health has been reduced by %d.\n\n", wizardAttack);
        health = health-wizardAttack;
        wizardAttack = randint (10, 15);
    }
    }while(wizardHealth>0 && health>0);
    if(wizardHealth<=0){
    printf ("You have defeated the Wizard.");
    }
    if(health<=0){
        printf("You have died.");
    }
}
void dwarfFight(){
    int health = 60;
    int heal = randint(20, 25);
    int medicalHerb = randint(25, 30);
    do{
        do{
            printf ("Command?\n");
            printf ("HP:%d  MP:%d\n", health, magicPoints);
            printf ("\
            1 - Fight\n\
            2 - Heal\n\
            3 - Medical Herb\n\n");
            scanf ("%d", &command);
        }while(command != 1 && command != 2 && command != 3);
        if(command==1){
            printf ("%s attacks!\n", name);
            printf ("The Dwarf's health has been reduced by %d.\n\n", fight);
            dwarfHealth=dwarfHealth-fight;
            fight = randint(5, 10);
        }
        if(command==2){
            if(magicPoints>0){
                printf ("%s uses Heal!\n", name);
                printf ("You have recovered by %d Hit Points.\n", heal);
                health=health+heal;
                heal = randint (20, 25);
                printf ("%d", dwarfHealth);
                magicPoints=magicPoints-4;
            }else{
                printf("You attempt to use Heal, but you are all out of\n\
magic points. Without any time to recover, ");
            }
        }
        if(command==3){
            if(herbCount>0){
            printf ("%s uses the medical herb.\n", name);
            printf ("You have recovered by %d Hit Points.\n", medicalHerb);
            health=health+medicalHerb;
            herbCount=herbCount-1;
            medicalHerb = randint (25, 30);
            }else{
                printf("You searched your bag for a medical herb...");
                printf("but you are all\nout of medical herbs. Without any time to recover, ");
             }
        }
    if(dwarfHealth>0){
        printf ("The Dwarf Attacks!\n");
        printf ("Your health has been reduced by %d.\n\n", dwarfAttack);
        health = health-dwarfAttack;
        dwarfAttack = randint (5, 10);
    }
    }while(dwarfHealth>0 && health>0);
    if(dwarfHealth<=0){
    printf ("You have defeated the Dwarf.");
    }
    if(health<=0){
        printf("You have died.");
    }
}
void dragonFight(){
    int health = 150;
    int heal = randint(30, 35);
    int medicalHerb = randint(40, 45);
    do{
        do{
            printf ("Command?\n");
            printf ("HP:%d  MP:%d\n", health, magicPoints);
            printf ("\
            1 - Fight\n\
            2 - Heal\n\
            3 - Medical Herb\n\n");
            scanf ("%d", &command);
        }while(command != 1 && command != 2 && command != 3);
        if(command==1){
            printf ("%s attacks!\n", name);
            printf ("The Dragon's health has been reduced by %d.\n\n", fight);
            dragonHealth=dragonHealth-fight;
            fight = randint(5, 10);
        }
        if(command==2){
            if(magicPoints>0){
                printf ("%s uses Heal!\n", name);
                printf ("You have recovered by %d Hit Points.\n", heal);
                health=health+heal;
                heal = randint (30, 35);
                printf ("%d", dragonHealth);
                magicPoints=magicPoints-4;
            }else{
                printf("You attempt to use Heal, but you are all out of\n\
magic points. Without any time to recover, ");
            }
        }
        if(command==3){
            if(herbCount>0){
            printf ("%s uses the medical herb.\n", name);
            printf ("You have recovered by %d Hit Points.\n", medicalHerb);
            health=health+medicalHerb;
            herbCount=herbCount-1;
            medicalHerb = randint (30, 35);
            }else{
                printf("You searched your bag for a medical herb...");
                printf("but you are all\nout of medical herbs. Without any time to recover, ");
             }
        }
    if(dragonHealth>0){
        printf ("The Dragon Attacks!\n");
        printf ("Your health has been reduced by %d.\n\n", dragonAttack);
        health = health-dragonAttack;
        dragonAttack = randint (20, 30);
    }
    }while(dragonHealth>1 && health>0);
    if(dragonHealth<=0){
    printf ("You have defeated the Dragon.");
    }
    if(health<=0){
        printf("You have died.");
    }
}
//Other Functions
void cheatSheet(){
    printf("Would you like to see a roadmap for this game?\n");
    printf("\
    1 - Yes\n\
    2 - No\n\n");
    do{    
        scanf ("%d", &roadMap);
    }while(roadMap != 1 && roadMap != 2);
    if(roadMap==1){
        printf("                                              Introduction                                 \n");
        printf("                                      _______/      |      \\_______                       \n");
        printf("                                     /              |              \\                      \n");
        printf("                                    /               |               \\                     \n");
        printf("                                   /                |                \\                    \n");
        printf("                                  /                 |                 \\                   \n");
        printf("                                 /                  |                  \\                  \n");
        printf("                                /                   |                   \\                 \n");
        printf("                            Diamond           Golden Crown             Sword               \n");
        printf("                           __/ | \\__         /     |     \\         __/  |  \\__          \n");
        printf("                          /    |    \\       /      |      \\       /     |     \\         \n");
        printf("                         /     |     \\  Fight the  |    Ask the  /      |      \\         \n");
        printf("                        /      |      \\   Dwarf    |     Dwarf  /       |       \\        \n");
        printf("                       /       |       \\       Steel the       /        |        \\       \n");
        printf("                  Fight the    |     Ask the     Crown     Fight the    |      Ask the    \n");
        printf("                   Wizard      |      Wizard                 Dragon     |       Dragon    \n");
        printf("                               |                                        |                 \n");
        printf("                           Steel the                                Steel the             \n");
        printf("                            Diamond                                   Sword               \n\n");
    }
    
}
void intro(){
    printf ("Hello and welcome to your adventure story! What is your name?\n\n");
    scanf ("%s", &name);
    printf ("\nKing:\n");
    printf ("    'Hello, %s! I am King Erdrick of Tantagel Castle and you have been assigned \n\
    the task of retrieving one of three precious items. The first item is a diamond guarded \n\
    by a wizard. The second is a golden crown held safe by a dwarf. The last item is a \n\
    sword locked away in an dragons castle. Which item would you like to retrieve?'\n\n", name);
    printf ("Option\n\
    1 - The Diamond\n\
    2 - The Golden Crown\n\
    3 - The Sword\n\n");
    do{    
        scanf ("%d", &introans);
    }while(introans != 1 && introans != 2 && introans != 3);
    printf ("King:\n");
    printf ("\n    'Excellent choice!'\n");
    printf ("    'Return it to me and you shall make me proud!'\n");
    printf ("    'Here is a map of how to find it.'\n");
    printf ("    'But before you go, there are some things you should know. In case you choose to fight, \n\
    take this Iron Sword which will greatly increase your attack power.'\n\n");
    printf ("You have received an Iron Sword.\n\n");
    printf ("    'Also, take some medical herbs which will heal you while in battle.'\n\n");
    printf ("You have received 3 medical herbs.\n\n");
    printf ("King:\n");
    printf ("    'Lastly you will have spells that you will be able to use when in battle. \n\
    You only have a certain amount of magic points so use them wisely.'\n");
    printf ("    'Good Luck %s! And remember, if you try to use a medical herb or a spell\n\
    while in battle, but don't have any more medical herbs or magic points, you won't have\n\
    enough time to recover, so know when your out of your resources.'\n\n", name);
}

void happyFace(){
    printf("\n                                    _________________________                      \n");
    printf("                               _____                         _____                 \n");
    printf("                             __                                   __               \n");
    printf("                           __                                       __             \n");
    printf("                          _                                           _            \n");
    printf("                          _              ()           ()              _            \n");
    printf("                          _                                           _            \n");
    printf("                          _                                           _            \n");
    printf("                          _                                           _            \n");
    printf("                          _          \\                       /        _           \n");
    printf("                           __         \\_____________________/       __            \n");
    printf("                             __                                   __               \n");
    printf("                               _____                         _____                 \n");
    printf("                                    _________________________                      \n");
    printf("                            ____            ___            ____                    \n");
    printf("                           |    |           ___           |    |                   \n");
    printf("                           |____|           ___           |____|                   \n");
    printf("                               \\            ___            /                      \n");
    printf("                                \\           ___           /                       \n");
    printf("                                 \\          ___          /                        \n");
    printf("                                  \\         ___         /                         \n");
    printf("                                   \\        ___        /                          \n");
    printf("                                    \\       ___       /                           \n");
    printf("                                     \\      ___      /                            \n");
    printf("                                      \\     ___     /                             \n");
    printf("                                       \\    ___    /                              \n");
    printf("                                        \\   ___   /                               \n");
    printf("                                         \\  ___  /                                \n");
    printf("                                          \\ ___ /                                 \n");
    printf("                                           \\___/                                  \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                            ___                                    \n");
    printf("                                           /   \\                                  \n");
    printf("                                          /     \\                                 \n");
    printf("                                         /       \\                                \n");
    printf("                                        /         \\                               \n");
    printf("                                       /           \\                              \n");
    printf("                                      /             \\                             \n");
    printf("                                     /               \\                            \n");
    printf("                                    /                 \\                           \n");
    printf("                                   /                   \\                          \n");
    printf("                                  /                     \\                         \n");
    printf("                                 /                       \\                        \n");
    printf("                            ____/                         \\____                   \n");
}
//End Options
void option1A(){
    printf ("\nYou have decided to kill the Wizard.\n\n");
    printf ("You slowly creep forward and draw your sword. As you approach, the floor creeks and the Wizard awakes!\n\
You are about to strike but the Wizard dodges the blow and is now standing in front of you. The Wizard\n\
rolls to the left and grabs his sword. \n\n");
    printf ("You are now fighting the Wizard.\n\n");
}
void option1B(){
    printf ("\nYou have decided to steal the Diamond.\n\n");
    printf ("You tip-toe slowly past the Wizard and approach the Diamond. You lift up the glass container\n\
and gently put it down. You look behind you one last time only to see the Wizard still\n\
sleeping in his chair. You look back at the Diamond and reach towards it to pick it up.\n\
As you pick it up an alarm goes of which wakes up the Wizard. With the Diamond still in\n\
your hand, you run for the door, however, the Wizard blocks your path.\n\n");
    printf ("You are now fighting the Wizard.\n\n");
}
void option1C(){
    printf ("\nYou have decided to ask the Wizard for the Diamond.\n\n");
    printf ("You knock on the door and the Wizard awakes.\n\n");
    printf ("%s:\n", name);
    printf ("   'Excuse me sir, I was sent here by the King of Tantagel Castle and have\n\
    been asked to retrieve this Diamond of yours and return it to King Erdrick.'\n");
    printf ("Wizard:\n");
    printf ("   'I'm sorry, but I can't let you take this Diamond.\n");
    printf ("%s:\n", name);
    printf ("   'But King Erdrick has requested I return the Diamond.'\n");
    printf ("Wizard:\n");
    printf ("   'I don't know who that is nor do I care. You can't have this Diamond.\n");
    printf ("%s:\n", name);
    printf ("   'Well then I'm going to have to take it by force.'\n");
    printf ("Wizard:\n");
    printf ("   'Oh, I bet you will.'\n\n");
    printf ("You both grab your weapons and prepare to fight.\n\n");
    printf ("You are now fighting the Wizard.\n\n");
}
void option2A(){
    printf ("\nYou have decided to fight the Dwarf.\n\n");
    printf ("You draw your sword as the Dwarf walks in.\n\n");
    printf ("Dwarf:\n");
    printf ("   'Who are you and what do you want?'\n");
    printf ("%s:", name);
    printf ("\n   'YOUR MOM!'\n");
    printf ("Dwarf:\n");
    printf ("   'NOOOOO!'\n\n");
    printf ("The Dwarf reaches for his axe and prepares for a fight!\n\n");
    printf ("You are now fighting the Dwarf.\n\n");
}
void option2B(){
    printf ("\nYou have decided to steal the Crown.\n\n");
    printf ("You take the Crown and book it to the door. You are almost to the door until it closes all of a sudden!\n\
You turn around with the Crown in your hand facing an angry dwarf in full battle armor.\n\n");
    printf ("You are now fighting the Dwarf.\n\n");
}
void option2C(){
    printf ("\nYou have decided to ask the Dwarf for the Crown.\n\n");
    printf ("The Dwarf is startled as he sees an unexpected guest inside of his workshop.\n\n");
    printf ("%s:\n", name);
    printf ("   'I'm sorry, I didn't knock. I was sent here by the King of Tantagel Castle.\n\
    I have been asked to retrieve this Golden Crown of yours and return it to\n\
    King Erdrick.'\n");
    printf ("Dwarf:\n");
    printf ("   'And?'\n");
    printf ("%s:\n", name);
    printf ("   'It's the King.'\n");
    printf ("Dwarf:\n");
    printf ("   'So?'\n");
    printf ("%s:", name);
    printf ("\n   'So, I need that Crown.'\n");
    printf ("Dwarf:\n");
    printf ("   'Well, then you are going to have to take it from me by force.'\n\n");
    printf ("The Dwarf reaches for his sword. You draw yours in defence.\n\n");
    printf ("You are now fighting the Dwarf.\n\n");
}
void option3A(){
    printf ("\nYou have decided to kill the Dragon.\n\n");
    printf ("You slowly creep forward and draw your sword. As you creep towards the Dragon\n\
the Dragon's red eyes open! The Dragon shuffles backwards ready for a fight.\n\n");
    printf ("You are now fighting the Dragon.\n\n");
}
void option3B(){
    printf ("\nYou have decided to steal the Sword.\n\n");
    printf ("You slowly tip-toe around the Dragon, up the steps, and to the throne. You\n\
look back at the Dragon to see if it's still sleeping which it is. You pick\n\
up the Sword from the ground and start to head back through the palace doors.\n\
However, you forget that there are steps and you tumble down the stairs and\n\
the sword which you were carrying hits the ground with a large clang! The Dragon\n\
awakes and looks straight at you. You make your way to your feet and prepare for\n\
a fight.\n\n");
    printf ("You are now fighting the Dragon.\n\n");
}
void option3C(){
    printf ("\nYou have decided to ask the Dragon for the Sword. ");
    printf ("You slowly creep towards the Dragon. You tap it with your sword and the\n\
Dragon's eyes flutter open.\n\n");
    printf ("%s:\n", name);
    printf ("   'Excuse me, I was wondering if-'\n\n");
    printf ("Unable to finish your sencence the Dragon opens its mouth and eats you whole.\n\
You realize your stupid mistake too late.\n\n");
    printf ("You have died.");
}
//Options
void option1(){
    printf ("You have left Tantagel Castle and are now on your way to retrieve the Diamond.\n\n");
    printf ("Following your map, you approach a strange dark castle with an open gate. You\n\
enter and inside it's mostly dark but you see a light glimmering from underneath one of\n\
the doors. You open the door and see the diamond on a table, inside of a glass container\n\
with a small light shining over it. You walk towards it but stop suddenly noticing the\n\
wizard sleeping in his chair. You have the option to kill the wizard where he lies, sneak\n\
by the wizard and steal the diamond without him noticing, or wake up the wizard and ask him\n\
for the diamond. Which option would you like to choose?\n\n");
    printf ("Option\n\
    1 - Kill the Wizard\n\
    2 - Steal the Diamond\n\
    3 - Ask the Wizard for the Diamond\n\n");
    do{    
        scanf ("%d", &optionOneAns);
    }while(optionOneAns != 1 && optionOneAns != 2 && optionOneAns != 3);
    if(optionOneAns==1){
        option1A();
        wizardFight();
    }
    if(optionOneAns==2){
        option1B();
        wizardFight();
    }
    if(optionOneAns==3){
        option1C();
        wizardFight();
    }
}
void option2(){
    printf ("You have left Tantagel Castle and are now on your way to retrieve the Golden Crown.\n\n");
    printf ("Following your map, you approach a mine shaft. You enter and inside it's mostly dark\n\
but you see a light glimmering from underneath one of the rooms. You creep towards the room and\n\
see the Crown on a forge table. You look around but don't see anyone so you walk towards it cautiously.\n\
As you approach the Crown, you start to hear footsteps walking in your direction. You have the option\n\
to fight the Dwarf, take the Crown and run, or ask the Dwarf for the Crown. Which option would you \n\
like to choose?\n\n");
    printf ("Option\n\
    1 - Fight the Dwarf\n\
    2 - Steal the Golden Crown\n\
    3 - Ask the Dwarf for the Golden Crown\n\n");
    do{    
        scanf ("%d", &optionOneAns);
    }while(optionOneAns != 1 && optionOneAns != 2 && optionOneAns != 3);
    if(optionOneAns==1){
        option2A();
        dwarfFight();
    }
    if(optionOneAns==2){
        option2B();
        dwarfFight();
    }
    if(optionOneAns==3){
        option2C();
        dwarfFight();
    }
}
void option3(){
    printf ("You have left Tantagel Castle and are now on your way to retrieve the Sword.\n\n");
    printf ("Following your map, you approach an abandoned castle. You enter and inside it's completely\n\
dark other than the small amount of light entering from the windows. You walk around looking for the\n\
Sword but can't seem to find it. Knowing it's similar to a normal castle, but just abandoned, you\n\
enter the Throne Room. You walk in and see a Dragon sleeping in the middle of the floor. Behind it\n\
you see it. The Sword is on the ground right next to the throne. You have the option to kill the dragon,\n\
take the sword and run, or politely ask the dragon for the sword. Which option would you like to choose?\n\n");
    printf ("Option\n\
    1 - Fight the Dragon\n\
    2 - Steal the Sword\n\
    3 - Ask the Dragon for the Sword\n\n");
    do{    
        scanf ("%d", &optionOneAns);
    }while(optionOneAns != 1 && optionOneAns != 2 && optionOneAns != 3);
    if(optionOneAns==1){
        option3A();
        dragonFight();
    }
    if(optionOneAns==2){
        option3B();
        dragonFight();
    }
    if(optionOneAns==3){
        option3C();
    }
}
//Introduction
int main(){
    cheatSheet();
    intro();
    if(introans==optionOne){
        option1();
    }
    if(introans==optionTwo){
        option2();
    }
    if(introans==optionThree){
        option3();
    }
    happyFace();
}
