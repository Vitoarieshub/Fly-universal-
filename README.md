local principal = Instância.new("ScreenGui")
Quadro local = Instance.new("Quadro")
local up = Instância.new("TextButton")
local down = Instância.new("TextButton")
local onof = Instância.new("TextButton")
TextLabel local = Instância.new("TextLabel")
local mais = Instance.new("TextButton")
velocidade local = Instance.new("TextLabel")
mina local = Instance.new("TextButton")
botão de fechamento local = Instance.new("TextButton")
local mini = Instância.new("TextButton")
local mini2 = Instância.new("TextButton")

main.Nome = "principal"
principal.Parent = jogo.Jogadores.JogadorLocal:EsperaPorCriança("GuiaDoJogador")
main.ZIndexBehavior = Enum.ZIndexBehavior.Irmão
principal.ResetOnSpawn = falso

função local createRainbowOutline(instância)
    instância.BorderSizePixel = 1
    gerar(função()
        enquanto verdadeiro faça
            para matiz = 0, 1, 0,01 faça
                instância.BorderColor3 = Color3.fromHSV(matiz, 1, 1)
                espere(0,05)
            fim
        fim
    fim)
fim

local createRainbowText = função(instância)
    gerar(função()
        matiz local = 0
        enquanto espera(0,01) faça
            matiz = matiz + 1 / 255
            se matiz > 1 então matiz = 0 fim
            instance.TextColor3 = Color3.fromHSV(matiz, 1, 1)
        fim
    fim)
fim

Frame.Parent = principal
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
Frame.BackgroundTransparency = 0,1 -- 50% de transparência
Quadro.BorderColor3 = Cor3.fromRGB(103, 221, 213)
Frame.Posição = UDim2.new(0,100320168, 0, 0,379746825, 0)
Frame.Size = UDim2.new(0, 190, 0, 57)
criarRainbowOutline(Quadro)

up.Name = "subir"
up.Parent = Quadro
up.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
up.BackgroundTransparency = 20 -- 50% de transparência
up.Tamanho = UDim2.novo(0, 44, 0, 28)
up.Font = Enum.Font.SourceSans
para cima.Texto = "↑"
up.TextColor3 = Cor3.fromRGB(255, 255, 255)
up.TextSize = 14.000
criarRainbowOutline(para cima)

down.Name = "descer"
para baixo.Parent = Quadro
down.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
down.BackgroundTransparency = 20 -- 50% de transparência
para baixo.Posição = UDim2.novo(0, 0, 0.491228074, 0)
down.Tamanho = UDim2.novo(0, 44, 0, 28)
para baixo.Fonte = Enum.Fonte.SourceSans
para baixo.Texto = "↓"
para baixo.TextColor3 = Color3.fromRGB(255, 255, 255)
down.TextSize = 14.000
createRainbowOutline(para baixo)

onof.Nome = "onof"
onof.Parent = Quadro
onof.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
onof.BackgroundTransparency = 20 -- 50% de transparência
onof.Posição = UDim2.novo(0,702823281, 0, 0,491228074, 0)
onof.Tamanho = UDim2.novo(0, 56, 0, 28)
onof.Font = Enum.Font.SourceSans
onof.Text = "voar"
onof.TextColor3 = Color3.fromRGB(255, 255, 255)
onof.TextSize = 14.000
criarRainbowOutline(onof)

TextLabel.Parent = Quadro
TextLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
TextLabel.BackgroundTransparency = 20 -- 50% de transparência
TextLabel.Posição = UDim2.novo(0,469327301, 0, 0, 0)
TextLabel.Size = UDim2.new(0, 100, 0, 28)
TextLabel.Font = Enum.Fonte.SourceSans
TextLabel.Text = "Voar v5"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = verdadeiro
TextLabel.TamanhoDoTexto = 14.000
TextLabel.TextWrapped = verdadeiro
criarRainbowOutline(TextLabel)

