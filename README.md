# Yinan-Repository
Some fundamental concepts of modeling and simulation in the field of biology involve an understanding of the circulation model.
In my case, I will take the non-linear Navier-Stokes equation for conservation of mass and linearize them. I will implement a two step Lax-Wendroff method. My results will tell us how pressure affects area and flow of a blood vessel.

reference: Pan, M. (n.d.). Linearized model of blood flow in vessels project 2 for modeling and simulation in science, engineering and economics. Github.Io. Retrieved 28 April 2022, from https://modelingsimulation.github.io/undergraduateClass/murphy_project.pdf
<img width="415" alt="image" src="https://user-images.githubusercontent.com/101072075/165861513-a306024d-61b0-4529-b7be-166c6961f87e.png">
<img width="416" alt="image" src="https://user-images.githubusercontent.com/101072075/165861565-c21b9ef5-18ef-47f2-b201-beae3a723f92.png">

My work: 
Use code example to find the values contained in these formulas, redefine or assign values to suit our project. Use Matlab to run the most basic formulas from the found code, such as blood vessel volume, flow rate and compliance, and then slowly change some data based on those. Divide it into two analysis of rigid wall and deformable wall, and finally compare their wall stress difference → the error

1.Error of rigid vs. deformable walls simulations.
For Rigid wall
-the interaction between the arterial wall and the blood domain is not taken into account.
-only the arterial lumen needs to be reconstructed and discretized.
-assume that the flow is laminar and incompressible and the blood is modelled as a Newtonian fluid
-Fluid Structure Interaction (FSI) models 
-combining the arterial wall domain with the blood domain, taking into account the interaction between the blood and the arterial wall.

2.The term capacity (C)  C = V / P →rigid wall
-static values of blood volume: V
-Transmural pressure   P = Pi–Po
-the pressure at one section inside the vessel (Pi)
-the pressure outside (Po) the vessel

3.Compliance of blood vessel: capacitance, or compliance (Cd)  Cd = ΔV / ΔP →deformable wall
-the variation in volume 
-per unit change in transmural pressure.

4.Wall shear stress
-circumferential wall stress
(τ, in dynes/cm2)   τ=P/w (1/r1 + 1/r2) 	τ = Pr / w
-transmural pressure (P, in dynes/cm2) 
-w is the wall thickness (assumed to be uniform)
-r1 and r2 are the major and minor radii of curvature of the chamber. 
-For cylindrical vessels, its cross sectional radius r is one of the radii of curvature and the other is infinity
-Specially, τ=T/w, the wall tension (T, which is the force per unit vessel length, in dynes/cm)
