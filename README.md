# Project - Specification and Description Language

<a href="https://www.pragmadev.com/">
  <img src="https://img.shields.io/badge/language-SDL-3dc1c6?style=flat-square" alt="laguage-SDL" />
</a>

---

For this project, we used <a href="https://www.pragmadev.com/">PragmaStudio</a> to use the language.

- To build the project, in the tree, right-click on the system and *Build*.
- To launch a simulation, in the tree structure, right-click on the system and *Debug*.

---

Initially our objective was simply to manage a protocol that receives data (here a string) from the user, inserts it into data messages (here a string with previous data) and delivers it on arrival.

<p align="center">
  <img src=/Documents/partie1.png alt="Partie 1" />
  <br><em>Packet transmission</em>
</p><br>


In the second part we had to insert a disruptive element. Between the protocol and the user, we add a layer that can split packets randomly. It must be able to split data messages as well as acknowledgements.

<p align="center">
  <img src=/Documents/partie2.png alt="Partie 2" />
  <br><em>Packet duplication</em>
</p><br>


Subsequently we complete the disruptive element which now has the possibility of losing packets.

<p align="center">
  <img src=/Documents/partie3.png alt="Partie 3" />
  <br><em>Packet loss</em>
</p><br>


After adding the possibility of duplicated packets and other lost packets, we need to make our protocol more reliable in order to deal with these error cases.
To do this we use the *alternating bit* principle, also known as *sliding window of size 1*.

<p align="center">
  <img src=/Documents/partie4-1.png alt="Partie 4-1" />
  <br><em>Alternating bit principle</em>
</p><br>

<p align="center">
  <img src=/Documents/partie4-2.png alt="Partie 4-2" />
  <br><em>Loss management with the timer</em>
</p><br>

<p align="center">
  <img src=/Documents/partie4-3.png alt="Partie 4-3" />
  <br><em>Starting and resetting the timer</em>
</p><br>

> **Warning**<br>
> To use the timer in the simulation, you have to activate it via the menu *Options → Timer → Real time timers*.
