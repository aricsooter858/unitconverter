# Unit Converter

This program converts metric units to imperial units for weight, length, and volume.


### Controller Code
```
myModule.controller('UnitConverter', 
            function ($scope) {
                var uc = this;
                
                uc.weight = 0;
                uc.convertedweight = 0;
                uc.long = 0;
                uc.convertedlength = 0;
                uc.volume = 0;
                uc.convertedvolume = 0;
                
                uc.convertweight = function convertweight(){
                    if (uc.metric_weight.name == "Grams" && uc.imperial_weight.name =="Ounces"){
                        uc.convertedweight = uc.weight * 0.03527396195;
                    return uc.convertedweight;
                    }
                    else if(uc.metric_weight.name == "Grams" && uc.imperial_weight.name =="Pounds"){
                        uc.convertedweight = uc.weight *  0.00220462262185;
                    return uc.convertedweight;
                    }
                    else if(uc.metric_weight.name == "Kilograms" && uc.imperial_weight.name =="Ounces"){
                        uc.convertedweight = uc.weight *  35.274;
                    return uc.convertedweight;
                    }
                    else{
                        uc.convertedweight = uc.weight * 2.20462
                    return uc.convertedweight;
                    }
                }
                
                uc.convertlength = function convertlength(){
                    if (uc.metric_length.name == "Millimeters" && uc.imperial_length.name == "Inches"){
                        uc.convertedlength = uc.long * 0.0393701;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Millimeters" && uc.imperial_length.name == "Feet"){
                        uc.convertedlength = uc.long * 0.00328084;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Millimeters" && uc.imperial_length.name == "Yards"){
                        uc.convertedlength = uc.long * 0.00109361;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Millimeters" && uc.imperial_length.name == "Miles"){
                        uc.convertedlength = uc.long * 0.00000062;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Centimeters" && uc.imperial_length.name == "Inches"){
                        uc.convertedlength = uc.long * 0.393701;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Centimeters" && uc.imperial_length.name == "Feet"){
                        uc.convertedlength = uc.long * 0.0328084;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Centimeters" && uc.imperial_length.name == "Yards"){
                        uc.convertedlength = uc.long * 0.0109361;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Centimeters" && uc.imperial_length.name == "Miles"){
                        uc.convertedlength = uc.long * 0.0000062;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Meters" && uc.imperial_length.name == "Inches"){
                        uc.convertedlength = uc.long * 39.3701;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Meters" && uc.imperial_length.name == "Feet"){
                        uc.convertedlength = uc.long * 3.28084;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Meters" && uc.imperial_length.name == "Yards"){
                        uc.convertedlength = uc.long * 1.09361;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Meters" && uc.imperial_length.name == "Miles"){
                        uc.convertedlength = uc.long * 0.000621371;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Kilometers" && uc.imperial_length.name == "Inches"){
                        uc.convertedlength = uc.long * 39370.1;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Kilometers" && uc.imperial_length.name == "Feet"){
                        uc.convertedlength = uc.long * 3280.84;
                        return uc.convertedlength;
                    }
                    else if(uc.metric_length.name == "Kilometers" && uc.imperial_length.name == "Yards"){
                        uc.convertedlength = uc.long * 1093.61;
                        return uc.convertedlength;
                    }
                    else{
                        uc.convertedlength = uc.long * 0.621371;
                        return uc.convertedlength;
                    }
                    
                }
                
                 uc.convertvolume = function convertvolume(){
                    if(uc.metric_volume.name == "Cubic Centimeters" && uc.imperial_volume.name == "Fluid Ounces"){
                        uc.convertedvolume = uc.volume * 0.033814;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Cubic Centimeters" && uc.imperial_volume.name == "Pints"){
                        uc.convertedvolume = uc.volume * 0.00211338;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Cubic Centimeters" && uc.imperial_volume.name == "Gallons"){
                        uc.convertedvolume = uc.volume * 0.000264172;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Cubic Meters" && uc.imperial_volume.name == "Fluid Ounces"){
                        uc.convertedvolume = uc.volume * 33814;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Cubic Meters" && uc.imperial_volume.name == "Pints"){
                        uc.convertedvolume = uc.volume * 2113.38;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Cubic Meters" && uc.imperial_volume.name == "Gallons"){
                        uc.convertedvolume = uc.volume * 264.172;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Cubic Meters" && uc.imperial_volume.name == "Gallons"){
                        uc.convertedvolume = uc.volume * 264.172;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Liters" && uc.imperial_volume.name == "Fluid Ounces"){
                        uc.convertedvolume = uc.volume * 33.814;
                        return uc.convertedvolume;
                    }
                    else if(uc.metric_volume.name == "Liters" && uc.imperial_volume.name == "Pints"){
                        uc.convertedvolume = uc.volume * 2.11338;
                        return uc.convertedvolume;
                    }
                    else{
                        uc.convertedvolume = uc.volume * 0.264172;
                        return uc.convertedvolume;
                    }
                }
                
                
                uc.metric_weight_options = [
                        {name:"Grams"},
                        {name:"Kilograms"}
                    ];
                uc.metric_weight = uc.metric_weight_options[0];    
                
                    
                uc.imperial_weight_options = [
                    {name:"Ounces"},
                    {name:"Pounds"}
                ];
                
                uc.imperial_weight = uc.metric_weight_options[0];
                
                uc.metric_length_options = [
                  {name:"Millimeters"},
                  {name:"Centimeters"},
                  {name:"Meters"},
                  {name:"Kilometers"}
                ];
                
                uc.metric_length = uc.metric_length_options[0];
                
                uc.imperial_length_options = [
                    {name:"Inches"},
                    {name:"Feet"},
                    {name:"Yards"},
                    {name:"Miles"}
                ];
                
                uc.imperial_length = uc.imperial_length_options[0];
                
                uc.metric_volume_options = [
                    {name:"Cubic Centimeters"},
                    {name:"Cubic Meters"},
                    {name:"Liters"}
                ];
                
                uc.metric_volume = uc.metric_volume_options[0];
                
                uc.imperial_volume_options = [
                    {name:"Fluid Ounces"},
                    {name:"Pints"},
                    {name:"Gallons"}
                ];
                
                uc.imperial_volume = uc.imperial_volume_options[0];
                
            }
            
        );

```


