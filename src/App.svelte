<script>
  import Todos from "./components/Todos.svelte";

  let todos = [
    { 
      id: 1, 
      name: "fix arrow bounding box", 
      completed: true 
    },
    { 
      id: 2, 
      name: "make arrow collide with walls", 
      completed: true 
    },
    {
      id: 3,
      name: "arrows limited, if out can't shoot can pick up arrows to shoot again",
      completed: false,
    },
    { id: 4, name: "add ui to display number of arrows", completed: false },
    {
      id: 5,
      name: "add goblin entity with animations make it follow player",
      completed: false,
    },
    {
      id: 6,
      name: "add health to player and goblin if goblin touches player player loses health, if player shoots goblin goblin loses health if either dies (health == 0) rotate sprite facing up",
      completed: false,
    },
  ];
</script>

<Todos {todos} />
