# Creature Battle Project (OOP + Git Branching Practice)

This project is designed to help me learn object-oriented programming in Python — especially inheritance — while also practicing key Git concepts like branching, merging, conflict resolution, and version history.

I will begin with a base class (Creature) and create additional subclasses on separate Git branches to simulate a real development workflow.

---

##  Learning Objectives

### Python / OOP
- Understand and implement **classes**
- Use **inheritance** to extend behaviors
- Override and extend methods (e.g., `attack()`)
- Practice writing simple test code in `main`

### Git / Version Control
- Create and switch branches
- Merge branches into `main`
- Resolve merge conflicts
- View commit history (`git log --graph --all`)


---

## Project Structure
oop_creature_code/
│
├── creature_simulation.py # Base class + subclasses
└── README.md

## Project Structure

There is one base class and three subclasses.

Creature: mainly part is to store a creature's basic stats and let it fight, including with 4 main methods 1. init, store the name, hp and attack_power 2. attack, deal attack_power damage to a target creature 3. is_alive, check whether hp is above 0 4. str, return the creature name with current hp.

SwimmingCreature (inherits Creature): mainly part is to add a water-based movement and attack, including with 2 main methods 1. dive_to, set the creature's depth and print it 2. attack, override the base attack to print an underwater splash attack and clamp target hp at 0 instead of going negative.

FlyingCreature (inherits Creature): mainly part is to add an air-based movement and attack, including with 2 main methods 1. fly_to, set the creature's altitude and print it 2. attack, override the base attack to print an aerial swoop attack and clamp target hp at 0 instead of going negative.

FireCreature (inherits Creature): mainly part is to add a fire_level stat that boosts damage, including with 2 main methods 1. emit_fire, change fire_level if it's between 0 and 100, otherwise print an error and keep the old value 2. attack, override the base attack to add fire_level // 10 as bonus damage on top of attack_power.

How to Test and Run Your Program

Run the file directly with python creature_simulation.py. The if __name__ == "__main__": block runs 6 tests on the base Creature class (init, basic attack, overkill not going below 0, is_alive(), dead creature can't attack, multiple attacks), followed by tests for SwimmingCreature, FlyingCreature, and FireCreature covering their movement methods and their overridden attack().

I've tested the code and checked the printed "Expected" vs "Actual" values after each test, and it matches correctly for all the base Creature tests and the subclass tests.