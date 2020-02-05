# Fermi-LAT: Convert TS + Degree of Freedom --> sigma      

This short routine is intended as a tool to calculate the  statistical significance (\sigma) of a \gamma-ray signature, detected with the Fermi Large Area Telescope (LAT). The sigma value depends on the number of Degrees of Freedom (dof) involved in a Likelihood Analysis and the resulting Test Statistic (TS) value. 

 
**A standard analysis with Fermi-LAT** involves four degrees of freedom. Two associated to the uncertain position of the source (R.A.,Dec.), and another two associated with the shape of the \gamma-ray spectrum that -in the simplest case- can be assumed to follow a power-law, dN/dE = N_0 (E/E_0)^\Gamma . Here, N_0 is the pre-factor or normalization parameter [photons/cm^2/s/MeV], \Gamma is the photon index, and E_0 is the pivot-energy [MeV] where both N_0 and \Gamma are estimated. Usually, the E_0 value has to be fixed during the analysis, otherwise, the number of degrees of freedom brings far too much uncertainty to the N_0, \Gamma and E_0 values. Still, one should run the analysis testing over a reasoable range of E_0 values (from 500 MeV up to Tens of GeV) to optimize the N_0 and \Gamma estimates. This is the typical approach to Fermi-LAT data, if the analysis is solo based in \gamma-ray information (blind to information collected from other bands).

In this case, a signature with TS = 25, from a likelihood analysis with 4 degrees of freedom, corresponds to a 3.88 \sigma detection. 

**Multifrequency Information:** However, it is possible to take into account multifrequency information, and lower the uncertainty of the analysis, by fixing the position of the \gamma-ray emitter. Please check the [2BIGB gamma-ray catalogue](https://arxiv.org/abs/1911.08912). This is perfectly fine if one considers the position of Blazars -especially out of the galactic plane- because blazars are the dominant extragalactic \gamma-ray sources. 

In this case, if the position of the \gamma-ray candidate is known, there are only two degrees of freedom for the likelihood analysis: the ones associated with the power-law spectral modeling. 

A signature with TS = 19.5, deduced from a likelihood analysis with only 2 degrees of freedom, corresponds to a 3.85 \sigma detection. Therefore, if one searches for gamma-ray signatures associated with blazars (as for the 2BIGB catalogue), a TS=19.5 threshold is equivalent to a TS=25 blind search detection threshold. 

A signature with TS = 10, deduced from a likelihood analysis with only 2 degrees of freedom, corresponds to a 2.47 \sigma detection. 
