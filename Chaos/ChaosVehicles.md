# ChaosVehicles

## Modules

ChaosVehicles (Plugins/Experimental/ChaosVehiclesPlugin)
ChaosVehiclesEditor (Plugins/Experimental/ChaosVehiclesPlugin)
ChaosVehiclesCore (Source/Runtime/Experimental)
ChaosVehiclesEngine (Source/Runtime/Experimental)
Chaos (Source/Experimental/Chaos)

## Macros

VEHICLE_DEBUGGING_ENABLED

## Classes

* APawn
	* AWheeledVehiclePawn

* FAnimInstanceProxy
	* FVehicleAnimationInstanceProxy
* FBaseSnapshotData
	* FWheelSnapshotData
* FChaosWheelSetup
* FDeferredForces
* FNetworkPhysicsDatas
	* FNetworkVehicleInputs
	* FNetworkVehicleStates
* FPhysicsVehicleOutput
* FVehicleAerofoilConfig
* FVehicleDifferentialConfig
* FVehicleEngineConfig
* FVehicleInputRateConfig
* FVehicleInputs
	* FControlInputs
	* FVehicleReplicatedState
* FVehicleStabilizeControlConfig
* FVehicleState
* FVehicleSteeringConfig
* FVehicleTargetRotationControlConfig
* FVehicleThrustConfig
* FVehicleTorqueControlConfig
* FVehicleTransmissionConfig
* FWheeledVehicleDebugParams
* FWheelSnapshot
* FWheelState
* FWheelStatus
* FWheelTraceParams
* FWheelsOutput

* UObject
	* UAnimInstance
		* UVehicleAnimationInstance
	* UActorComponent
		* UMovementComponent
			* UNavMovementComponent
				* UPawnMovementComponent
					* UChaosVehicleMovementComponent
						* UChaosWheeledVehicleMovementComponent
	* UChaosVehicleWheel
* UChaosVehicleSimulation
	* UChaosWheeledVehicleSimulation