# POO_Reto_2

Here we intend to model a garden with the OOP method.

```mermaid
classDiagram
    Plant <|-- Weed
    Plant <|-- Bush
    Plant <|-- Tree
    Gardener --> Garden
    Garden *-- Plant
    Flower *-- Bush
    Flower *-- Tree
    class Gardener{
      +str name
      +plant(Plant)
      +water(Plant)
      +fertilize(Plant)
      +pull(Weed)
      +prune(Tree)
    }
    class Garden{
      +list~Bush~ list_of_bushes
      +list~Tree~ list_of_trees
      +add_plant(Plant)
      +remove_plant(Plant)
    }
    class Plant{
      +str scientific_name
      +str specie
      +bool is_fertilized
      +bool is_hydrated
      +bool is_diseased
      +grow()
    }
    class Weed{
        +bool is_venomous
        +invade(Garden)
    }
    class Bush{
        +bool has_spikes
        +int number_of_flowers 
    }
    class Tree{
        +float height
        +bool is_perennial
        +int number_of_flowers
    }
    class Flower{
        +str color
        +bool has_odor
        +bool can_bloom
        +bloom()
    }
```
The gardener is in charge of most of the interactions with the plants in the garden, such as water, fertilize or even pull them. Here, the classes weed, bush and tree are all a kind of plant, and therefore inherit its methods. Weed isn't recognized as a member of the garden per se. The bushes and trees are meant to have flowers in order to be in the garden, and each flower has an specific time of the year to bloom.
