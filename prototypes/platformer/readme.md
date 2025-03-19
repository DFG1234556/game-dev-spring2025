# Platformer Development Reflection
Game Development
2025 Spring


## Prototype 1
![enter image description here](https://dfg1234556.github.io/game-dev-spring2025/pic/1.png)
[Play Prototype 1](https://dfg1234556.github.io/game-dev-spring2025/builds/platformer-1/)

In this prototype, I was exploring how a player could navigate a small 3D space, where all three axes (X, Y, and Z) are crucial but not viewable simultaneously. A camera mode switching system was implemented to allow the player to adjust their view dynamically. Basic character movement and physics were incorporated, alongside scripted platform movements instead of relying on an animator. Additionally, I experimented with a fall damage system that calculated damage based on fall height, speed, and duration, adding an element of risk to movement if player has to jump down a platform. In addition, I also tested cursor-locking toggles to ensure smooth transitions between gameplay and interface interaction to avoid destroying the immersion.

  
Through this prototype, I gained a deeper understanding of camera control in constrained 3D spaces and how perspective influences level navigation with missing information. The camera modes provided valuable insight into how players might need to reorient themselves in a platformer with complex spatial relationships. However, I found that emulating the visual observation system from a first-person perspective may not be the best implemented with the camera placed where the character is. Implementing scripted platform movement allowed for more precise control over timing and interactions compared to animation-driven platforms. The fall damage system led to more design challenges too —setting appropriate thresholds for damage and adjusting platform distances versus instant death was quite difficult.



## Prototype 2
![enter image description here](https://dfg1234556.github.io/game-dev-spring2025/pic/21.png)
![enter image description here](https://dfg1234556.github.io/game-dev-spring2025/pic/22.png)
[Play Prototype 2](https://dfg1234556.github.io/game-dev-spring2025/builds/platformer-2/)


In this prototype, I focused on character state changes based on both player input and environmental interactions. This meant that the player needed to adapt to different hazards by using specific actions to navigate safely. One key experiment was the gale zone system, which includes an actual gale area and an alert area. UI warnings for gale conditions are implemented once the character enters the alert area, and a detection system is there to determine when the player is affected by strong winds. Another major experiment was a rope and pole system, allowing the player to attach a rope to surfaces within a certain range. The goal was to constrain movement along the rope while walking in hazards, adding an additional traversal mechanic.

I learned that managing character states dynamically requires careful design to ensure smooth transitions and clear feedback for the player. The gale system worked well in concept, but fine-tuning detection and UI feedback was crucial to avoid frustration. The rope and pole system, however, did not fully function as intended. Instead of restricting movement to the rope, the character could still move freely, which did not bring the effect I wanted.  Future iterations would need a more structured constraint system so that Unity’s physics system does not behave unexpectedly when trying to restrict movement.



## Prototype  Final

For the final iteration, I focused on spatial perception and player guidance by redesigning platform layouts to create visual illusions when viewed from a single camera's perspective. This encouraged players to switch between different perspectives to fully understand the level structure. I also reorganized collectibles to subtly lead players toward a point where the character triggers a gale alert before entering the gale zone. Besides, the camera system underwent major changes too as the free-look first-person view was replaced with a top-down orthographic perspective with a y-axis camera rotation, limiting the amount of information available from each angle. In this new free-look mode, player movement except jumping is no longer disallowed, so that the player would move to a desired position before switch back to the main camera. Additionally, the main camera was set to a front orthographic view, forcing the player to switch between the two perspectives to determine precise positioning. A grid system was briefly experimented to aid movement decisions but was later removed due to visual disturbance. Particle effects were added to the gale zone for a visual improvement. 

Working around spatial repositioning and player guidance through controlled perspectives and environmental cues, I learned how challenging level design is for a platformer game, where the playability relies heavily on it.  I experimented with how player perception can be manipulated to create certain challenges by redesigning the platforms and cameras to create visual illusions when viewed from a single angle and with how players can be guided to activate certain objects without explicit instructions using environmental elements, which can make the gameplay to be more fluent. The decision to allow movement and disable jumping in the look state also aims to achieve the effect that each perspective had different functions and limitations, encouraging players to actively switch between them. Experimenting with these adjustments, I gained valuable insights into how camera constraints can shape problem-solving and movement decisions and how intentional perspective limitations can add a little depth to a platforming experience.
![enter image description here](https://dfg1234556.github.io/game-dev-spring2025/pic/final1.png)
![enter image description here](https://dfg1234556.github.io/game-dev-spring2025/pic/final2.png)
[Prototype Final](https://dfg1234556.github.io/game-dev-spring2025/builds/platformer-final)
