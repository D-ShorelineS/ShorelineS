Input and Output Parameters
===========================

In this section, the list of model input and output parameters are going to be listed. The user can easily change the value of these parameters in the MATLAB/ Octave code. 
If not changed, the below default values would be used by the ShorelineS model.

Model Inputs
-----

	S
	  :description:		the main structure that includes the default settings of the ShorelineS model
	  :units:		-
	  :default:		-
	  :min:			-
	  :max:			-
Simulation wave parameters:
^^^^^^^^^

	S.Hso
		:description:		wave height
		:units:		[m]
		:default:		1
		:min:			-
		:max:			-	  
	S.phiw0
		:description:		deep water wave angle 
		:units:		degrees
		:default:		330
		:min:			-
		:max:			-
	S.spread
		:description:		wave spreading (wave_dir from range:  S.phiw0 +/- 0.5*S.spread)
		:units:		degrees
		:default:		90
		:min:			-
		:max:			-
	S.WVCfile
		:description:		wave time-series file path <-leave empty to use wave parameters ('S.Hso', 'S.phiw0' and 'S.spread')
		:units:		-
		:default:		''
		:min:			-
		:max:			-
	S.Hso
		:description:		wave height
		:units:		[m]
		:default:		1
		:min:			-
		:max:			-



Advanced Input parameters (only for advanced users)
-----


Model Output Parameters
-----

		  