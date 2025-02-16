while true do
    local part = Instance.new("Part")
    part.Parent = game.Workspace
    part.Position = Vector3.new(math.random(-100,100), math.random(10,50), math.random(-100,100))
    part.Size = Vector3.new(5,5,5)
    part.Anchored = true
    part.BrickColor = BrickColor.Random()
    wait(0.01) -- Ajuste o tempo para causar mais ou menos lag
end
