local function comma(num)
    local formatted = tostring(num)
    while true do
        local k
        formatted, k = string.gsub(formatted, "^(-?%d+)(%d%d%d)", "%1,%2")
        if k == 0 then break end
    end
    return formatted
end

local Blocks = game.Players.LocalPlayer.PlayerGui.ScreenGui.StatsFrame.Tokens:Clone()
Blocks.Logo.Image = 'rbxassetid://15906467021'
Blocks.More:Destroy()
Blocks.Amount.TextColor3 = game.Players.LocalPlayer.PlayerGui.ScreenGui.StatsFrame.Coins.Amount.TextColor3
Blocks.Amount.Text = comma(game.Players.LocalPlayer:WaitForChild("leaderstats"):WaitForChild("Blocks Mined").Value)
Blocks.Position = UDim2.new(0, 0, 1.566, 10)
Blocks.Parent = game.Players.LocalPlayer.PlayerGui.ScreenGui.StatsFrame

local Rebs = game.Players.LocalPlayer.PlayerGui.ScreenGui.StatsFrame.Tokens:Clone()
Rebs.Logo.Image = 'rbxassetid://15906467021'
Rebs.More:Destroy()
Rebs.Amount.TextColor3 = game.Players.LocalPlayer.PlayerGui.ScreenGui.StatsFrame.Coins.Amount.TextColor3
Rebs.Amount.Text = comma(game.Players.LocalPlayer:WaitForChild("leaderstats"):WaitForChild("Rebirths").Value)
Rebs.Position = UDim2.new(0, 0, 2.162, 10)
Rebs.Parent = game.Players.LocalPlayer.PlayerGui.ScreenGui.StatsFrame

game.Players.LocalPlayer:WaitForChild("leaderstats"):WaitForChild("Blocks Mined"):GetPropertyChangedSignal("Value"):Connect(function()
    Blocks.Amount.Text = comma(game.Players.LocalPlayer:WaitForChild("leaderstats"):WaitForChild("Blocks Mined").Value)
end)

game.Players.LocalPlayer:WaitForChild("leaderstats"):WaitForChild("Rebirths"):GetPropertyChangedSignal("Value"):Connect(function()
    Rebs.Amount.Text = comma(game.Players.LocalPlayer:WaitForChild("leaderstats"):WaitForChild("Rebirths").Value)
end)
