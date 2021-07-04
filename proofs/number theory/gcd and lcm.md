# GCD and LCM
## GCD
%%> **Therum gcd1**
> 
> **Claim**: If $\g(a, b)=k$, then $\g(ax, bx)=kx$ where $a, b\in\Z$ and $x\in\Z^+.$
> 
> **Proof:**
> $\plet a, b\in \Z$.
> $\plet x\in\Z^+$.
> By [[proofs/number theory/definitions#^65eeb4| definition of the gcd]], $k$ is the greatest element of $Z^+$ such that $k|a$, and $k|b$. By [[proofs/number theory/definitions#^8508b9|definition of divisibility]], there exists an $n\in\Z^+$, and $m\in\Z^+$ such that $kn=a$, and $km=b$. This can be rearranged as follows:
> $$kn=a\implies knx=ax$$
> $$km=b\implies kmx=bx$$
> By [[proofs/number theory/definitions#^8508b9|definition of divisibility]], $$ax|kx\and$$ $$bx|kx$$.
> Also, note that %%
> **Therum gcd1**
> **Claim**: If $\g(ak, bk)=k\implies \g(a, b)=1$.
> 
> **Proof:**
> $\plet ak, bk\in \Z$ where $k\in\Z^+$
> Assume that $\g(a, b)\not=1$. Therefore, there is an $l\in\Z^+$ such that $\gcd(a, b)=l$ and $l\not=1$. By [[proofs/number theory/definitions#^65eeb4|the definition of gcd]], this implies that $l$ is the largest integer such that $l|a$, and $l|b$.  Note that $l|a \implies lk|ak$, and $l|b\implies lk|bk$. Therefore, $\gcd(ak, bk)\not=k$ because $k$ is not the largest integer that divides $ak$, and $bk$. The contrapositive of the claim is true, so is the claim.