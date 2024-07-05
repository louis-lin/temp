Rocket Trajectory Calculation
-----------------------------

Here's a simple MATLAB function to calculate the maximum height of a rocket:

.. code-block:: matlab

   function max_height = rocket_height(initial_velocity, acceleration)
       % Calculate time to reach max height
       time_to_max = initial_velocity / acceleration;
       
       % Calculate max height
       max_height = initial_velocity * time_to_max - 0.5 * acceleration * time_to_max^2;
   end

   % Example usage
   v0 = 1000; % Initial velocity in m/s
   a = 9.8;   % Acceleration due to gravity in m/s^2
   h_max = rocket_height(v0, a);
   fprintf('Maximum height: %.2f meters\n', h_max)