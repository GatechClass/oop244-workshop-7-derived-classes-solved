# oop244-workshop-7-derived-classes-solved
**TO GET THIS SOLUTION VISIT:** [OOP244-Workshop 7 Derived Classes Solved](https://mantutor.com/product/oop244-workshop-7-derived-classes-solved/)


---

**For Custom/Order Solutions:** **Email:** mantutorcodes@gmail.com  

*We deliver quick, professional, and affordable assignment help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;59051&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;OOP244-Workshop 7 Derived Classes Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
In this workshop, you code a simple hierarchy and define helper functions to support your base and derived classes.

<h1>LEARNING OUTCOMES</h1>
Upon successful completion of this workshop, you will have demonstrated the abilities to:

<ul>
<li>inherit a derived class from a base class</li>
<li>shadow a base class member function with a derived class member function</li>
<li>access a shadowed member function that is defined in a base class</li>
<li>define a non-friend helper function that supports a class</li>
<li>implement friendship between a helper function and the class it supports</li>
<li>describe what you have learned in completing this workshop</li>
</ul>
<strong>I</strong><strong>N</strong><strong>-L</strong><strong>AB </strong><strong>&nbsp;</strong>

Design a base class named Hero, in namespace sict.&nbsp; This class holds information about a fictional hero character. Place your class definition in a header file named Hero.h and your function definitions in an implementation file named Hero.cpp. Include in your design all the statements necessary to compile and to run your code successfully using a standard C++ compiler.

The model for any battle between two Heroes is simple. Each Hero has a non-negative integer health number. A Hero is alive as long as their health is greater than 0. During a battle two Heroes attack one another. Each Hero has their own attack strength. Each attack inflicts damage on the attacked Hero. The inflicted damage reduces the attacked Hero’s health. The winner of the battle is the Hero who remains alive once the other Hero dies. A battle ends in a draw after MAX_ROUNDS rounds.

Initialize MAX_ROUNDS to 100.

A Hero object contains the following data:

<ul>
<li>The name of the Hero – up to 40 characters (excluding the null byte)</li>
<li>The health of the Hero – a positive-valued integer</li>
<li>The attack strength of the Hero – a positive-valued integer</li>
</ul>
Upon instantiation, a Hero object receives no information or information on all three values. If all the information received is valid, the object accepts the values. Otherwise, the object assumes a safe empty state.

Your design includes the following member functions:

void operator-=(int attack): an overloaded operator that receives an attack strength. If that strength is positive-valued, your operator deducts that strength from the current object’s health. If the attack strength received is not positive-valued, your operator does nothing. If the deduction drops the current object’s health below 0, your operator resets the current object’s health to 0. bool isAlive() const: a query that returns true if the current object is healthy and false otherwise.

int attackStrength() const: a query that returns the attack strength of the current object. If the object is in a safe empty state, this function returns 0.

Two helper operators support your class:

ostream&amp; operator&lt;&lt;(ostream&amp; os, const Hero&amp; hero): a friend that inserts the name of hero into output stream os and returns a reference to that stream. If hero is empty, this function inserts the message:

No hero

const Hero&amp; operator*(const Hero&amp; first, const Hero&amp; second): a nonfriend that returns an unmodifiable reference to the winner of the battle between the Heroes after MAX_ROUNDS rounds. Your operator displays the names of the battle participants as shown in the sample output below, makes local copies of the participants, determines the damage that each inflicts on the other in a single attack and battles until either one of the participants dies or the maximum number of rounds is reached. In each round, your operator deducts the damage inflicted on one Hero by the other Hero. Finally, your operator displays the name of the winner. In the case of a draw, your operator assumes arbitrarily that the left operand (first) has won. Your operator returns a reference to the winner object.

Using the sample implementation of the w7_in_lab.cpp main module listed below, test your code and make sure that it works.&nbsp; The expected output from your program is listed below this source code. The output of your program should match <strong>exactly</strong> the expected one.

<h2>IN-LAB MAIN MODULE</h2>
#include &lt;iostream&gt;

#include “Hero.h”

using namespace std; using namespace sict;

<table width="628">
<tbody>
<tr>
<td width="628">&nbsp;

int main()

{

cout &lt;&lt; “Greek Heroes”;

Hero hercules&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Hercules”,&nbsp; 32, 4);

Hero theseus&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Theseus”,&nbsp;&nbsp; 14, 5);

