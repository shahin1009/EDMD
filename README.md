# EDMD vs DMD
DMD stands for Dynamic Mode Decomposition and is basically a technique that helps in approximating the spectral properties of the Koopman operator. Now, the Koopman operator is something that tells us how the observables of a nonlinear dynamical system change over time. With DMD, we can extract the most important modes and frequencies of the system from time-series data and use them to create a linear combination that can help us understand the system better.

However, DMD has a few limitations. For instance, it fails to capture the nonlinear dynamics of the system. One more drawback is that it is sensitive to noise and also requires a large number of 'snapshots' (a.k.a data points in time) for high-dimensional systems to work.

This is where eDMD comes into play. It is a generalized version of DMD that lets us choose the observables more flexibly. This makes the method more accurate and also expands its applicability in a broader range of areas.

For eDMD, we use a dictionary of observables(The first three functions in the notebook) that describe the finite-dimensional subspace over which the Koopman operator can be approximated. Hence, we can reconstruct the solution with better accuracy by using a finite number of terms.

The challenge with eDMD is to choose the right dictionary that can capture the nonlinear dynamics of the system. In case of high-dimensional and highly nonlinear systems, we may use machine learning techniques like artificial neural networks or dictionary learning algorithms to select a suitable dictionary.

In a nutshell, eDMD is quite similar to DMD, but employs a dictionary of observables instead of the original state variables, which makes it more flexible and accurate. It is still an approximation method for the Koopman operator that can help us understand both the linear and nonlinear dynamics of the system.
