---
layout: essay
type: essay
title: "Building Software with a Blueprint"
# All dates must be YYYY-MM-DD format!
date: 2024-12-4
published: true
labels:
  - Design Patterns
  - Software Architecture
  - React
---
### Design Patterns as Software Architecture

When constructing a house, you wouldn't start by nailing random drywall onto the foundation, or pouring concrete aimlessly. Instead, the construction team would follow detailed blueprints and plans that rely on previously established patterns and principles, to create a properly constructed home. In software development, design patterns serve a similar purpose to us with the construction of projects. These patterns, developed and refined by the software development community over decades, provide structured approaches to solving common programming challenges. They are the guidelines that bring intention and understanding to what would otherwise be a chaotic codebase. Applying design patterns is similar to building a home, with each part of the project contributing to building our digital project 'house'. In this, I am both the architect and the builder. The blueprints (design patterns) guide my decisions, and the actual coding is the construction work. Just as blueprints provide standard solutions to architecture challenges, design patterns solve recurring software architecture problems.

Design patterns form the base of the architecture of a project, offering solutions to common challenges, and creating maintainability and scalability. Essentially, just solving the recurring problems within any codebase or project. In a recent web application project, the component pattern is central to the design. Like rooms in a house, components each serve a distinct purpose when creating our larger structure. Each component encapsulates the components layout, logic, and styling into a self-contained unit. Just like a kitchen or a bedroom has a specific function within a house, and the blueprint for that room can be used as many times as you need in the planning of the home, components are also modular pieces that can be reused and altered without impacting the larger project. However, just as a house needs more than just singular rooms to become a house, we need more than just components to make a functioning app. We need to look at how the components are styled, how they are put together, to create our 'house'.

#### Building the Structure

In a house, the framework (beams, walls, and wiring etc) provides the structural integrity and setup, and the decor adds an aesthetic, personal design to the home after it is built. These components of a house parallel my use of container and presentational patterns in my project. The container components manage the logic and data flow, while presentational components in the CSS styling files handle individual rendering. Let's look at a practical example of how these patterns work together in a real application:

``` typescript 
interface Recipe {
  id: number;
  title: string;
  imageUrl: string;
  cookTime: string;
  category: string;
}

const recipes: Recipe[] = [
  {
    id: 1,
    title: 'Superfood fruit salad',
    imageUrl: '/landing-img/acai.png',
    cookTime: '30 Minutes',
    category: 'Healthy',
  },
  {
    id: 2,
    title: 'Steak frites in your dorm',
    imageUrl: '/landing-img/steakmeal.png',
    cookTime: '30 Minutes',
    category: 'Western',
  },
  {
    id: 3,
    title: 'Fried rice with veges and eggs',
    imageUrl: '/landing-img/ricemeal.png',
    cookTime: '30 Minutes',
    category: 'Healthy',
  },
// With all the recipes following this structure
];
```

<img src="/img/design-patterns-interface-example.png" alt="Example of the Recipe interface implementation" style="max-width: calc(100% - 40px); padding: 0 20px; display: block;">

#### Styling the Architecture

The layout of this house is created using CSS grid styling (a flexible way to arrange elements in columns and rows) and flexbox (a layout model for arranging items in a container), which arranges the rooms (components) into the cohesive design of the home (project). The styling for this in the .categories-grid class organizes this recipe data into a visually pleasing and understandable grid layout, similar to how interior designers organize rooms to have functional use and aesthetic design.

#### The Building Codes of Software

Every home must adhere to building codes to ensure safety and structural integrity. In software, Typescript interfaces (contracts that define the structure of data) and prop definitions serve as our built-in building codes for the digital home we are building, ensuring each component only deals with the data it is designed to, so it functions correctly. Take the post interface in the Instablog component for example: 
```typescript
interface Post {
  id: number;
  likes: number;
  likedBy: string;
  date: string;
  caption: string;
}
```
#### Bringing It All Together

Just as building codes specify standard door widths and ceiling heights, this interface ensures every post shown on the site has the required properties. The final assembly of the house is defined in the Composition Pattern. Just as an architect arranges the rooms and requirements into the final blueprints and design for a house, the separated page.tsx files for each linked page, composes all the individual components to serve a purpose on a functional webpage. This is where all the pieces come together, the room design, layout, structure, etc, to create a complete, aesthetically pleasing and usable application.


Design patterns are the blueprints that ensure a project is built with intent and precision. They solve common reoccurring problems within a project, allowing for developers to have a shared understanding of structure and functionality. By applying common React design patterns like the composition, container, presentational, and component patterns, I was able to build a digital 'house' that mirrors real-world construction principles. Through this lens of design patterns, my projects are more than collections of code - they are carefully architected solutions designed to evolve and scale with changing requirements, just as well-designed houses can be renovated and expanded while maintaining their structural integrity.
