-- Configuração de elementos de UI
TextLabel.Text = "Voar v5"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 14
TextLabel.TextWrapped = true
criarRainbowOutline(TextLabel)

mais.Name = "mais"
mais.Parent = Quadro
mais.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
mais.BackgroundTransparency = 0.2
mais.Position = UDim2.new(0, 231, 0, 0)
mais.Size = UDim2.new(0, 45, 0, 28)
mais.Font = Enum.Font.SourceSans
mais.Text = "+"
mais.TextColor3 = Color3.fromRGB(255, 255, 255)
mais.TextScaled = true
mais.TextSize = 14
mais.TextWrapped = true
criarRainbowOutline(mais)

velocidade.Name = "velocidade"
velocidade.Parent = Quadro
velocidade.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
velocidade.BackgroundTransparency = 0.2
velocidade.Position = UDim2.new(0, 468, 0, 0)
velocidade.Size = UDim2.new(0, 44, 0, 28)
velocidade.Font = Enum.Font.SourceSans
velocidade.Text = "10"
velocidade.TextColor3 = Color3.fromRGB(255, 255, 255)
velocidade.TextScaled = true
velocidade.TextSize = 14
velocidade.TextWrapped = true
criarRainbowOutline(velocidade)

meu.Name = "meu"
meu.Parent = Quadro
meu.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
meu.BackgroundTransparency = 0.2
meu.Position = UDim2.new(0, 231, 0, 0)
meu.Size = UDim2.new(0, 45, 0, 29)
meu.Font = Enum.Font.SourceSans
meu.Text = "-"
meu.TextColor3 = Color3.fromRGB(255, 255, 255)
meu.TextScaled = true
meu.TextSize = 14
meu.TextWrapped = true
criarRainbowOutline(meu)

closebutton.Name = "Fechar"
closebutton.Parent = main.Frame
closebutton.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
closebutton.BackgroundTransparency = 0.1
closebutton.Font = Enum.Font.SourceSans
closebutton.Size = UDim2.new(0, 45, 0, 28)
closebutton.Text = "X"
closebutton.TextSize = 20
closebutton.Position = UDim2.new(0, 0, -1, 27)
criarRainbowOutline(closebutton)
criarRainbowText(closebutton)

mini.Name = "minimizar"
mini.Parent = main.Frame
mini.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
mini.BackgroundTransparency = 0.1
mini.Font = Enum.Font.SourceSans
mini.Size = UDim2.new(0, 45, 0, 28)
mini.Text = "Fechar"
mini.TextSize = 20
mini.Position = UDim2.new(0, 44, -1, 27)
criarRainbowOutline(mini)
criarRainbowText(mini)

mini2.Name = "minimizar2"
mini2.Parent = main.Frame
mini2.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
mini2.BackgroundTransparency = 0.1
mini2.Font = Enum.Font.SourceSans
mini2.Size = UDim2.new(0, 45, 0, 28)
mini2.Text = "Abrir"
mini2.TextSize = 20
mini2.Position = UDim2.new(0, 44, -1, 57)
mini2.Visible = false
criarRainbowOutline(mini2)
criarRainbowText(mini2)

-- Iniciando variáveis de controle
local velocidades = 10
local player = game:GetService("Players").LocalPlayer
local chr = player.Character
local humanoid = chr and chr:FindFirstChildWhichIsA("Humanoid")
local agora = false

-- Notificação inicial
game:GetService("StarterGui"):SetCore("SendNotification", {
    Title = "Fly v5";
    Text = "Programador por KALI LINUX";
    Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150"
})
wait(5)

main.Frame.Active = true
main.Frame.Draggable = true

-- Alternando o estado de voo
onof.MouseButton1Down:Connect(function()
    if agora then
        agora = false
        -- Desabilitar estados do Humanoide
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Climbing, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.FallingDown, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Flying, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Freefall, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.GettingUp, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Landed, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Physics, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Ragdoll, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Running, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Sitting, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics, true)
        humanoid:SetStateEnabled(Enum.HumanoidStateType.Swimming, true)
        humanoid:ChangeState(Enum.HumanoidStateType.RunningNoPhysics)
    else
        agora = true
    end
end)

-- Função para aumentar a velocidade
plus.MouseButton1Down:Connect(function()
    velocidades = velocidades + 1
    velocidade.Text = velocidades
    if agora then
        tpwalking = false
        for i = 1, velocidades do
            spawn(function()
                local hb = game:GetService("RunService").Heartbeat
                tpwalking = true
                local chr = game.Players.LocalPlayer.Character
                local humanoid = chr and chr:FindFirstChildWhichIsA("Humanoid")
                while tpwalking and hb:Wait() and chr and humanoid and humanoid.Parent do
                    if humanoid.MoveDirection.Magnitude > 0 then
                        chr:TranslateBy(humanoid.MoveDirection)
                    end
                end
            end)
        end
    end
end)

-- Função para diminuir a velocidade
meu.MouseButton1Down:Connect(function()
    if velocidades > 1 then
        velocidades = velocidades - 1
        velocidade.Text = velocidades
        if agora then
            tpwalking = false
            for i = 1, velocidades do
                spawn(function()
                    local hb = game:GetService("RunService").Heartbeat
                    tpwalking = true
                    local chr = game.Players.LocalPlayer.Character
                    local humanoid = chr and chr:FindFirstChildWhichIsA("Humanoid")
                    while tpwalking and hb:Wait() and chr and humanoid and humanoid.Parent do
                        if humanoid.MoveDirection.Magnitude > 0 then
                            chr:TranslateBy(humanoid.MoveDirection)
                        end
                    end
                end)
            end
        end
    else
        velocidade.Text = "Não pode ser menor que 1"
        wait(1)
        velocidade.Text = velocidades
    end
end)

-- Fechar botão
closebutton.MouseButton1Click:Connect(function()
    main:Destroy()
end)

-- Minimizar / Restaurar interface
mini.MouseButton1Click:Connect(function()
    up.Visible = false
    para baixo.Visible = false
    onof.Visible = false
    plus.Visible = false
    velocidade.Visible = false
    meu.Visible = false
    mini.Visible = false
    mini2.Visible = true
    main.Frame.BackgroundTransparency = 1
    closebutton.Position = UDim2.new(0, 0, -1, 57)
end)

mini2.MouseButton1Click:Connect(function()
    up.Visible = true
    para baixo.Visible = true
    onof.Visible = true
    plus.Visible = true
    velocidade.Visible = true
    meu.Visible = true
    mini.Visible = true
    mini2.Visible = false
    main.Frame.BackgroundTransparency = 0
    closebutton.Position = UDim2.new(0, 0, -1, 27)
end)
