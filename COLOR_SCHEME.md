# Birthday Project - Complete Color Scheme

## 🎨 Primary Color Palette

### Main Colors
- **Primary Pink**: `#ff6b9d` - Main brand color, used for buttons, highlights, and primary elements
- **Deep Pink**: `#c44569` - Secondary brand color, used for gradients and accents
- **Light Pink**: `#f8b5d3` - Tertiary brand color, used for backgrounds and subtle elements
- **Gold**: `#ffd700` - Accent color for special text and highlights

### Background Gradients
```css
/* Main background gradient */
background: linear-gradient(135deg, #ff6b9d, #c44569, #f8b5d3);

/* Alternative gradients */
background: linear-gradient(45deg, #ff6b9d, #c44569);
background: linear-gradient(45deg, #f8b5d3, #ff6b9d);
background: linear-gradient(45deg, #c44569, #ff6b9d);
```

## 🎯 Color Usage by Element

### Text Colors
- **Primary Text**: `white` - Main content text
- **Accent Text**: `#ffd700` - Special headings and highlights
- **Secondary Text**: `rgba(255, 255, 255, 0.9)` - Subtle text
- **Selection Text**: `#333` - Text when selected

### Button Colors
```css
/* Primary buttons */
background: linear-gradient(45deg, #ff6b9d, #c44569);
color: white;

/* Hover state */
background: linear-gradient(45deg, #c44569, #ff6b9d);
```

### Card Colors
```css
/* Card backgrounds */
background: rgba(255, 255, 255, 0.1);
backdrop-filter: blur(10px);
border: 1px solid rgba(255, 255, 255, 0.2);

/* Card hover */
background: rgba(255, 255, 255, 0.2);
```

### Interactive Elements
```css
/* Scrollbar */
background: linear-gradient(45deg, #ff6b9d, #c44569);

/* Selection highlight */
background: rgba(255, 107, 157, 0.3);

/* Glow effects */
box-shadow: 0 0 20px rgba(255, 107, 157, 0.5);
text-shadow: 0 0 10px rgba(255, 107, 157, 0.8);
```

## 🌈 Animation Colors

### Confetti Colors
```css
/* Confetti pieces use these colors */
--color: #ff6b9d;
--color: #c44569;
--color: #f8b5d3;
--color: #ffd700;
```

### Candle Flame
```css
/* Candle flame gradient */
background: linear-gradient(to bottom, #ffd700, #ff6b35);
```

### Cake Layers
```css
/* Cake layer gradients */
.layer-bottom { background: linear-gradient(45deg, #ff6b9d, #c44569); }
.layer-middle { background: linear-gradient(45deg, #f8b5d3, #ff6b9d); }
.layer-top { background: linear-gradient(45deg, #c44569, #ff6b9d); }
.icing { background: linear-gradient(45deg, #fff, #f0f0f0); }
```

## 📱 CSS Variables for Easy Implementation

```css
:root {
  /* Primary Colors */
  --primary-pink: #ff6b9d;
  --deep-pink: #c44569;
  --light-pink: #f8b5d3;
  --gold: #ffd700;
  
  /* Gradients */
  --main-gradient: linear-gradient(135deg, #ff6b9d, #c44569, #f8b5d3);
  --button-gradient: linear-gradient(45deg, #ff6b9d, #c44569);
  --hover-gradient: linear-gradient(45deg, #c44569, #ff6b9d);
  
  /* Transparencies */
  --card-bg: rgba(255, 255, 255, 0.1);
  --card-border: rgba(255, 255, 255, 0.2);
  --selection-bg: rgba(255, 107, 157, 0.3);
  
  /* Text Colors */
  --text-primary: white;
  --text-accent: #ffd700;
  --text-secondary: rgba(255, 255, 255, 0.9);
  --text-selection: #333;
  
  /* Effects */
  --glow-pink: rgba(255, 107, 157, 0.5);
  --glow-text: rgba(255, 107, 157, 0.8);
}
```

## 🎨 Complete Color Implementation

### For HTML/CSS Projects
```css
/* Import the color scheme */
@import url('https://fonts.googleapis.com/css2?family=Instrument+Sans:wght@400;600;900&display=swap');

:root {
  /* Copy all CSS variables from above */
}

/* Apply to your elements */
.primary-button {
  background: var(--button-gradient);
  color: var(--text-primary);
  border-radius: 25px;
  padding: 15px 30px;
  border: none;
  cursor: pointer;
  transition: all 0.3s ease;
}

.primary-button:hover {
  background: var(--hover-gradient);
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.card {
  background: var(--card-bg);
  backdrop-filter: blur(10px);
  border: 1px solid var(--card-border);
  border-radius: 20px;
  padding: 2rem;
}

.gradient-bg {
  background: var(--main-gradient);
  min-height: 100vh;
}

.accent-text {
  color: var(--text-accent);
  font-weight: 600;
}
```

## 🎯 Color Psychology

- **#ff6b9d (Primary Pink)**: Love, warmth, celebration, joy
- **#c44569 (Deep Pink)**: Passion, depth, sophistication
- **#f8b5d3 (Light Pink)**: Gentleness, romance, sweetness
- **#ffd700 (Gold)**: Luxury, celebration, special moments, happiness

## 📋 Quick Copy Colors

```
Primary Pink: #ff6b9d
Deep Pink: #c44569
Light Pink: #f8b5d3
Gold: #ffd700
White: #ffffff
```

## 🎨 Usage Tips

1. **Primary Pink (#ff6b9d)** - Use for main buttons, links, and primary actions
2. **Deep Pink (#c44569)** - Use for secondary elements and hover states
3. **Light Pink (#f8b5d3)** - Use for backgrounds and subtle accents
4. **Gold (#ffd700)** - Use sparingly for special highlights and important text
5. **White** - Use for main text on dark backgrounds
6. **Gradients** - Use the provided gradients for backgrounds and buttons

This color scheme creates a romantic, celebratory, and warm atmosphere perfect for birthday and love-themed projects! 