Hero oddyseus&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Odysseus”,&nbsp; 15, 3);

Hero ajax&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Ajax”,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 17, 5);

Hero achilles&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Achilles”,&nbsp; 20, 6);

Hero hector&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Hector”,&nbsp;&nbsp;&nbsp; 30, 5);

Hero atalanta&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Atalanta”,&nbsp; 10, 3);

Hero hippolyta&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Hippolyta”, 10, 2);

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Quarter Finals” &lt;&lt; endl;&nbsp;&nbsp; const Hero&amp; greek_winner1 = achilles * hector;&nbsp;&nbsp;&nbsp; const Hero&amp; greek_winner2 = hercules * theseus;&nbsp;&nbsp; const Hero&amp; greek_winner3 = oddyseus * ajax;&nbsp;&nbsp; const Hero&amp; greek_winner4 = atalanta * hippolyta;

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Semi Finals” &lt;&lt; endl;

const Hero&amp; greek_winner_semifinal1 = greek_winner1&nbsp; * greek_winner2; &nbsp;&nbsp;const Hero&amp; greek_winner_semifinal2 = greek_winner3&nbsp; * greek_winner4;

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Finals” &lt;&lt; endl;

greek_winner_semifinal1 * greek_winner_semifinal2;

&nbsp;

return 0;

}
</td>
</tr>
</tbody>
</table>
<h2>IN-LAB EXPECTED OUTPUT</h2>
<table width="628">
<tbody>
<tr>
<td width="628">Greek Heroes

Quarter Finals

Ancient Battle! Achilles vs Hector : Winner is Hector in 4 rounds.

Ancient Battle! Hercules vs Theseus : Winner is Hercules in 4 rounds.

Ancient Battle! Odysseus vs Ajax : Winner is Ajax in 3 rounds.

Ancient Battle! Atalanta vs Hippolyta : Winner is Atalanta in 4 rounds.

Semi Finals

Ancient Battle! Hector vs Hercules : Winner is Hector in 7 rounds. Ancient Battle! Ajax vs Atalanta : Winner is Ajax in 2 rounds.

Finals

Ancient Battle! Hector vs Ajax : Winner is Hector in 4 rounds.
</td>
</tr>
</tbody>
</table>
<strong>A</strong><strong>T</strong><strong>-H</strong><strong>OME </strong><strong>&nbsp;</strong>

Derive a class named SuperHero from the Hero class that you coded for the <em>in-lab</em> section. Include in your design all the statements and keywords necessary to compile and to run your code successfully using a standard C++ compiler.

Super Heroes behave like Heroes, except that Super Heroes have Super Powers! A SuperHero has a normal attack strength and health, but can also use their super power to attack with a bonus, and to defend themselves —but only against another

SuperHero. <strong><em>When a </em></strong>SuperHero<strong><em> fights against a </em></strong>Hero<strong><em>, the </em></strong>SuperHero<strong><em> does not use its super power, but only uses its normal </em></strong>Hero<strong><em> attack strength.</em></strong>

Upon instantiation, a SuperHero object may receive no information or the following <strong>five </strong>values:

