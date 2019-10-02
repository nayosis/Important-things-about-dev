---
layout: post
title:  "The functionnal way WIP!"
date:   2019-10-01 21:40:53 +0200
categories: functionnal dev
---


Parlons fonctionnel. Kesako et pourquoi ! 

Ici, le mot fonctionnel provient de fonction et pas du terme "fonctionnel" qui est la notion à laquelle votre programme doit répondre pour le besoin (sous entendu fonctionnel qui doit fonctionner). Genre les "spécifications fonctionnelles" ... 

Donc reprenons sur la base qu'est ce qu'une fonction:

> En mathématiques, une fonction peut se comprendre comme une combinaison d’opérations permettant de définir un résultat à partir de données initiales, de façon que les mêmes données donnent toujours le même résultat.
[wikipedia][wikipedia-Fonction] 


Je vais insister sur :
> [...] , de façon que les mêmes données donnent toujours le même résultat.

(Vous allez voir cela va induire plusieurs choses)

Dans un cas admettons que nous avions une liste de personne avec une date de naissance et on veux une liste de personne qui sont nés en 1985. 

![Ma Class Person](http://www.plantuml.com/plantuml/png/SoWkIImgAStDuKhEIImkLWX8BIhEpwlcKb08BYdAp4jNo4lCJGNoN19BKXMSCejACa0iX7HwQbvHge82LoqN5vT3QbuAq2G0)


Je suis javaiste, je vais le faire en java ! "A l'ancienne"

{% highlight java %}
public class MegaExample
{
    public List<Person> getPersonByYear(List<Person> persons, Integer birthYear){
        List<Person> persons2 = new ArrayList<Person>();
        for(person in persons){}
            if ( person.getdate().getYear().isEqual(birthYear)){
                persons2.add(person);
            }
        }
        return persons2;
    }
}
{% endhighlight %}


Et maintenant on veux aussi les filter par genre ! 

{% highlight java %}
public class MegaExample
{
    public List<Person> getPersonByYearAndByGender(List<Person> persons, Integer birthYear,String gender){
        List<Person> persons2 = new ArrayList<Person>();
        for(person in persons){}
            if ( person.getdate().getYear().isEqual(birthYear) && 
                person.getGender().isEqual(gender)){
                persons2.add(person);
            }
        }
        return persons2;
    }
}
{% endhighlight %}

Bon ca marche, cool ! Mais coté lisibilité c'est pas folichon ! Cote effet de bord c'est pareil !! Effet de quoi !!! Disons que si j'ai un truc null en paramètre, ca va être compliqué. 

....

{% highlight java %}
public class MegaExample
{

    public List<Person> getPersonByYearAndByGender(List<Person> persons, Integer birthYear,String gender){
        return persons.stream().filter(isGender(gender)).filter(isBirthYear(birthYear)).collect(Collectors.<Person>toList());
    }

    private Predicate<Person> isGender(String gender){
        return person -> person.getGender().isEquals(gender);
    }

    private Predicate<Person> isBirthYear(Integer birthYear){
        return person -> person.getYear().isEquals(birthYear);
    }

  
}
{% endhighlight %}



Parlons immutabilité


[wikipedia-Fonction]: https://fr.wikipedia.org/wiki/Fonction_(math%C3%A9matiques)
