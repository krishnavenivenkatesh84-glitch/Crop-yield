# Crop-yield
Agricultural crop yield estimation
```matlab
function y = fcn(u)
% Agricultural Crop Yield Estimation

rainfall = u(1);
temperature = u(2);
soilPH = u(3);
nitrogen = u(4);
irrigation = u(5);
previousYield = u(6);

y = 1 + 0.002*rainfall ...
      - 0.05*abs(temperature - 27) ...
      + 0.01*irrigation ...
      + 0.003*nitrogen ...
      + 0.4*previousYield;
end
```
