# POO_Reto_2

´´´classDiagram
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
    }´´´
    
