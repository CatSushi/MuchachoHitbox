# MuchachoHitbox

A lightweight, flexible, easy to use hitbox module for Roblox that's been used by thousands of developers for over 3 years.

## Why MuchachoHitbox?

- **Simple API** - Get up and running in seconds with intuitive, property-based configuration
- **Velocity Prediction** - Automatically predicts moving part positions for accurate hit detection
- **Multiple Detection Modes** - Default, HitOnce, HitParts, and ConstantDetection modes for different use cases
- **TouchEnded Events** - Handle both hit start and hit end for damage-over-time and area effects
- **Reliable** - Used by thousands of developers in production games
- **Lightweight** - Clean, readable code that's easy to understand and modify

## Quick Start

```lua
local MuchachoHitbox = require(path.to.MuchachoHitbox)

-- Create a hitbox
local hitbox = MuchachoHitbox.CreateHitbox()
hitbox.Size = Vector3.new(10, 10, 10)
hitbox.CFrame = workspace.Part

-- Handle hits
hitbox.Touched:Connect(function(hit, humanoid)
    print("Hit:", hit.Name)
    if humanoid then
        humanoid:TakeDamage(10)
    end
end)

-- Start the hitbox
hitbox:Start()
```

CFrame can either be a vector3, or an instance (will follow said instance)
```lua
  hitbox.CFrame = CFrame.new(10,10,10)
  -- or
  hitbox.CFrame = CFrame.new(workspace.Part)
```

## Key Features

### Velocity Prediction
```lua
hitbox.VelocityPrediction = true
hitbox.VelocityPredictionTime = 0.2
```
Perfect for fast-moving projectiles and combat systems.

### Detection Modes
- **Default** - Hit humanoids once with debounce
- **HitOnce** - Stop after first hit
- **HitParts** - Hit any parts, not just humanoids
- **ConstantDetection** - No debounce, constant detection

### Visual Debug
```lua
hitbox.Visualizer = true
hitbox.VisualizerColor = Color3.fromRGB(255, 0, 0)
hitbox.VisualizerTransparency = 0.8
```

## Installation

1. Download the `MuchachoHitbox.rbxm` file
2. Import it into Roblox Studio
3. Place it in `ServerStorage` or wherever you keep your modules

## Documentation

For complete documentation, examples, and advanced usage, check the [Wiki](https://github.com/CatSushi/MuchachoHitbox/wiki).

## Philosophy

MuchachoHitbox is designed to be a simple tool that doesn't get in your way. It gives you a clean hitbox system and lets you build whatever you want around it. Want client-side hitboxes? Just put it in a LocalScript. Need custom networking? Go for it! Want to tweak the detection logic? The code is straightforward and easy to modify.
## Community

- **YouTube**: [Your Channel Name](https://www.youtube.com/@SushiMasterOfficial)
- **DevForum**: [Your DevForum](https://devforum.roblox.com/t/muchachohitbox-an-easy-to-use-spatialquery-based-hitbox-system/3682320)
- Found a bug? Open an issue!
- Have a feature request? Let's discuss it!

## License

MIT License - see [LICENSE](LICENSE) file for details

---

*Used by thousands of developers since 2022*
