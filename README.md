local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local Button = Instance.new("TextButton")

ScreenGui.Name = "BazukaHub"
ScreenGui.Parent = game.CoreGui

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
Frame.Size = UDim2.new(0, 400, 0, 300)
Frame.Position = UDim2.new(0.5, -200, 0.5, -150)

Title.Parent = Frame
Title.Text = "Bazuka Hub"
Title.Size = UDim2.new(0, 400, 0, 50)
Title.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.Font = Enum.Font.SourceSans
Title.TextSize = 30

Button.Parent = Frame
Button.Text = "Pegar Tudo"
Button.Size = UDim2.new(0, 200, 0, 50)
Button.Position = UDim2.new(0.5, -100, 0.5, 0)
Button.BackgroundColor3 = Color3.fromRGB(60, 60, 60)
Button.TextColor3 = Color3.fromRGB(255, 255, 255)
Button.Font = Enum.Font.SourceSans
Button.TextSize = 20

Button.MouseButton1Click:Connect(function()
    print("Tentando pegar tudo no jogo...")
    -- Aqui você colocaria o código para interagir com o jogo, o que no caso seria um hack ilegal.
end)
