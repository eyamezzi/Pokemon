# Code Review – Projet Pokémon

### La classe `PokemonVector` n’est pas abstraite

La consigne demande une classe abstraite `PokemonVector` servant de base aux classes `Pokedex`, `PokemonParty` et `PokemonAttack`.

Cependant, dans le code actuel, `PokemonVector` peut être directement instanciée et ne contient aucune méthode virtuelle pure.

### Le Singleton `Pokedex` peut être copié

Le Singleton `Pokedex` peut actuellement être copié, ce qui permet de créer plusieurs instances à partir de l’instance existante.

Pour empêcher la copie et l’affectation, on peut utiliser :

```cpp
Pokedex(const Pokedex&) = delete;
Pokedex& operator=(const Pokedex&) = delete;
```

### Remarques Clean Code
Éviter les nombres magiques : la valeur `6` est utilisée directement dans `PokemonAttack`. Il serait préférable de la remplacer par une constante, par exemple `MAX_POKEMONS`.
### Conseils
Mettre un graphe UML dans le README.
Mettre des javadocs pour chaque classe.
### Conclusion

J’ai bien aimé la mise en forme globale du projet. Le projet est clair et bien organisé. Les améliorations proposées concernent principalement le Singleton, la classe PokemonVector et quelques aspects du Clean Code.