<ul>
<li>The address of a C-style string containing the name of the SuperHero,</li>
<li>The <strong>health</strong> of the SuperHero,</li>
<li>The <strong>attack</strong> strength of the SuperHero in attacks on a Hero,  The super power attack <strong>bonus</strong> of the SuperHero,  The <strong>defend</strong> strength of the SuperHero.</li>
</ul>
The model for a SuperHero battle is the same as the model for a Hero battle, but the damage in any single round is calculated differently. When a SuperHero attacks another SuperHero, the attack strength of the attacking SuperHero is its attack strength plus its bonus attack strength. When a SuperHero is attacked by another SuperHero, the damage to the attacked SuperHero is the attack strength of the attacking SuperHero minus the defend strength of the attacked SuperHero.

Damage(A) = ( &nbsp;&nbsp; Attack of B + AttackBonus of B) – DefendStrength of A

Damage(B) = (Attack of A + AttackBonus of A) – DefendStrength of B

Your SuperHero class includes the two constructors described above and the following member functions:

int attackStrength() const: a query that returns the attack strength of the current object including its super power bonus. If the object is in a safe empty state, this function returns 0.

int defend() const: a query that returns the defend strength of the current object. If the object is in a safe empty state, this function returns 0.

Your design includes a helper operator, which supports your class:

const SuperHero&amp; operator*(const SuperHero&amp; first, const SuperHero&amp; second): a non-friend operator overload that returns an unmodifiable reference to the winner of the battle between the SuperHeroes after MAX_ROUNDS rounds. Your operator displays the names of the battle participants as shown in the sample output below, makes local copies of the participants, determines the damage that each inflicts on the other in a single attack and battles until either one of the participants dies or the maximum number of rounds is reached. In each round, your operator deducts the damage inflicted on a SuperHero by the other SuperHero. Finally, your operator displays the name of the winner. In the case of a draw, your operator assumes arbitrarily that the left operand (first) has won. Your operator returns a reference to the winner object.

The following program (w7_at_home.cpp) uses your SuperHero and Hero classes and produces the output listed below.

<h2>AT-HOME MAIN MODULE</h2>
<table width="628">
<tbody>
<tr>
<td width="628">#include &lt;iostream&gt;

#include “Hero.h”

#include “SuperHero.h”

using namespace std; using namespace sict;

&nbsp;

void line(int width) {&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; cout.width(width – 1);&nbsp; &nbsp; cout.fill(‘-‘);&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; cout &lt;&lt; ‘-‘;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; cout.fill(‘ ‘);

}

int main() {&nbsp;&nbsp; line(60);

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Greek Heroes”;

Hero hercules&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Hercules”,&nbsp; 32, 4);

Hero theseus&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Theseus”,&nbsp;&nbsp; 14, 5);

Hero oddyseus&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Odysseus”,&nbsp; 15, 3);

Hero ajax&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Ajax”,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 17, 5);

Hero achilles&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Achilles”,&nbsp; 20, 6);

Hero hector&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Hector”,&nbsp;&nbsp;&nbsp; 30, 5);

Hero atalanta&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Atalanta”,&nbsp; 10, 3);

Hero hippolyta&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Hippolyta”, 10, 2);

cout &lt;&lt; endl &lt;&lt; “Quarter Finals” &lt;&lt; endl;&nbsp;&nbsp; const Hero&amp; greek_winner1 = achilles * hector;&nbsp;&nbsp;&nbsp; const Hero&amp; greek_winner2 = hercules * theseus;&nbsp;&nbsp; const Hero&amp; greek_winner3 = oddyseus * ajax;&nbsp;&nbsp; const Hero&amp; greek_winner4 = atalanta * hippolyta;

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Semi Finals” &lt;&lt; endl;

const Hero&amp; greek_winner_semifinal1 = greek_winner1&nbsp; * greek_winner2;&nbsp;&nbsp; const Hero&amp; greek_winner_semifinal2 = greek_winner3&nbsp; * greek_winner4;

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Finals” &lt;&lt; endl;

const Hero&amp; greek_final = greek_winner_semifinal1 * greek_winner_semifinal2;

&nbsp;

line(60);

