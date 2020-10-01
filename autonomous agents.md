# autonomous agents


  perceive environment limited 
  process information to calculate an action 
  has no leader unless set 
  
####   Turtles, Termites, and Traffic Jams by Mitchel Resnick
  read
  
  
### whats going to happen 


action selection 
 a vechinle has a goal seeking a target, avoid and obstacle and following a path

steering

 once an action has been selected the vehicle has
  to calculate it next move 
   steering force = desired velocity - current velocity

locomotion 
 left right left right foot 
 with circle , triangles this doesn't really matter 
  but add illusion or effect  to show  this  paddles or wheels
  
  
  steer force
  
  
   steering force = desired  velocity -current velocity 
   
   asking the vechile to make intelligent decision
   (how fast and in what direction) 
   
   	Pvector steer = Pvector.sub(desired,velocity);
   	
   what is desired 
   the desired velocity
   would be 
   
   	Pvector desired = Pvector.Sub(target,location);
   	
   this would teleport use because  it would happen instantly without set  ammount of pixel to travel
   
   need to add  
   		
   		float maxspeed;
   	
  to a class 
   	
   so know we take are vector scale it down by normalize then we mult it by max speed
   
   Pvector desired = Pvector.Sub(target,location);
   desired.normalize();
   desired.mult(maxspeed);
   
 put in all together in a function 
 
 	void seek(PVector target){
 	
 		// find
 	Pvector desired = Pvector.Sub(target,location);
   	desired.normalize();
   	desired.mult(maxspeed);
   
   	//where to move too
  	Pvector steer = Pvector.sub(desired,velocity);
   
  	 applyForce(Steer);
 	 
 	}
   
   
   
   can limited the magnitude of the  steering force
   by  float maxforce
   
   applying to the function 
   
   
   
    	void seek(PVector target){
 	
 		// find
 	Pvector desired = Pvector.Sub(target,location);
   	desired.normalize();
   	desired.mult(maxspeed);
   
   	//where to move too
  	Pvector steer = Pvector.sub(desired,velocity);
   
   steer.limit(maxforce);
   applyForce(Steer);
  	 
 	 
 	}
   
   
 
  
  
  
  
  