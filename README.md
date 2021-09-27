Put this in your mechanicjob/client.lua

![](images/you-picture.png)

```RegisterNetEvent('upgradecar')
AddEventHandler('upgradecar', function()
    local vehicle = QBCore.Functions.GetClosestVehicle()
    local plate = GetVehicleNumberPlateText(vehicle)


    veh = QBCore.Functions.GetClosestVehicle()
    turbo = IsToggleModOn(veh, 18)
    if turbo == 0 then
        turbo = "Standard"
    elseif
        turbo == 1 then
        turbo = "You have a Turbo"
    end

    veh = QBCore.Functions.GetClosestVehicle()
    engine = GetVehicleMod(veh, 11)
    if engine == -1 then
        engine = "Standard"
    elseif
        engine == 0 then
        engine = "Engine Lvl 1"
    elseif
        engine == 1 then
        engine = "Engine Lvl 2"
    elseif
        engine == 2 then
        engine = "Engine Lvl 3"
    elseif
        engine == 3 then
        engine = "Engine Lvl 4"
    elseif
    engine == 4 then
    engine = "Engine Lvl 5"
    end

    veh = QBCore.Functions.GetClosestVehicle()
    transmission = GetVehicleMod(veh, 13)
    if transmission == -1 then
        transmission = "Standard"
    elseif
    transmission == 0 then
        transmission = "Transmission Lvl 1"
    elseif
    transmission == 1 then
        transmission = "Transmission Lvl 2"
    elseif
    transmission == 2 then
        transmission = "Transmission Lvl 3"
    elseif
    transmission == 3 then
        transmission = "Transmission Lvl 4"
    end

    veh = QBCore.Functions.GetClosestVehicle()
    suspension = GetVehicleMod(veh, 15)
    if suspension == -1 then
        suspension = "Standard"
    elseif
    suspension == 0 then
        suspension = "Suspension Lvl 1"
    elseif
    suspension == 1 then
        suspension = "Suspension Lvl 2"
    elseif
    suspension == 2 then
        suspension = "Suspension Lvl 3"
    elseif
    suspension == 3 then
        suspension = "Suspension Lvl 4"
    elseif
    suspension == 4 then
        suspension = "Suspension Lvl 5"
    end

    veh = QBCore.Functions.GetClosestVehicle()
    brakes  = GetVehicleMod(veh, 12)
    if brakes == -1 then
        brakes  = "Standard"
    elseif
    brakes  == 0 then
        brakes = "Brakes Lvl 1"
    elseif
    brakes  == 1 then
        brakes  = "Brakes Lvl 2"
    elseif
    brakes  == 2 then
        brakes  = "Brakes Lvl 3"
    elseif
    brakes  == 3 then
        brakes  = "Brakes Lvl 4"
    end
    
    TriggerEvent('nh-context:sendMenu', {
        {
            id = 1,
            header = "Vehicle Menu",
            txt = "Menu ...",
        },
        {
            id = 1,
            header = "- Engine Level",
            txt = engine,
        },
        {
            id = 2,
            header = "- Transmission Level",
            txt = transmission,
        },
        {
            id = 4,
            header = "- Suspension Level",
            txt = suspension,
        },
        {
            id = 5,
            header = "- Brakes Level",
            txt = brakes,
        },
        {
            id = 6,
            header = "- Turbo",
            txt = turbo,
        },
        {
            id = 7,
            header = "< Go back  ",
            txt = "Go back to the main menu",
            params = {
                event = "client:car"
            }
        },        
    })
end) 
