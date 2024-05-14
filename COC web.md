Creating a game like Clash of Clans in React with TypeScript, Tailwind CSS, and Jest for testing would be quite an extensive project, but I can outline a basic structure to get you started.

First, let's define the components you might need:

1. **Main Game Component:** This component will manage the overall game state.
2. **Buildings Component:** This component will handle rendering and managing buildings.
3. **Troops Component:** This component will handle rendering and managing troops.
4. **Resources Component:** This component will handle rendering and managing resources like gold, elixir, etc.
5. **Animations Component:** This component will handle animations for various actions in the game.
6. **Game Controls Component:** This component will handle user interactions and game controls.

Now, let's outline a basic structure for these components:



```typescript
// src/components/MainGame.tsx 
import React, { useState } from 'react'; import Buildings from './Buildings'; import Troops from './Troops'; import Resources from './Resources'; import GameControls from './GameControls';  const MainGame: React.FC = () => {   const [gold, setGold] = useState(1000);   const [elixir, setElixir] = useState(500);    return (     <div className="flex flex-col justify-center items-center w-full h-screen bg-gray-800">       <Buildings gold={gold} elixir={elixir} />       <Troops />       <Resources gold={gold} elixir={elixir} />       <GameControls />     </div>   ); };  export default MainGame;
```


```typescript
// src/components/Buildings.tsx
import React from 'react';  const Buildings: React.FC<{ gold: number; elixir: number }> = ({ gold, elixir }) => {   // Logic to render buildings };  export default Buildings;
```


```typescript
// src/components/Troops.tsx 
import React from 'react';  const Troops: React.FC = () => {  
// Logic to render troops
}; 
export default Troops;
```


```typescript
// src/components/Resources.tsx 
import React from 'react';  const Resources: React.FC<{ gold: number; elixir: number }> = ({ gold, elixir }) => {   
// Logic to render resources 
}; 
export default Resources;
```



```typescript
// src/components/GameControls.tsx 
import React from 'react';  const GameControls: React.FC = () => { 
// Logic to handle game controls 
};  
export default GameControls;
```

You can then add Tailwind CSS classes to style your components and animations, and implement Jest tests for your components to ensure they behave as expected.

This is just a basic starting point. Building a full-fledged game like Clash of Clans would require implementing various game mechanics, such as building placement, troop training, resource management, battles, etc. You would also need backend services for managing player data, storing game state, handling real-time interactions, etc.