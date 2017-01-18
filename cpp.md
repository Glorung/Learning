# Learning cpp #

## Définition d'une class ##

Une classe est comme une structure. On peut y définir des fonctions (membres)
et des variables (attributs). Elle se définie ainsi

class     exemple
{
  public:
    void  membreExemple (void);
  private:
    int   attribut;
};

Ici le terme public défini ce qui sera accessible en dehors de le class
et le terme private defini ce qui sera accessible seulement à l'intérieur de
la class.

## Utilisation d'une class ##

Une class peut être déclarée comme une variable, mais elle peut aussi prendre
des paramètres.

exempleClass    var;
ou
exempleClass    var("Hello world");

Afin de récupérer ces paramètres et de paramétrer la class lors de sa
déclaration on utilise un constructeur. Le constructeur d'une class doit
avoir le même nom que la class, et doit être définie en public au sein de la
class.

class     exempleClass
{
  public:
    exempleClass(char *name);
    private:
    char *      nomDeMaClass;
};

La définition et l'implémentation du constructeur se fait comme une fonction.
Sauf qu'elle n'a pas de valeur retour. (En réalité la valeur retour est la class
  crée).

exempleClass::exempleClass  (char *name)
{
  this->nomDeMaClass = name;
}
