## Portfolio

---
### Notable School Projects
#### Lambda Lifting
<!--- <img src="images/dummy_thumbnail.jpg?raw=true"/> -->
Lambda Lifting is the process of independently defining each function in a given program by "lifting" each function to a single global scope. This involves renaming all variables and functions to avoid any clashes while maintaining the meaning of the program, building a call graph that organizes function calls, then changing function calls to include any variables that the callee uses as arguments for the caller.
<br>
I used Haskell to Lambda Lift programs written in a simple language that consists of functions, variables, and "let" clauses. Here's an example:
```
fun main x y = let
  fun add p = add_to_x p
  fun add_to_x q = (add_to_y q) + x
  fun add_to_y q = q + y
in add y + x
```


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
