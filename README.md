local principal = Instance.new("ScreenGui")
local quadro = Instance.new("Frame")
local up = Instance.new("TextButton")
local down = Instance.new("TextButton")
local onof = Instance.new("TextButton")
local textLabel = Instance.new("TextLabel")
local mais = Instance.new("TextButton")
local velocidade = Instance.new("TextLabel")
local mina = Instance.new("TextButton")
local botaoFechar = Instance.new("TextButton")
local mini = Instance.new("TextButton")
local mini2 = Instance.new("TextButton")

principal.Name = "principal"
principal.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
principal.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
principal.ResetOnSpawn = false

function createRainbowOutline(instance)
    instance.BorderSizePixel = 1
    spawn(function()
        while true do
            for hue = 0, 1, 0.01 do
                instance.BorderColor3 = Color3.fromHSV(hue, 1, 1)
                wait(0.05)
            end
        end
    end)
end

function createRainbowText(instance)
    spawn(function()
        local hue = 0
        while wait(0.01) do
            hue = hue + 1 / 255
            if hue > 1 then hue = 0 end
            instance.TextColor3 = Color3.fromHSV(hue, 1, 1)
        end
    end)
end

quadro.Parent = principal
quadro.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
quadro.BackgroundTransparency = 0.1 -- 10% de transparência
quadro.BorderColor3 = Color3.fromRGB(103, 221, 213)
quadro.Position = UDim2.new(0, 100, 0, 0)
quadro.Size = UDim2.new(0, 190, 0, 57)
createRainbowOutline(quadro)

up.Name = "subir"
up.Parent = quadro
up.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
up.BackgroundTransparency = 0.2 -- 20% de transparência
up.Size = UDim2.new(0, 44, 0, 28)
up.Font = Enum.Font.SourceSans
up.Text = "↑"
up.TextColor3 = Color3.fromRGB(255, 255, 255)
up.TextSize = 14
createRainbowOutline(up)

down.Name = "descer"
down.Parent = quadro
down.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
down.BackgroundTransparency = 0.2 -- 20% de transparência
down.Position = UDim2.new(0, 0, 0.5, 0)
down.Size = UDim2.new(0, 44, 0, 28)
down.Font = Enum.Font.SourceSans
down.Text = "↓"
down.TextColor3 = Color3.fromRGB(255, 255, 255)
down.TextSize = 14
createRainbowOutline(down)

onof.Name = "onof"
onof.Parent = quadro
onof.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
onof.BackgroundTransparency = 0.2 -- 20% de transparência
onof.Position = UDim2.new(0, 100, 0, 0.5)
onof.Size = UDim2.new(0, 56, 0, 28)
onof.Font = Enum.Font.SourceSans
onof.Text = "voar"
onof.TextColor3 = Color3.fromRGB(255, 255, 255)
onof.TextSize = 14
createRainbowOutline(onof)

textLabel.Parent = quadro
textLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
textLabel.BackgroundTransparency = 0.2 -- 20% de transparência
textLabel.Position = UDim2.new(0, 60, 0, 0)
textLabel.Size = UDim2.new(0, 100, 0, 28)
textLabel.Font = Enum.Font.SourceSans
textLabel.Text = "Voar v5"
textLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
textLabel.TextScaled = true
textLabel.TextSize = 14
textLabel.TextWrapped = true
createRainbowOutline(textLabel)

mais.Name = "mais"
mais.Parent = quadro
mais.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
mais.BackgroundTransparency = 0.2 -- 20% de transparência
mais.Position = UDim2.new(0, 120, 0, 0)
mais.Size = UDim2.new(0, 45, 0, 28)
mais.Font = Enum.Font.SourceSans
mais.Text = "+"
mais.TextColor3 = Color3.fromRGB(255, 255, 255)
mais.TextScaled = true
mais.TextSize = 14
mais.TextWrapped = true
createRainbowOutline(mais)

