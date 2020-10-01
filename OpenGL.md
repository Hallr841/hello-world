# OpenGL


lesson 101

Creating context figuring out what verison you are running 


include the libaries

what is glew

	#include <stdlib.h>
	#define GLEW_STATIC
	#include <GL/glew.h>
	#include "GLFW/glfw3.h"	
	#include <iostream>

this is using the class 

	using namespace std;



window code guts


initatie of  code

	int main(int argc, char * argv[]){

pointer to the window * equal pointer?

    GLFWwindow * window;
 
    if (!glfwInit()) exit(EXIT_FAILURE);
    window = 

create the window  with w,h name and if the fails 
we exit
 what is the null null?
 
	glfwCreateWindow(1024,768,"glfw",NULL,NULL);
    if (!window) {
        glfwTerminate();
        exit(EXIT_FAILURE);
    }
  
  set window to current context
   
  	glfwMakeContextCurrent(window);
    
   //Get Version String
          
  	const GLubyte * p = glGetString(GL_VERSION);
  	cout << "OpenGL Version: " << p << endl;
  	return 0;
	}


glfw manages window context


Create a window with GlFW


1. include

2. here
 	code guts 
 	
 	 int main (){ 
 	 if(!glfwInit())exit(EXIT_FAILURE);
 	 
 	 int w = 1024; 
 	 int h= 768;
 	 
 	 GLFWwindow * window;
 	 window =glfwCreateWindow(w,h,"glfw",NULL,NuLL);
 	 
 	 if(!window){
 	 glfwTerminate();
 	  exit(EXIT_FAILURE);
 	 }
 	 glfwContextCurrent(window);
 	 
 	 printf("hello window\n");
 	 
 	 
 	/*-----------------
 	  main loop
 	 ------------------*/
 	 
 		 while(!glfwWindowShouldClose(window)){
 		
 		 glViewport(0,0,w,h);     //set Viewport in pixels
 		 glClearColor(1,0,0,1);  //CLEAR WINDOW CONTENTS
 	 	 glClear(GL_COLOR_BUFFER_BIT|Gl_DEPTH_BUFFER_BIT);
 	 
 	 //put drawing code in here
 	 	
 	 	 glfwSwappBuffers(window);  //<---SWAP BUFFER
 	 	 glfwPollEvents();  
 	 
 	 	}
 	 
 	 
 	 Destroy window and terminate glfw
 	 
 	 	glfwDestroyWindow(window);
 	 	glfwTerminate();
 	 	printf("goodbye window\n");
 	 	return 0;
 	 	e }
  



