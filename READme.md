# assignment-05  

1. **getElementById**  
   -> use to select only one element by its id  
   -> gives single element or null if not there  

2. **getElementsByClassName**  
   -> use to select all elements with same class  
   -> return live HTMLCollection (not full array)  

3. **querySelector**  
   -> can select by any css selector (#id, .class, tag)  
   -> only gives first match  

4. **querySelectorAll**  
   -> same like querySelector but gives all  

2. how to create and insert element  
-> make element first  

const div = document.createElement("div")

-> write some text or add class  

div.textContent = "Hello world"
div.className = "my-box"

-> pick parent and put inside  

const box = document.getElementById("container")
box.appendChild(div)
 
3. event bubbling 
-> when click start on target element and go up parent by parent  
-> example  

<div id="parent">
  <button id="child">Click me</button>
</div>

if you click button event triggers on the button first

4. event delegation    
-> check which child clicked using event.target  
-> less code and works if new child add later  

5. preventDefault vs stopPropagation  
-> preventDefault() stop browser normal thing  
-> stopPropagation() stop bubbling so parent cannot run  