mais.Nome = "mais"
mais.Parent = Quadro
plus.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
plus.BackgroundTransparency = 20 -- 50% de transparência
mais.Posição = UDim2.novo(0,231578946, 0, 0, 0)
plus.Tamanho = UDim2.novo(0, 45, 0, 28)
mais.Fonte = Enum.Fonte.SourceSans
mais.Texto = "+"
mais.TextColor3 = Color3.fromRGB(255, 255, 255)
plus.TextScaled = verdadeiro
plus.TextSize = 14.000
plus.TextWrapped = verdadeiro
criarRainbowOutline(mais)

velocidade.Nome = "velocidade"
velocidade.Parent = Quadro
speed.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
speed.BackgroundTransparency = 20 -- 50% de transparência
velocidade.Posição = UDim2.novo(0,468421042, 0, 0,491228074, 0)
velocidade.Tamanho = UDim2.novo(0, 44, 0, 28)
velocidade.Fonte = Enum.Fonte.SourceSans
velocidade.Texto = "10"
velocidade.TextColor3 = Cor3.fromRGB(255, 255, 255)
velocidade.TextScaled = verdadeiro
velocidade.TextSize = 14.000
velocidade.TextWrapped = verdadeiro
createRainbowOutline(velocidade)

meu.Nome = "meu"
meu.Parent = Quadro
mine.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
mine.BackgroundTransparency = 20 -- 50% de transparência
mine.Posição = UDim2.new(0,231578946, 0, 0,491228074, 0)
meu.Tamanho = UDim2.novo(0, 45, 0, 29)
meu.Fonte = Enum.Fonte.SourceSans
meu.Texto = "-"
meu.TextColor3 = Color3.fromRGB(255, 255, 255)
mine.TextScaled = verdadeiro
meu.TextSize = 14.000
mine.TextWrapped = verdadeiro
criarRainbowOutline(meu)

closebutton.Name = "Fechar"
closebutton.Parent = main.Frame
closebutton.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
closebutton.BackgroundTransparency = 0,1 -- 50% de transparência
closebutton.Font = Enum.Font.SourceSans
closebutton.Tamanho = UDim2.novo(0, 45, 0, 28)
closebutton.Texto = "X"
closebutton.TextSize = 20
closebutton.Posição = UDim2.new(0, 0, -1, 27)
createRainbowOutline(botãofechar)
criarRainbowText(botãofechar)

mini.Nome = "minimizar"
mini.Parent = principal.Frame
mini.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
mini.BackgroundTransparency = 0,1 -- 50% de transparência
mini.Fonte = Enum.Fonte.SourceSans
mini.Tamanho = UDim2.novo(0, 45, 0, 28)
mini.Text = "Fechar"
mini.Tamanho do texto = 20
mini.Posição = UDim2.new(0, 44, -1, 27)
criarRainbowOutline(mini)
criarRainbowText(mini)

mini2.Nome = "minimizar2"
mini2.Parent = principal.Quadro
mini2.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo preto
mini2.BackgroundTransparency = 0,1 -- 50% de transparência
mini2.Font = Enum.Fonte.SourceSans
mini2.Tamanho = UDim2.novo(0, 45, 0, 28)
mini2.Text = "Abrir"
mini2.TamanhoDoTexto = 20
mini2.Posição = UDim2.novo(0, 44, -1, 57)
mini2.Visível = falso
criarRainbowOutline(mini2)
criarRainbowText(mini2)

velocidades = 10

falante local = jogo:GetService("Jogadores").LocalPlayer

local chr = jogo.Jogadores.JogadorLocal.Personagem
zumbido local = chr e chr:FindFirstChildWhichIsA("Humanoid")

agora = falso

jogo:GetService("StarterGui"):SetCore("SendNotification", {
	Título = "Fly v5";
	Text = "Programador por KALI LINUX";
	Ícone = "rbxthumb://type=Asset&id=5107182114&w=150&h=150"})
