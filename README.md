
local BazukaHub = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local ActivateButton = Instance.new("TextButton")

BazukaHub.Name = "BazukaHub"
BazukaHub.Parent = game.CoreGui

MainFrame.Name = "MainFrame"
MainFrame.Parent = BazukaHub
MainFrame.BackgroundColor3 = Color3.new(0.2, 0.2, 0.2)
MainFrame.Position = UDim2.new(0.5, -150, 0.5, -100)
MainFrame.Size = UDim2.new(0, 300, 0, 200)
MainFrame.BorderSizePixel = 2

Title.Name = "Title"
Title.Parent = MainFrame
Title.Text = "Bazuka Hub"
Title.TextColor3 = Color3.new(1, 1, 1)
Title.BackgroundTransparency = 1
Title.Size = UDim2.new(0, 300, 0, 50)
Title.Font = Enum.Font.SourceSansBold
Title.TextSize = 24

ActivateButton.Name = "ActivateButton"
ActivateButton.Parent = MainFrame
ActivateButton.BackgroundColor3 = Color3.new(0.3, 0.7, 0.3)
ActivateButton.Position = UDim2.new(0.5, -75, 0.6, 0)
ActivateButton.Size = UDim2.new(0, 150, 0, 50)
ActivateButton.Text = "Ativar Script"
ActivateButton.Font = Enum.Font.SourceSansBold
ActivateButton.TextSize = 20

ActivateButton.MouseButton1Click:Connect(function()
    print("Script do Bazuka Hub ativado!")
    -- Exemplo de função fictícia (adicione suas funções aqui)
    local player = game.Players.LocalPlayer
    player.Character.Humanoid.WalkSpeed = 100 -- Mudar a velocidade de movimento, por exemplo
end)
