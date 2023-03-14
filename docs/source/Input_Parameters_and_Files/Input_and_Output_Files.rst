Model Inputs
-----

	S
	  :description:		the main structure that includes the default settings of the ShorelineS model
	  :units:		-
	  :default:		-
	  :min:			-
	  :max:			-
Simulation wave input files:
^^^^^^^^^

	S.WVCfile
	    :description:		(Spatially Varying) wave time-series file path.
	    :units:		        [m], [Hr], [degrees], [-]
        :default:           '' (empty)
	    :required:	        No; leave empty to use wave parameters ('S.Hso', 'S.phiw0' and 'S.spread').
	    :format:		    .wvt (Obligatory extension)
	S.Waveclimfile
		:description:	    Wave climate file that contains fou columns: Hs, Tp, Direction, and Probability.
		:units:		        [m]
		:default:		    1
		:required:		    No; leave empty to use wave parameters ('S.Hso', 'S.phiw0' and 'S.spread').
		:format:			-