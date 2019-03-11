# Example I

(Playground to learn RestDesc)

to run:

```$xslt
npm -g install h-eye

hes serve ./workspace
```

## 3 sailors

This is the use case I used back in 2012. At that time I was not aware of the N3 reasoner, and I had to use a less powerful abstraction called semantic decision tables. 

This time I will use RestDesc to show [The 3 sailor's story](https://www.slideshare.net/cristianvasquez/social-emergent-semantics-for-personal-data-management) as example

Each sailor counts with an:

* a vocabulary that makes sense to each of them. (ex_1, ex_2 and ex_3) 

* personal data space
    * [greek sailor annotation space](workspace/greek/1_greek.n3), and some [rules](workspace/greek/1_greek_rules.n3)
    * [british sailor annotation space](workspace/british/2_british.n3), and some [rules](workspace/british/2_british_rules.n3)
    * [slavic sailor annotation space](workspace/slavic/3_slavic.n3), and some [rules](workspace/slavic/3_slavic_rules.n3)

The also commit to a blackboard called bar, that:

* holds some agreed [common-sense rules](workspace/bar/bar_rules.n3) 
* provides an [API](workspace/bar/bar_api.n3)
* is at an [initial state](workspace/bar/bar_initial_state.n3).

Each sailor use applications that already agree on one vocabulary (ex) 

## Context

The sailors enjoy talking about:

### Global semantics

Practical things:

* Geographical Information
* Journey advice
* Weather
* Hazzards

### Personal semantics

And not so practical things:

* Histories about their trips
* Gossip
* Big sea monsters
* Phantom Ships
* Mermaids

### Artifacts

These sailors would like to share information about: 

* Maps
* Drawings
* Travel Logs

Which are useful to their community of sailors

### Devices

Sailor count with advanced technological devices that they use to record and store:

* movies
* photographs
* sound
* geographical information

On all their journeys

### Problem

Sailors would like to share information with other sailors.

The problem:

* Every sailor has its own way of organizing information
* Is difficult to find their own information
* Data is not well structured

### Metadata

Sailors can attach data to other data. Here we define metadata as a triadic relationship, where an additional node is created to contain information of the associative link itself.

```

<www.example.org/annotation/1> a ex:Annotation ;
    ex:hasSource  <www.example.org/travel/log/january> ;
    ex:hasTarget  <www.example.org/sea/mermaid/2> ;
    ex:hasContent  "A dangerous mermaid" ;
    ex:author <www.example.org/sailor/british> .

```

Note that in this way we can:

* define more complex annotation structures via SHACL.
* attach administrative metadata to the association, for management purposes.

### Annotation types

Sailors can use several artifacts to annotate their metadata

* Simple models, such as taxonomies
* Coordinates
* Tags

#### Actors

Three sailors that want to share the pictures and geographical position of the mermaids they've seen.

Sailor 1 (Greek)

* These creatures are called seirenes
* They live in the sea
* They are woman
* They have beautiful and long hair
* They have enchanting voices
* They do not have fish-like tail

Sailor 2 (British Isles)

* These creatures are called mermaids
* They live in the sea
* They are woman
* They can be giant
* They don't have immortal soul
* They do have fish-like tail

Sailor 3 (Slavic)

* These creatures are called rusalkas
* They live in the sea
* They are woman
* They do not have a fish-like tail
* They are beautiful young women with long green hair