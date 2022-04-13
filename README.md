![image](https://user-images.githubusercontent.com/92790405/163167173-57a795b1-ec52-43d9-aa4d-3f5c7a6cdd6f.png)

# NFT-Preview-Card-Component
HTML

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- displays site properly based on user's device -->
  <link href="stylesheet.css" rel="stylesheet">
  <link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">
  
  <title>Frontend Mentor | NFT preview card component</title>

  <!-- Feel free to remove these styles or customise in your own stylesheet 👍 -->
  <style>
    .attribution { font-size: 11px; text-align: center; }
    .attribution a { color: hsl(228, 45%, 44%); }
  </style>
</head>
<body>
  <div class="main-container">

    <div class="container">
        <img src="../nft-preview-card-component-main/images/image-equilibrium.jpg" alt="image of equilibrium" class="image1">
        <div class="title">
          <h1>Equilibrium #3429</h1>
          <p class="product-desc">Our Equilibrium collection promotes balance and calm.</p>
        </div>

      <div class="bid">
        <div class="equilibrium">
          <img src="../nft-preview-card-component-main/images/icon-ethereum.svg" alt="equilibrim icon">
        </div>
          <p class="price">0.041 ETH</p>
        <div class="timer-icon">
          <img src="../nft-preview-card-component-main/images/icon-clock.svg" alt="clock icon">
        </div>
        <p class="date">3 days left</p>
      </div>

      <div class="profile">
        <img src="../nft-preview-card-component-main/images/image-avatar.png" alt="profile image" class="image2">
        <p class="creator">Creation of <a href="#" target="_blank">Jules Wyvern</a></p>
      </div>
    </div>
  </div>
  
  <div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
    Coded by <a href="#">Daisuke Mogi</a>.
  </div>
</body>
</html>

CSS

*,
*::before,
*::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

:root {
    --primary-main: hsl(217, 54%, 11%);
    --primary-card: hsl(216, 50%, 16%);
    --primary-line: hsl(215, 32%, 27%);
    --primary-white: hsl(0, 0%, 100%);
    --primary-blue: hsl(215, 51%, 70%);
    --primary-cyan: hsl(178, 100%, 50%);
}

body {
    font-size: 1.125rem;
    font-family: 'Work Sans', sans-serif;
    background-color: var(--primary-main);
    display: grid;
    grid-template-columns: auto-fit(1fr);
}

.main-container {
    display: flex;
    justify-content: center;
    margin: 1em auto;
}

.container {
    background-color: var(--primary-card);
    text-align: center;
    max-width: 90%;
    border-radius: 1em;
}

.image1 {
    max-width: 80%;
    margin-top: 1em;
    border-radius: 0.5em;
    cursor: pointer;
}

.title {
    margin: 0.5em 1em;
    padding: 0 0.8em;
    text-align: left;
}

.title h1 {
    color: var(--primary-white);
    font-size: 1.5rem;
}

.title p {
    color: hsl(215.2, 28.5%, 43.3%);
    font-size: 0.9rem;
    margin: 1rem 0;
}

.bid {
    display: flex;
    margin: 1em 1.8em 0.5em 1.8em;
    justify-content: space-between;
    position: relative;
}

.price {
    font-size: 0.9rem;
    font-weight: 550;
    color: var(--primary-cyan);
    margin-right: 5em;
}

.timer-icon {
    margin-left: 0.5em;
}

.date {
    color: var(--primary-blue);
    font-size: 0.9rem;
    font-weight: 600;
}

.bid::before {
    content: "";
    position: absolute;
    border: 1px solid var(--primary-line);
    width: 100%;
    bottom: -50%;
    margin: 0 auto;
}

.profile {
    display: flex;
    align-items: center;
    gap: 1em;
    padding: 1em 0px 1.2em 0px;
}

.image2 {
    max-width: 10%;
    margin-left: 1.8em;
    border-radius: 50%;
    border: 1.5px solid var(--primary-white);
    cursor: pointer;
}

.creator {
    color: var(--primary-blue);
    font-size: 0.8rem;
    font-weight: 600;
}

.creator a {
    text-decoration: none;
    color: var(--primary-white);
    font-weight: 400;
}

.creator a:hover {
    opacity: 0.8;
    transition: 0.3s;
}

.attribution {
    color: var(--primary-blue);
}

.attribution a:hover {
    color: var(--primary-blue);
}

@media screen and (min-width: 1440px) {

    body {
        display: grid;
        grid-template-columns: 1fr;
    }
    
    .main-container {
        max-width: 30%;
        margin: 2em auto;
    }

    .price {
        margin-right: 8em;
    }
}
