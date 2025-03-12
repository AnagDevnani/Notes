# K-Map
- Follows gray code in which only one bit change is allowed when going in increasing order.
	- This is done because it (<font color=red>Presumably</font>) simplifies the expressions.

## Sum of Product & Product of Sum
1. SOP $\rightarrow$ minterms $\bigg(\sum m\bigg)$
2. POS $\rightarrow$ maxterms $\bigg(\Pi M\bigg)$

### Steps to solove boolean expressions using k-map
1. Select the k-map according to the number of input variables.
2. Identify minterms or maxterms as given in the problem.
	- For SOP, put 1s in all blocks / cells of k-map respective to the minterms and 0s elsewhere.
	- For POS, put 0s in all blocks / cells of k-map respective to the maxterms and 1s elsewhere.
3. Make rectangular groups containing total terms in powers of 2.
4. From the groups made find the:
	- Product terms and sum them up for SOP form.
	- Addition terms and multiply them up for POS form.

**Note:** The rectangular region is loopable. i.e. the first and last can be grouped (like pacman)

minterms is the combination of input having high (1) value.
maxterms is the combination of input having low (0) value.

Draw k-map of A/BC.
Apply step 2 based on the value of the block is k-map corresponding to min/maxterms.

**Note:** In SOP, $A = 1$, $\overline{A}=0$
**Note:** In POS, $A = 0$, $\overline{A}=1$

## Minimal Sum and Product with <font color=red> </font>
During the process of designing SOP map, each don't care is treated as 1, If it is helpful in map reduction otherwise it is treated as 0.

During the process of designing POS map, each don't care is treated as 0, If it is helpful in map reduction otherwise it is treated as 1.

An SOP expression with don't care can be convertes int oPOS form by keeping the don't cares as they are and writing the missing minterms of the SOP form as the maxterms of POS form.

And vice-versa for POS to SOP form.
