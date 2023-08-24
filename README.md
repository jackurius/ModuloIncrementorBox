# ModuloIncrementorBox
A class using Pytket that adds a set increment to any sub-section of computational bases states.

A modulo increment is a permutation that satisfies:  

$C_{k}|j\rangle = |(j + k) \mod 2^{n\_qubits}\rangle$
<br>
<br>
$E.g.:$  <br>
$C_{3}|000\rangle = |011\rangle$  <br>
$C_{3}|101\rangle = |000\rangle$  <br> 
$Etc. for \space all \space states \space in \space the \space bases$

The original idea of applying a modulo increment by using the QFT (Quantum Fourier Transform) was given by Julien Sorci. The QFT approach uses around $2N^2$ two qubit gates, whereas the ToffoliBox uses around $2^N$ two qubit gates for N qubits. Benchmarked against ToffoliBox, we see a very clear increase in efficiency for uniform increments. However this approach only works for modulo increments, and not for any arbitrary permutation (as expected), therefore there are lots of limits to its applications:  
<br>
![image.png](attachment:89c8a4f0-f3d0-4f3d-bd5e-a79a519304be.png)  
<br>
