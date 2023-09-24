# Miscellaneous

cashier can just ignore the customers while on their phone, but usually
customers will interrupt the cashier when this happens after a while,
but you'll just be on your phone indefinitely because you don't want to
interact with them

first play through as you, with very limited options (un-pickable options
visible). Then have the option of playing as any one of the other customers or
employees
But the goal shouldn't be for you to learn other people's behavious. They should
adapt to you, not the other way around.
So when playing as the other characters, maybe a goal could be to make
them leave you alone.
But the game should still allow for interactivities that don't aim
for this.


if you try to take an item while already taking some item, you will
forget the first one and won't be able to retake it. Maybe you can get
distracted by music or other sounds



People can get angry if there are not enough groceries stocked. Usually
groceries will be restocked by the store personnel, but not if they give
up working at the store due to a bad working environment. If you can aid
in causing a bad working environment without being thrown out, you can
thereby indirectly cause the shoppers to get angry. Maybe you can blame
other shoppers for your chaos.


# Flavour text

This can top off the simulation the first time something is encountered.
There are no rules in flavour text, and as such there's also a risk that
it will be wrong and become out of date wrt. the underlying simulation.
But if constrained enough, maybe it's a good enough compromise.


# Testing

A test of the system could be to write down a series of actions that you
expect the system to accept, and then also provide a world state
inspection function that can verify that at least a subset of the world
state is as expected.


# Ideas for interaction chains

Each of these should preferably be without dialogue and instead focus on
actions that can be encoded in a rule-based system in some kind of
meaningful way.

---

They had really been increasing the crampiness factor of these small
supermarkets over the recent years.  You're standing at the end of an
aisle, looking for the ketchup.  It's not here.  You make a very
decisive movement to enter the aisle, only for it to get broken off by an
opposing person moving in your direction.  This aisle only has room for
one person at a time.

You finally manage to walk along the narrow aisle corridor, and notice a
series of red colors to your left.

However, a person behind you coughs impatiently.  Is it the same person
as before?  If so, it seems like an unstructured way of exploring a
supermarket.  In any case, the purposeful coughing only grows the more
you stand still.

> keep investigating => other person will become angry with you
> does not want confrontation => move forward and loop around => no reaction from other person

Related: person.can-remember-faces, interaction.confrontation-averse, items blocking

---

cannot leave unwanted conversation because of 'opinon.polite you'

---

cannot remember where things are if get stressed

---

cannot remember what to buy if get distracted


# Relations

Items can have relations to each other.

`lt taste johnson-mayonaisse supreme-mayo`

This fact will then be presented both when examing Johnson's Mayonaisse
and when examing Supreme Mayo.


# Inventing past interaction chains to ensure a current action

Everything must be grounded in a simulation.  If, for narrative reasons,
we want something to happen to the player at a given time or after a
given set of conditions have been fulfilled, we need the system to be
able to retroactively search and invent a series of past actions that
cause NPC's to perform actions that change the world state in a way that
allows for the narrative event to happen.

For example, it may be that we want the player to get stuck behind
another shopper who refuses to budge.  In that case we need to let the
system decide what actions the NPC could have done beforehand in order
to end up here.  A complete history from the point of entering the
store.  The past actions leading to this point should not involve the
player character, since the player has not seen this NPC before (since
it didn't exist until this point).  This can always be trivially solved
by just letting the NPC enter the store before the character enters it,
but maybe it can also be solved in a less conservative way.

It may be that the NPC's personality traits will then also have to be
generated on-the-fly in order to force a certain walk through the
supermarket.  For example, it might be necessary to have the NPC
*really* like cakes to ensure that they will be standing still at the
cake section of the supermarket.


# Time relations

The initial configuration of the store is manually crafted.
In addition to the store, the world state can also contain a
series of manually crafted temporal action relations that state who
moved what where and when, and who knows that.

These don't need to be in a complete ordering.  Characters might only
know that the Emmentaler cheese was moved somewhere in August and that
the tacos were moved somewhere at the end of August, but not know in
which internal order that the Emmentaler and the tacos were moved in.

Such memories have the same status as personality details in that they
*define* the character.  Alternatively, it might be that it's better to
let the memories organically through a pre-play simulation over the
initial configuration.  But this will then have to generate something
that corresponds to a condition that we're aiming for, which might be
harder.  We can also do both.