### HTML Code
```
<div ng-controller="UnitConverter as uc">
            <p>
                <h1>Weight Converter</h1>
                <input type="text" ng-model="uc.weight" placeholder="0" />
                <span><select ng-model="uc.metric_weight" ng-options="s.name for s in uc.metric_weight_options" ng-change="uc.convertweight()"></select></span>
                To <span><select ng-model ="uc.imperial_weight" ng-options="s.name for s in uc.imperial_weight_options" ng-change="uc.convertweight()"></select>
                <button ng-click="uc.convertweight()">Convert</button></span><br/>
                The selected unit is <span ng-bind="uc.metric_weight.name"></span>
            </p>
            <p>
             <span ng-bind="uc.weight"></span> <span ng-bind="uc.metric_weight.name"></span> equals {{uc.convertedweight}} <span ng-bind="uc.imperial_weight.name"></span>
            </p>
            <p>
                <h1>Length Converter</h1>
                <input type="text" ng-model="uc.long" placeholder="0" />
                <span><select ng-model="uc.metric_length" ng-options="s.name for s in uc.metric_length_options" ng-change="uc.convertlength()"></select></span>
                To <span><select ng-model ="uc.imperial_length" ng-options="s.name for s in uc.imperial_length_options" ng-change="uc.convertlength()"></select>
                <button ng-click="uc.convertlength()">Convert</button></span><br/>
                The selected unit is <span ng-bind="uc.metric_length.name"></span>
            </p>
            <p>
                <span ng-bind="uc.long"></span> <span ng-bind="uc.metric_length.name"></span> equals {{uc.convertedlength}} <span ng-bind="uc.imperial_length.name"></span>
            </p>
            <p>
                <h1>Volume Converter</h1>
                <input type="text" ng-model="uc.volume" placeholder="0" />
                <span><select ng-model="uc.metric_volume" ng-options="s.name for s in uc.metric_volume_options" ng-change="uc.convertvolume()"></select></span>
                To <span><select ng-model ="uc.imperial_volume" ng-options="s.name for s in uc.imperial_volume_options" ng-change="uc.convertvolume()"></select>
                <button ng-click="uc.convertvolume()">Convert</button></span><br/>
                The selected unit is <span ng-bind="uc.metric_volume.name"></span>
            </p>
            <p>
                <span ng-bind="uc.volume"></span> <span ng-bind="uc.metric_volume.name"></span> equals {{uc.convertedvolume}} <span ng-bind="uc.imperial_volume.name"></span>
            </p>
        </div>

```