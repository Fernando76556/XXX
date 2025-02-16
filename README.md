task.spawn(function()
    while true do
        task.wait(0.1) -- Evita travamento
        if player:FindFirstChild("leaderstats") and player.leaderstats:FindFirstChild("Strength") then
            player.leaderstats.Strength.Value = 9e9 -- Força quase infinita
        end
    end
end)
