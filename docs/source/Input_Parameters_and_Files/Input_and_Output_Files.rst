Input and Output Parameters
===========================


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

Simulation coastline definition:
^^^^^^^^^
	S.LDBcoastline=''
		:description:	    LDB with initial coastline shape 
		:units:		        ([Nx2] ASCII FILE WITHOUT HEADER)
		:default:		    ''
		:required:		    No; leave empty to use interactive mode.
		:format:			file path [.ldb]