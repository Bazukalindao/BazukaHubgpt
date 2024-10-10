local BazukaHub = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local AutoFarmButton = Instance.new("TextButton")

BazukaHub.Name = "BazukaHub"
BazukaHub.Parent = game.CoreGui

MainFrame.Name = "MainFrame"
MainFrame.Parent = BazukaHub
MainFrame.Size = UDim2.new(0, 300, 0, 200)
MainFrame.Position = UDim2.new(0.5, -150, 0.5, -100)
MainFrame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)

AutoFarmButton.Name = "AutoFarmButton"
AutoFarmButton.Parent = MainFrame
AutoFarmButton.Size = UDim2.new(0, 200, 0, 50)
AutoFarmButton.Position = UDim2.new(0.5, -100, 0.5, -25)
AutoFarmButton.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
AutoFarmButton.Text = "Auto Farm Level"

AutoFarmButton.MouseButton1Click:Connect(function()
    local level = 1
    while level < 2550 do
        local npc = findClosestNPC()
        if npc then
            startMission(npc)
        end
        farmLevel()
        level = getCurrentLevel()
    end
end)

function findClosestNPC()
end

function startMission(npc)
end

function farmLevel()
end

function getCurrentLevel()
    return math.random(1, 2550)
end
