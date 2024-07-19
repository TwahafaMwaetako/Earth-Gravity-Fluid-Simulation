# Earth Gravity Fluid Simulation

This project is a web-based simulation that demonstrates fluid particle behavior under Earth's gravity. It uses HTML5 Canvas and JavaScript to create an interactive environment where users can observe and manipulate particle dynamics.

## How It Works

The simulation creates a 2D environment where particles move and interact with each other and the canvas boundaries. Here's an overview of the key components and their functionality:

1. **Particle System**: The core of the simulation is a particle system. Each particle is represented as a circular object with properties such as position, velocity, and size.

2. **Physics Engine**: A simple physics engine updates the particles' positions and velocities in each frame. It applies forces like gravity and handles collisions with boundaries.

3. **Rendering**: The Canvas API is used to draw particles on the screen, creating a visual representation of the simulation.

4. **User Interaction**: Users can interact with the simulation by adjusting parameters through on-screen controls and adding new particles by clicking on the canvas.

## Physics Explained

The simulation incorporates several physical principles to create realistic particle behavior:

1. **Gravity**: Earth's gravity is simulated by applying a constant downward acceleration to all particles. The default value is set to 9.8 m/s², which is the approximate acceleration due to gravity on Earth's surface.

2. **Newton's Laws of Motion**: The simulation applies Newton's laws of motion to update particle positions and velocities:
   - First Law: Particles maintain their velocity unless acted upon by a force (like gravity or collisions).
   - Second Law: The acceleration of a particle is directly proportional to the net force acting on it and inversely proportional to its mass (F = ma).

3. **Collisions**: When particles hit the canvas boundaries, they bounce off. This is implemented using a simple reflection model, where the component of velocity perpendicular to the boundary is reversed and scaled by a bounce factor.

4. **Air Resistance**: A simple drag force is applied to simulate air resistance. This is implemented by reducing the particle's velocity slightly each frame, causing particles to eventually come to rest if no other forces are acting on them.

5. **Scaling**: The simulation uses a scale where 100 pixels represent 1 meter in the real world. This scaling allows for more intuitive visualization of the particles' behavior.

6. **Time Step**: The simulation uses a fixed time step (DT) of 1/60 seconds for each update. This ensures consistent behavior regardless of the actual frame rate.

By combining these physical principles, the simulation creates a simplified but engaging representation of fluid-like particle behavior under Earth's gravity. Users can experiment with different parameters to observe how changes in gravity, particle size, and other factors affect the overall behavior of the system.