cout &lt;&lt; endl &lt;&lt; “Comic book SuperHeros”;

&nbsp;

SuperHero superman&nbsp;&nbsp;&nbsp; (“Superman”,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 50, 9, 1, 9);

SuperHero hulk&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“The_Hulk”,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 70, 6, 14, 3);

SuperHero wonderwoman (“WonderWoman”,&nbsp;&nbsp; 80, 5, 10, 10);

SuperHero raven&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (“Raven”,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 30, 10, 2, 5);

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Semi Finals” &lt;&lt; endl;

const SuperHero&amp; comic_winner1 = superman * hulk;&nbsp;&nbsp; const SuperHero&amp; comic_winner2 = wonderwoman * raven;

&nbsp;

cout &lt;&lt; endl &lt;&lt; “Finals” &lt;&lt; endl;

const SuperHero&amp; comic_final = comic_winner1 * comic_winner2;

&nbsp;

line(60);
</td>
</tr>
</tbody>
</table>
cout &lt;&lt; endl &lt;&lt; “Best Greeks Hero vs Best Comic Book SuperHero” &lt;&lt; endl;&nbsp;&nbsp; greek_final * comic_final; }

<h2>AT-HOME EXPECTED OUTPUT</h2>
<table width="628">
<tbody>
<tr>
<td width="628">———————————————————–

Greek Heroes

Quarter Finals

Ancient Battle! Achilles vs Hector : Winner is Hector in 4 rounds.

Ancient Battle! Hercules vs Theseus : Winner is Hercules in 4 rounds.

Ancient Battle! Odysseus vs Ajax : Winner is Ajax in 3 rounds.

Ancient Battle! Atalanta vs Hippolyta : Winner is Atalanta in 4 rounds.

Semi Finals

Ancient Battle! Hector vs Hercules : Winner is Hector in 7 rounds. Ancient Battle! Ajax vs Atalanta : Winner is Ajax in 2 rounds.

Finals

Ancient Battle! Hector vs Ajax : Winner is Hector in 4 rounds.

———————————————————–

Comic book SuperHeros

Semi Finals

Super Fight! Superman vs The_Hulk : Winner is The_Hulk in 5 rounds.

Super Fight! WonderWoman vs Raven : Winner is WonderWoman in 3 rounds.

Finals

Super Fight! The_Hulk vs WonderWoman : Winner is WonderWoman in 6 rounds.

———————————————————–

Best Greeks Hero vs Best Comic Book SuperHero

Ancient Battle! Hector vs WonderWoman : Winner is WonderWoman in 6 rounds.
</td>
</tr>
</tbody>
</table>
<h2>REFLECTION</h2>
Study your final solution, reread the related parts of the course notes, and make sure that you have understood the concepts covered by this workshop

Create a file named reflect.txt that contains your <strong>detailed description of the topics that you have learned </strong>in completing this workshop and mention any issues that caused you difficulty. Include in your explanation—<strong>but do not limit it to</strong>—the following points:

<ol>
<li>Does the Hero class need to know about the existence of the SuperHero class? (Hint: search for “SuperHero” in Hero.cpp)</li>
<li>Does the SuperHero class need to know about the existence of the Hero class? (Hint: search for “Hero” in SuperHero.cpp)</li>
<li>The program prints out “Ancient Battle!” when two Heroes It prints out “Super Fight!” when two SuperHeroes fight. When you made a Hero fight a SuperHero, what did it print out?</li>
<li>True or False: is the following definition for main valid? Explain. int main() {</li>
</ol>
Hero(“Achilles”, 20, 6) * Hero(“Hector”, 30, 5);

}

<ol start="5">
<li>True or False: is the following definition for main valid? Explain. int main() {</li>
</ol>
(Hero(“Achilles”, 20, 6) * Hero(“Hector”, 30, 5))

*

(Hero(“Atalanta”, 10, 3) * Hero(“Hippolyta”, 10, 2));

}
