-- Create a ScreenGui for the GUI
local gui = Instance.new("ScreenGui")
gui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Create a Frame for the draggable GUI
local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 300, 0, 300)  -- Boyutları burada değiştirdik
frame.Position = UDim2.new(0.5, -150, 0.5, -150)
frame.BackgroundColor3 = Color3.new(0, 0, 0)
frame.BackgroundTransparency = 0.5
frame.Active = true
frame.Draggable = true
frame.Parent = gui

-- Create a button for Nameless Admin
local namelessAdminButton = Instance.new("TextButton")
namelessAdminButton.Size = UDim2.new(0.8, 0, 0.2, 0)
namelessAdminButton.Position = UDim2.new(0.1, 0, 0.1, 0)
namelessAdminButton.BackgroundColor3 = Color3.new(0, 0, 1)
namelessAdminButton.Text = "Nameless Admin"
namelessAdminButton.Parent = frame

-- Create a button for Infinite Yield
local infiniteYieldButton = Instance.new("TextButton")
infiniteYieldButton.Size = UDim2.new(0.8, 0, 0.2, 0)
infiniteYieldButton.Position = UDim2.new(0.1, 0, 0.3, 0)
infiniteYieldButton.BackgroundColor3 = Color3.new(0, 1, 0)
infiniteYieldButton.Text = "Infinite Yield"
infiniteYieldButton.Parent = frame

-- Create a button for Fly V3
local flyV3Button = Instance.new("TextButton")
flyV3Button.Size = UDim2.new(0.8, 0, 0.2, 0)
flyV3Button.Position = UDim2.new(0.1, 0, 0.5, 0)
flyV3Button.BackgroundColor3 = Color3.new(1, 0, 0)
flyV3Button.Text = "Fly V3"
flyV3Button.Parent = frame

-- Create a button for SystemBroken
local systemBrokenButton = Instance.new("TextButton")
systemBrokenButton.Size = UDim2.new(0.8, 0, 0.2, 0)
systemBrokenButton.Position = UDim2.new(0.1, 0, 0.7, 0)
systemBrokenButton.BackgroundColor3 = Color3.new(1, 1, 0)
systemBrokenButton.Text = "SystemBroken"
systemBrokenButton.Parent = frame

-- Function to execute scripts based on button clicks
local function executeScript(scriptUrl)
    return function()
        loadstring(game:HttpGet(scriptUrl))()
    end
end

-- Connect button clicks to script execution functions
namelessAdminButton.MouseButton1Click:Connect(executeScript("https://raw.githubusercontent.com/FilteringEnabled/NamelessAdmin/main/Source"))
infiniteYieldButton.MouseButton1Click:Connect(executeScript('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))
flyV3Button.MouseButton1Click:Connect(executeScript("https://raw.githubusercontent.com/XNEOFF/FlyGuiV3/main/FlyGuiV3.txt"))
systemBrokenButton.MouseButton1Click:Connect(executeScript("https://raw.githubusercontent.com/H20CalibreYT/SystemBroken/main/script"))
