% Day 03 worksheet solution
% EOSC 340
% Sept. 18, 2019


# Worksheet - EOSC 340 - Day 3

## Prove: Good absorbers are good emitters

The two walls shown below are initially at the same temperature, though they have different emissivities as shown. Assume the transmissivity is 0 for both walls. The space between the walls is a vacuum. Recall that $\sigma$=5.67x10<sup>-8</sup> W/m<sup>2</sup>/K<sup>4</sup>. Note that the right all absorbs everything that hits it (it’s a blackbody), while the left wall partially absorbs some radiation and reflects the rest.

![Two walls with the same temperature but different emissivities](media/two_walls.png){ width=60% }

## These four questions assume $abs=\epsilon$:

**Q1: ** On average, is there a net heat transfer between the two walls? If so, which way does it go? Provide reasoning, but **do not** do any math at this point.

**The 2<sup>nd</sup> law of thermodynamics says that the temperature can’t change without some process doing work, so the net transfer has to be zero at both walls.**

**Q2:** Do either or both of the walls change their temperature with time? If so, which becomes warmer with time, and which cools down with time?  Again, don’t do any math at this point.

**No temperature change for either wall.**

**Q3:** What is the radiative flux (in W/m<sup>2</sup>) emitted by the:

a) the right wall, and  
b) the left wall?

**Right wall: $I_{right} = \sigma T^4 =348.5 W/m^2$**

**Left wall: $I_{left}= \epsilon \sigma T^4$ = 0.6x348.5=209
$W/m^2$**

**Q4:** How much flux is absorbed at the left wall, assuming Kirchoff’s law is
true?

**If abs=$\epsilon$ then $abs \times I_{right}$ = $\epsilon \times I_{right} = 209\ W/m^2$**

## The proof

**Q5:** **Kirchhoff’s Law** states that *abs* = $\epsilon$. Show algebraically that this must be true at the left wall. Do not use numeric values\! Assume that the left wall can’t change temperature, so that all the arrows at the wall have to cancel out. Remember that the wall is absorbing and reflecting, but not transmitting.

**Since the 2nd law says temperature can’t change, that means the fluxes in and out have to balance. If we use a minus sign for outbound fluxes and plus sign for inbound fluxes, then the balance at the left wall is:**

\begin{align}
I_{emit-R} - I_{emit-L} - I_{\alpha-L} = 0
\end{align}
where $\alpha$ = reflectivity (albedo) as in the Day 3 reading.

**Also, we can use conservation of energy to write the reflectivity in terms of the absorptivity,
since from the day 3 reading we know that the reflectivity $\alpha$, absorptivity abs and transimissivity are related by:**

\begin{align}
\alpha + abs + tr = 1 \\
\alpha = 1 - abs
\end{align}
since the wall can't transmit radiation so tr=0.

**using this, we have:**

\begin{align}
I_{\alpha-L}= (1 - abs)I_{emit-R}
\end{align}

**So put all this together**:


\begin{align*}
I_{emit-R} - I_{emit-L} - I_{\alpha-L}=0 \\
\sigma T^4 - \epsilon \sigma T^4 - (1-abs) \sigma T^4=0 \\
\text{now divide out the $\sigma T^4$} \\
1 - \epsilon - (1-abs) = 0 \\
\epsilon = abs \\
QED
\end{align*}





```python

```
