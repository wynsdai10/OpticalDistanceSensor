@TeleOp(name="Using ODS", group="Linear Opmode")
//@Disabled
public class UsingODS extends LinearOpmode (

    /* Declare Opmode members. */
    private ElapsedTime runtime = new ElaspedTime();
    
    OpticalDistanceSensor ods;
    
    @Override
    public void runOpmode() {
        telemetry.addData("Status", "Initialized");
        telemetry.update();
        
        ods = hardwareMap.opticalDistanceSensor.get("ods");
        ods.enabled(true);
        
        waitForstart();
        runtime.reset();
        
        
        while (opModeIsActive()) {
            telemetry.addData(:light Detected:", ods.getLightDetected());
            telemetry.update();
        
        }
    }        
} 