velocidade.Name = "velocidade"
velocidade.Parent = quadro
velocidade.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
velocidade.BackgroundTransparency = 0.2 -- 20% de transparência
velocidade.Position = UDim2.new(0, 100, 0, 0.5)
velocidade.Size = UDim2.new(0, 44, 0, 28)
velocidade.Font = Enum.Font.SourceSans
velocidade.Text = "10"
velocidade.TextColor3 = Color3.fromRGB(255, 255, 255)
velocidade.TextScaled = true
velocidade.TextSize = 14
velocidade.TextWrapped = true
createRainbowOutline(velocidade)

mina.Name = "mina"
mina.Parent = quadro
mina.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
mina.BackgroundTransparency = 0.2 -- 20% de transparência
mina.Position = UDim2.new(0, 120, 0, 0.5)
mina.Size = UDim2.new(0, 45, 0, 28)
mina.Font = Enum.Font.SourceSans
mina.Text = "-"
mina.TextColor3 = Color3.fromRGB(255, 255, 255)
mina.TextScaled = true
mina.TextSize = 14
mina.TextWrapped = true
createRainbowOutline(mina)

botaoFechar.Name = "Fechar"
botaoFechar.Parent = quadro
botaoFechar.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
botaoFechar.BackgroundTransparency = 0.1 -- 10% de transparência
botaoFechar.Font = Enum.Font.SourceSans
botaoFechar.Size = UDim2.new(0, 45, 0, 28)
botaoFechar.Text = "X"
botaoFechar.TextSize = 20
botaoFechar.Position = UDim2.new(0, 0, -1, 27)
createRainbowOutline(botaoFechar)
createRainbowText(botaoFechar)

mini.Name = "minimizar"
mini.Parent = principal
mini.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
mini.BackgroundTransparency = 0.1 -- 10% de transparência
mini.Font = Enum.Font.SourceSans
mini.Size = UDim2.new(0, 45, 0, 28)
mini.Text = "Fechar"
mini.TextSize = 20
mini.Position = UDim2.new(0, 44, -1, 27)
createRainbowOutline(mini)
createRainbowText(mini)

mini2.Name = "minimizar2"
mini2.Parent = principal
mini2.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
mini2.BackgroundTransparency = 0.1 -- 10% de transparência
mini2.Font = Enum.Font.SourceSans
mini2.Size = UDim2.new(0, 45, 0, 28)
mini2.Text = "Abrir"
mini2.TextSize = 20
mini2.Position = UDim2.new(0, 44, -1, 57)
mini2.Visible = false
createRainbowOutline(mini2)
createRainbowText(mini2)

-- Função de controle de voo
local velocidades = 10
local player = game.Players.LocalPlayer
local character = player.Character
local humanoid = character and character:FindFirstChildWhichIsA("Humanoid")

local agora = false

game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "Fly v5";
    Text = "Programado por KALI LINUX";
    Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150";
    Duration = 5;
})

quadro.Active = true -- principal = gui
quadro.Draggable = true

onof.MouseButton1Down:Connect(function()
    if agora == true then
        agora = false
        humanoid.PlatformStand = false
        humanoid:ChangeState(Enum.HumanoidStateType.Physics)
    else
        agora = true
        humanoid.PlatformStand = true
        humanoid:ChangeState(Enum.HumanoidStateType.Physics)
    end
end)

mais.MouseButton1Down:Connect(function()
    velocidades = velocidades + 10
    velocidade.Text = velocidades
end)

mina.MouseButton1Down:Connect(function()
    if velocidades > 10 then
        velocidades = velocidades - 10
        velocidade.Text = velocidades
    end
end)

botaoFechar.MouseButton1Down:Connect(function()
    principal:Destroy()
end)

mini.MouseButton1Down:Connect(function()
    quadro.Visible = false
    mini.Visible = false
    mini2.Visible = true
end)

mini2.MouseButton1Down:Connect(function()
    quadro.Visible = true
    mini.Visible = true
    mini2.Visible = false
end)

game:GetService("RunService").Heartbeat:Connect(function()
    if agora == true then
        humanoid.PlatformStand = true
        humanoid:ChangeState(Enum.HumanoidStateType.Physics)
        character:SetPrimaryPartCFrame(character.PrimaryPart.CFrame + (character.PrimaryPart.CFrame.lookVector * velocidades / 5))
    end
end)
