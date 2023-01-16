Introduction
============

Sandy beaches are extremely valuable natural resources, providing the
first line of defence against coastal storm impacts, as well as other
ecosystem services (Barbier et al., 2011) such as ecological habitats
and recreation areas. These beaches often are an essential part of a
nation’s heritage. However, many of the world’s coastlines suffer
erosion, due to interruption of sand flows from upstream (Syvitski et
al., 2005) and alongshore, sand mining and sea-level rise effects, which
is especially the case in the vicinity of tidal inlets (Ranasinghe et
al., 2013). Science-based strategies for managing complex sandy coasts
are, therefore, of the utmost importance, requiring stable, robust and
rapid evaluation methods.

Coastline changes along sandy beaches at timescales beyond events and
seasons often are dominated by gradients in wave-driven longshore
transport. The first practical concept for predicting coastline change
due to interruption of this wave-driven longshore transport was
developed by Pelnard-Considère (1956), who derived a diffusion-type
equation based on the assumptions of a small angle of incidence and a
constant cross-shore profile shape. The first very limiting assumption
of a small wave angle was relaxed to some extent by numerical,
one-dimensional (1D) model approaches, such as GENESIS (Hanson, 1989),
LITPACK (Kristensen et al., 2016), and UNIBEST (Tonnon et al., 2018).
These models, which we will refer to as ‘standard 1D models’ also
applied increasingly powerful and more advanced physics-based approaches
using newer transport formulations, (e.g., Bijker, 1967; Kamphuis, 1991;
van Rijn, 2014), to estimate the transport rate as a function of
incident wave conditions, sediment parameters and profile shape.
However, the main characteristic of the transport curve as a function of
the wave angle remained a sine curve, with a maximum at roughly
45\ :sup:`o`. For relative angles beyond this critical angle, longshore
transport decreases for increasing angles and the morphological behavior
of the coastline becomes fundamentally unstable.

While the existing coastline models had no real solution for this
instability, the Coastal Evolution Model (CEM) proposed by Ashton et al.
(2001) addressed this point using a grid-based, upwind approach, which
they showed to be able to explain a variety of coastal forms found in
nature. The high angle wave instability mechanism (HAWI) has been
studied extensively through linear and non-linear stability
analysis,(Falqués & Calvete, 2005; e.g., Ashton & Murray, 2006; van den
Berg et al., 2011; Falqués et al., 2017) the latter included both this
and the low angle instability mechanism (LAWI) proposed by Idier et al.
(2011). These analyses pointed out the importance of the refraction on
the foreshore of shoreline undulations, which generally stabilize the
coastline relative to the original HAWI mechanism proposed by Ashton et
al. (2001). Recently, Robinet et al. (2018, 2020), starting from the
same grid-based one-line approach, extended the concept by coupling it
with a 2D wave refraction model and including cross-shore transport.
Such models are quite powerful in describing complex coastal shapes but
at the cost of requiring complex and relatively time-consuming codes.

The standard 1D models approaches so far address either a single,
possibly curving, coastline or disparate sections of coastline
represented by separate models. However, there are many cases where
islands, shoals and spits shield other parts of the coast from waves. In
other situations, spits weld onto the coast to form lagoons that in turn
may break up into different parts, or islands migrate towards the coast
and weld onto it. Even though some gradual reshaping from a straight
beach to a bay shape was achieved with numerical models (e.g., Hanson,
1989), still the grid definition in existing models only allows for a
small re-curvature of the coast, generally much less than 90\ :sup:`o`.
As a result, research often focuses on a final stage of the
morphological development (e.g., a static bay shape; Hsu et al., 2010).
The flexible generation of the grid at each time step is a requisite to
deal with complex shoreline shapes which may change substantially over
time, such as spits, salients and tombolos.

A vector-based approach to represent the coastline was first used by
Kaergaard and Fredsoe (2013a), as part of a system that coupled a
one-line coastline approach with a two-dimensional description of the
wave and sediment transport, on an unstructured mesh. They applied a
quite complicated approach to ensure the volume balance, using
triangular and trapezoidal elements. The original coastline
representation proposed by Kaergaard and Fredsoe (2013a) was adopted by
Hurst et al. (2015) which followed a similar approach to the one
presented in this manuscript but for a single coastline (i.e. no
splitting or merging was included). Kaergaard & Fredsoe (2013a) and
Hurst et al.(2015) implicitly assumed sediment rich environments. Payo
et al. (2017) extended the use of vector-based coastline models to
sediment-starved environments and applied it to a field study case to
simulate the coastal change after defence removal (Payo et al., 2018).
In all these vector-based models the coastline followed is at the top of
the active profile. This choice implies a strong need to correct the
volume balance for strongly curved coasts. As we will explain in detail,
our approach follows a more representative coastline, situated
approximately at Mean Sea Level (MSL). This recognizes the fact that
typically, over longer periods aimed at by this model, the active
profile extends from a closure depth to the crest of foredunes; these
are at approximately equal vertical distances from the MSL contour. The
approach has two advantages: the contour usually extracted from
satellite imagery is the MSL contour, and as we will show, complex
curvature corrections to the sediment balance are not needed, which
makes our method much simpler.

It is noted that computations can be made with complex two-dimensional
horizontal (2DH) process-based models, as was shown for the recent case
of the ‘Sand Engine’ in Holland (Luijendijk et al., 2017) as well as for
other complex coastal forms. However, this comes at great computational
expense and requires considerable expertise. Even though an effort was
made to increase the robustness and efficiency of the process-based
morphological models (Kaergaard & Fredsoe, 2013a), still these detailed
field models are appropriate for the investigation of specific processes
(i.e. science), but are often less suited to apply in engineering
(design phase) for data poor environments where quick scenario
evaluations are needed. So, engineers are rather stuck with one approach
which does not capture the complexity of coastal evolution and another
which is too expensive.

Consequently, a new approach is needed to robustly follow coastal
features through complete lifecycles at reasonable computational cost.
We demonstrate here the capabilities that arise when a model with a flexible,
coastline-following grid is used: namely, straightforward definition of
a complex planform, freedom to allow coastal evolution in any direction,
and the possibility to merge and split coastline sections where needed.
The characteristic features of the model are presented for a selection
of analytical and principle test cases. In addition, the practical
simulation of coastline evolution is validated for a large-scale,
manmade land reclamation and a case of a groyne field filling in. 
We do not yet consider event-scale and seasonal variations,
which are mostly due to cross-shore transport. Methods for including
this as recently described by e.g. Vitousek (2017), Robinet (2018),
Antolínez (2019), Palalane and Larson (2020), and Tran and Barthélemy
(2020) are currently under consideration.