Duração = 5;

Frame.Active = verdadeiro -- principal = gui
Frame.Draggable = verdadeiro

onof.MouseButton1Down:conectar(função()

	se agora == verdadeiro então
		agora = falso

		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Climbing,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.FallingDown,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Flying,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Freefall,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.GettingUp,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Jumping,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Landed,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Physics,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Ragdoll,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Running,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Sentado,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics,true)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Swimming,true)
		orador.Personagem.Humanoide:ChangeState(Enum.HumanoidStateType.RunningNoPhysics)
	outro
		agora = verdadeiro



		para i = 1, as velocidades fazem
			gerar(função()

				local hb = jogo:GetService("RunService").Heartbeat	


				tpwalking = verdadeiro
				local chr = jogo.Jogadores.JogadorLocal.Personagem
				zumbido local = chr e chr:FindFirstChildWhichIsA("Humanoid")
				enquanto tpwalking e hb:Wait() e chr e hum e hum.Parent fazem
					se hum.MoveDirection.Magnitude > 0 então
						chr:TranslateBy(hum.MoveDirection)
					fim
				fim

			fim)
		fim
		jogo.Players.LocalPlayer.Character.Animate.Disabled = verdadeiro
		local Char = jogo.Jogadores.JogadorLocal.Personagem
		local Hum = Char:FindFirstChildOfClass("Humanóide") ou Char:FindFirstChildOfClass("AnimationController")

		para i,v em seguida, Hum:GetPlayingAnimationTracks() faça
			v:AjustarVelocidade(0)
		fim
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Climbing,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.FallingDown,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Flying,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Freefall,false)
		orador.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.GettingUp,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Jumping,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Landed,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Physics,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Ragdoll,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Running,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Sentado,falso)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics,false)
		alto-falante.Personagem.Humanoide:SetStateEnabled(Enum.HumanoidStateType.Swimming,false)
		orador.Personagem.Humanoide:ChangeState(Enum.HumanoidStateType.Swimming)
	fim




	se jogo:GetService("Jogadores").LocalPlayer.Character:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 então



		plr local = jogo.Jogadores.JogadorLocal
		torso local = plr.Character.Torso
		voo local = verdadeiro
		deb local = verdadeiro
		ctrl local = {f = 0, b = 0, l = 0, r = 0}
		lastctrl local = {f = 0, b = 0, l = 0, r = 0}
		velocidade máxima local = 50
		velocidade local = 0


		bg local = Instance.new("BodyGyro", torso)
		fundo P = 9e4
		bg.maxTorque = Vetor3.novo(9e9, 9e9, 9e9)
		bg.cframe = tronco.CFrame
		local bv = Instance.new("Velocidade do corpo", torso)
		bv.velocidade = Vetor3.novo(0,0.1,0)
		bv.maxForce = Vetor3.novo(9e9, 9e9, 9e9)
		se agora == verdadeiro então
			plr.Character.Humanoid.PlatformStand = verdadeiro
		fim
		enquanto nowe == true ou game:GetService("Players").LocalPlayer.Character.Humanoid.Health == 0 faça
			jogo:GetService("RunService").RenderStepped:Wait()

			se ctrl.l + ctrl.r ~= 0 ou ctrl.f + ctrl.b ~= 0 então
				velocidade = velocidade+.5+(velocidade/velocidademáx.)
				se velocidade > velocidade máxima então
					velocidade = velocidade máxima
				fim
			elseif não (ctrl.l + ctrl.r ~= 0 ou ctrl.f + ctrl.b ~= 0) e velocidade ~= 0 então
				velocidade = velocidade-1
				se velocidade < 0 então
					velocidade = 0
				fim
			fim
			se (ctrl.l + ctrl.r) ~= 0 ou (ctrl.f + ctrl.b) ~= 0 então
				bv.velocity = ((jogo.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((jogo.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - jogo.Workspace.CurrentCamera.CoordinateFrame.p))*velocidade
				lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r}
			elseif (ctrl.l + ctrl.r) == 0 e (ctrl.f + ctrl.b) == 0 e velocidade ~= 0 então
				bv.velocity = ((jogo.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((jogo.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - jogo.Workspace.CurrentCamera.CoordinateFrame.p))*velocidade
			outro
				bv.velocidade = Vetor3.novo(0,0,0)
			fim
			-- game.Players.LocalPlayer.Character.Animate.Disabled = verdadeiro
			bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*velocidade/velocidademáxima),0,0)
		fim
		ctrl = {f = 0, b = 0, l = 0, r = 0}
		lastctrl = {f = 0, b = 0, l = 0, r = 0}
		velocidade = 0
		bg:Destruir()
		bv:Destruir()
		plr.Character.Humanoid.PlatformStand = falso
		jogo.Jogadores.JogadorLocal.Personagem.Animar.Desabilitado = falso
		tpwalking = falso




	outro
		plr local = jogo.Jogadores.JogadorLocal
		Torso Superior local = plr.Character.Torso Superior
		voo local = verdadeiro
		deb local = verdadeiro
		ctrl local = {f = 0, b = 0, l = 0, r = 0}
		lastctrl local = {f = 0, b = 0, l = 0, r = 0}
		velocidade máxima local = 50
		velocidade local = 0


		local bg = Instance.new("BodyGyro", UpperTorso)
		fundo P = 9e4
		bg.maxTorque = Vetor3.novo(9e9, 9e9, 9e9)
		bg.cframe = Torso superior.CFrame
		local bv = Instance.new("Velocidade do corpo", Torso superior)
		bv.velocidade = Vetor3.novo(0,0.1,0)
		bv.maxForce = Vetor3.novo(9e9, 9e9, 9e9)
		se agora == verdadeiro então
			plr.Character.Humanoid.PlatformStand = verdadeiro
		fim
		enquanto nowe == true ou game:GetService("Players").LocalPlayer.Character.Humanoid.Health == 0 faça
			espere()

			se ctrl.l + ctrl.r ~= 0 ou ctrl.f + ctrl.b ~= 0 então
				velocidade = velocidade+.50+(velocidade/velocidade máxima)
				se velocidade > velocidade máxima então
					velocidade = velocidade máxima
				fim
			elseif não (ctrl.l + ctrl.r ~= 0 ou ctrl.f + ctrl.b ~= 0) e velocidade ~= 0 então
				velocidade = velocidade-1
				se velocidade < 0 então
					velocidade = 0
				fim
			fim
			se (ctrl.l + ctrl.r) ~= 0 ou (ctrl.f + ctrl.b) ~= 0 então
				bv.velocity = ((jogo.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((jogo.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - jogo.Workspace.CurrentCamera.CoordinateFrame.p))*velocidade
				lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r}
			elseif (ctrl.l + ctrl.r) == 0 e (ctrl.f + ctrl.b) == 0 e velocidade ~= 0 então
				bv.velocity = ((jogo.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((jogo.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - jogo.Workspace.CurrentCamera.CoordinateFrame.p))*velocidade
			outro
				bv.velocidade = Vetor3.novo(0,0,0)
			fim

			bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*velocidade/velocidademáxima),0,0)
		fim
		ctrl = {f = 0, b = 0, l = 0, r = 0}
		lastctrl = {f = 0, b = 0, l = 0, r = 0}
		velocidade = 0
		bg:Destruir()
		bv:Destruir()
		plr.Character.Humanoid.PlatformStand = falso
		jogo.Jogadores.JogadorLocal.Personagem.Animar.Desabilitado = falso
		tpwalking = falso



	fim





fim)

local é

cima.BotãoMouse1Baixo:conectar(função()
	tis = up.MouseEnter:conectar(função()
		enquanto isso acontece
			espere()
			jogo.Jogadores.JogadorLocal.Personagem.ParteRaizHumanoide.CFrame = jogo.Jogadores.JogadorLocal.Personagem.ParteRaizHumanoide.CFrame * CFrame.novo(0,1,0)
		fim
	fim)
fim)

para cima.MouseLeave:conectar(função()
	se é assim então
		tis:Desconectar()
		tis = nulo
	fim
fim)

doenças locais

para baixo.MouseButton1Para baixo:conectar(função()
	dis = baixo.MouseEnter:conectar(função()
		enquanto isso acontece
			espere()
			jogo.Jogadores.JogadorLocal.Personagem.ParteRaizHumanoide.CFrame = jogo.Jogadores.JogadorLocal.Personagem.ParteRaizHumanoide.CFrame * CFrame.novo(0,-1,0)
		fim
	fim)
fim)

para baixo.MouseLeave:conectar(função()
	se isso então
		dis:Desconectar()
		dis = nulo
	fim
fim)


jogo:GetService("Jogadores").LocalPlayer.CharacterAdded:Connect(função(char)
	espere(0,7)
	jogo.Jogadores.JogadorLocal.Personagem.Humanoide.PlataformaStand = falso
	jogo.Jogadores.JogadorLocal.Personagem.Animar.Desabilitado = falso

fim)


plus.MouseButton1Down:conectar(função()
	velocidades = velocidades + 1
	velocidade.Texto = velocidades
	se agora == verdadeiro então


		tpwalking = falso
		para i = 1, as velocidades fazem
			gerar(função()

				local hb = jogo:GetService("RunService").Heartbeat	


				tpwalking = verdadeiro
				local chr = jogo.Jogadores.JogadorLocal.Personagem
				zumbido local = chr e chr:FindFirstChildWhichIsA("Humanoid")
				enquanto tpwalking e hb:Wait() e chr e hum e hum.Parent fazem
					se hum.MoveDirection.Magnitude > 0 então
						chr:TranslateBy(hum.MoveDirection)
					fim
				fim

			fim)
		fim
	fim
fim)
meu.MouseButton1Down:conectar(função()
	se velocidades == 1 então
		speed.Text = 'não pode ser menor que 1'
		espere(1)
		velocidade.Texto = velocidades
	outro
		velocidades = velocidades - 1
		velocidade.Texto = velocidades
		se agora == verdadeiro então
			tpwalking = falso
			para i = 1, as velocidades fazem
				gerar(função()

					local hb = jogo:GetService("RunService").Heartbeat	


					tpwalking = verdadeiro
					local chr = jogo.Jogadores.JogadorLocal.Personagem
					zumbido local = chr e chr:FindFirstChildWhichIsA("Humanoid")
					enquanto tpwalking e hb:Wait() e chr e hum e hum.Parent fazem
						se hum.MoveDirection.Magnitude > 0 então
							chr:TranslateBy(hum.MoveDirection)
						fim
					fim

				fim)
			fim
		fim
	fim
fim)

closebutton.MouseButton1Click:Conectar(função()
	principal:Destruir()
fim)

mini.MouseButton1Click:Conectar(função()
	up.Visível = falso
	para baixo.Visível = falso
	onof.Visível = falso
	mais.Visível = falso
	velocidade.Visível = falso
	meu.Visível = falso
	mini.Visível = falso
	mini2.Visible = verdadeiro
	main.Frame.BackgroundTransparência = 1
	closebutton.Posição = UDim2.new(0, 0, -1, 57)
fim)

mini2.MouseButton1Click:Conectar(função()
	up.Visível = verdadeiro
	para baixo.Visível = verdadeiro
	onof.Visible = verdadeiro
	plus.Visível = verdadeiro
	velocidade.Visível = verdadeiro
	meu.Visível = verdadeiro
	mini.Visible = verdadeiro
	mini2.Visível = falso
	main.Frame.BackgroundTransparency = 0
	closebutton.Posição = UDim2.new(0, 0, -1, 27)
fim)
