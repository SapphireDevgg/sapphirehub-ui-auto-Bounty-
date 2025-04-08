local player = game.Players.LocalPlayer
local UIS = game:GetService("UserInputService")

local ScreenGui = Instance.new("ScreenGui")
ScreenGui.Name = "SapphireAutoBountyUI"
ScreenGui.Parent = player:WaitForChild("PlayerGui")
ScreenGui.ResetOnSpawn = false
ScreenGui.Enabled = false

local MainFrame = Instance.new("Frame")
MainFrame.Name = "MainFrame"
MainFrame.Parent = ScreenGui
MainFrame.Size = UDim2.new(0, 380, 0, 220)
MainFrame.Position = UDim2.new(0.5, -190, 0.5, -110)
MainFrame.BackgroundColor3 = Color3.fromRGB(160, 0, 0)
MainFrame.BorderSizePixel = 0
MainFrame.AnchorPoint = Vector2.new(0.5, 0.5)

local UICorner = Instance.new("UICorner", MainFrame)
UICorner.CornerRadius = UDim.new(0, 12)

local Title = Instance.new("TextLabel")
Title.Parent = MainFrame
Title.Size = UDim2.new(1, 0, 0, 50)
Title.BackgroundTransparency = 1
Title.Text = "SAPPHIRE AUTO BOUNTY"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.TextScaled = true
Title.Font = Enum.Font.GothamBold

local RedLineTop = Instance.new("Frame")
RedLineTop.Parent = MainFrame
RedLineTop.Size = UDim2.new(1, 0, 0, 2)
RedLineTop.Position = UDim2.new(0, 0, 0, 50)
RedLineTop.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
RedLineTop.BorderSizePixel = 0

local Description = Instance.new("TextLabel")
Description.Parent = MainFrame
Description.Size = UDim2.new(1, -40, 0, 110)
Description.Position = UDim2.new(0, 20, 0, 60)
Description.BackgroundTransparency = 1
Description.Text = "Welcome to the official Sapphire Hub Auto Bounty panel.\n\nThis UI is display-only. All actions run through the main script."
Description.TextColor3 = Color3.fromRGB(255, 200, 200)
Description.TextWrapped = true
Description.TextScaled = true
Description.Font = Enum.Font.Gotham

local RedLineBottom = Instance.new("Frame")
RedLineBottom.Parent = MainFrame
RedLineBottom.Size = UDim2.new(1, 0, 0, 2)
RedLineBottom.Position = UDim2.new(0, 0, 1, -2)
RedLineBottom.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
RedLineBottom.BorderSizePixel = 0

local Footer = Instance.new("TextLabel")
Footer.Parent = MainFrame
Footer.Size = UDim2.new(1, 0, 0, 20)
Footer.Position = UDim2.new(0, 0, 1, -24)
Footer.BackgroundTransparency = 1
Footer.Text = "Press ']' to open/close this panel."
Footer.TextColor3 = Color3.fromRGB(255, 100, 100)
Footer.TextScaled = true
Footer.Font = Enum.Font.Gotham

UIS.InputBegan:Connect(function(input, gameProcessed)
	if gameProcessed then return end
	if input.KeyCode == Enum.KeyCode.RightBracket then
		ScreenGui.Enabled = not ScreenGui.Enabled
	end
end)
