## Portfolio

---
### Notable School Projects
#### Lambda Lifting
<!--- <img src="images/dummy_thumbnail.jpg?raw=true"/> -->
Lambda Lifting is the process of independently defining each function in a given program by "lifting" each function to a single global scope. This involves renaming all variables and functions to avoid any clashes while maintaining the meaning of the program, building a call graph that organizes function calls, then changing function calls to include any variables that the callee uses as arguments for the caller.
<br>
We were tasked with writing a Haskell program that could lift a simple language consisting only of aritmethic, functions, variables, and "let" clauses.
<br><br>
Here's an example:
```
fun main x y z n =
  let
    fun f1 v = x + f2 v
    fun f2 j = let
      fun g2 b = b + f3 j
    in g2 y + f3 x
  fun f3 k = let
    fun g3 c = c * f1 k
   in g3 z
in f1 n

```
Then, the lifted program:
```
fun main x y z n = f1 n x y z
fun f1 v x y z = x + (f2 v x y z)
fun f2 j x y z = (g2 y j x y z) + (f3 x x y z)
fun g2 b j x y z = b + (f3 j x y z)
fun f3 k x y z = g3 z k x y z
fun g3 c k x y z = c * (f1 k x y z)
```
<br><br>
Frankly, this was the most dificult assignment of my university career. However, I aced it, and it is the reason I feel comfortable with Haskell.

---
#### Checkers in Haskell


---
#### Database Storage for Bessie Box
One of the group members in this project worked for [Bessie Box](https://bessiebox.com/), a meat delivery company. They needed a database storage system, and we got a project out of it.
We converted customer information from text files to a database hosted on [DigitalOcean](https://www.digitalocean.com/) while automating a lot of customer processes. The database itself was implemented in [PostgreSQL](https://www.postgresql.org/), and the app that connected to it used [Psycopg](https://www.psycopg.org/).

---
### Games & Apps

- [ZooStreet](/zoostreet.md)
- [Airy Plane](/airyplane.md)
- [Inator](/inator.md)

---

<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
