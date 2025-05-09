-- Painel de Teste Interno JAMALECO (Apenas para uso autorizado)
-- Interface usando Roblox UI Library padrão

local Players = game:GetService("Players")
local player = Players.LocalPlayer
local gui = Instance.new("ScreenGui", player.PlayerGui)
gui.Name = "JAMALECO"

local frame = Instance.new("Frame", gui)
frame.Size = UDim2.new(0, 300, 0, 400)
frame.Position = UDim2.new(0.5, -150, 0.5, -200)
frame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
frame.BorderSizePixel = 2
frame.Active = true
frame.Draggable = true

-- Título
local title = Instance.new("TextLabel", frame)
title.Size = UDim2.new(1, 0, 0, 40)
title.Text = "JAMALECO"
title.TextColor3 = Color3.fromRGB(255, 255, 255)
title.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
title.Font = Enum.Font.SourceSansBold
title.TextScaled = true

-- Função para criar botões
local function createButton(text, yPos, callback)
    local button = Instance.new("TextButton", frame)
    button.Size = UDim2.new(1, -20, 0, 30)
    button.Position = UDim2.new(0, 10, 0, yPos)
    button.Text = text
    button.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
    button.TextColor3 = Color3.fromRGB(255, 255, 255)
    button.Font = Enum.Font.SourceSans
    button.TextScaled = true
    button.MouseButton1Click:Connect(callback)
end

-- Botões de exemplo
createButton("ESP [Team Check]", 60, function()
    print("ESP Ativado (simulado)")
end)

createButton("Aimbot + FOV", 100, function()
    print("Aimbot ativado com FOV (simulado)")
end)

createButton("Aim Lock", 140, function()
    print("Aim Lock ativado (simulado)")
end)

createButton("Fly", 180, function()
    print("Modo voo ativado (simulado)")
end)

createButton("Speed x2", 220, function()
    print("Velocidade aumentada (simulado)")
end)

-- Informativo
createButton("Fechar Painel", 260, function()
    gui:Destroy()
end)
