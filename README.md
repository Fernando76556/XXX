local player = game.Players.LocalPlayer
local char = player.Character or player.CharacterAdded:Wait()

-- Ativa força infinita
task.spawn(function()
    while true do
        task.wait(0.1) -- Evita travamento
        if player:FindFirstChild("leaderstats") and player.leaderstats:FindFirstChild("Strength") then
            player.leaderstats.Strength.Value = 9e9 -- Força quase infinita
        end
    end
end)

-- Ativa renascimento automático
task.spawn(function()
    while true do
        task.wait(1) -- Ajuste o tempo conforme necessário
        local rebirthButton = game:GetService("Workspace"):FindFirstChild("RebirthButton") 
        if rebirthButton and rebirthButton:FindFirstChild("ClickDetector") then
            fireclickdetector(rebirthButton.ClickDetector) -- Simula clique para renascer
        end
    end
end)

print("🔥 Script de força infinita e renascimento ativado com sucesso! 🔥")
