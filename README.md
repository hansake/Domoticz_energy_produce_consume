# Domoticz_energy_produce_consume
Calculate and show difference between produced and consumed energy today

* The produced energy is measured by the SolarEdge solar cell inverter
*   the counter "counterToday" is read (device is called "SolarEdge kWh" here)
* The consumed energy is measured by the electrical meter for total consumption
*   the counter "counterToday" is read (device is called "Elmätare total" here)
*
* Create two virtual sensors in Domoticz:
*    name: "Till elnätet" (To grid)
*        Sensor Type: Counter
*        when created, edited to be of Type: Energy Generated (shows as kWh)
*    name: "Från elnätet" (From grid)
*        Sensor Type: Counter
*        when created, edited to be of Type: Energy (shows as kWh)
*
* For each virtual sensor a summation counter is created that is updated
*   when the daily counter shows a lower value than the last reading.
