


------------------ฟังชั่นต่างๆ------------------------------------------------------
function CA()
for i,v in pairs(game:GetService("Workspace").Chests:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
fireproximityprompt(v,30)
end
      end
      		end

function No()
for i, v in ipairs(workspace.Lives:GetChildren()) do
    if not game:GetService("Players"):GetPlayerFromCharacter(v) then -- if not player 
        local cleanedName = string.gsub(v.Name, "%d+$", "")
        v.Name = tostring(cleanedName)
    end
end

workspace.Lives.ChildAdded:Connect(function(model)
task.wait()
if not game:GetService("Players"):GetPlayerFromCharacter(model) then -- if not player then
        local cleanedName = string.gsub(model.Name, "%d+$", "")
        model.Name = cleanedName
				end
		end)
end

No()
------------------------------------------------------------------------------------------
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/LPO081/Ui-or/main/README.md')))()

local Window = OrionLib:MakeWindow({
		Name = "[ VIP ] SSS HUB [Shadow] Second Piece",
		HidePremium = false,
		SaveConfig = true,
		ConfigFolder = "OrionTest",
        IntroText = "BY NOOB-SCRIPT V2"       
}) 

local Tab = Window:MakeTab({
	Name = "| Equip Weapon",
	Icon = "rbxassetid://7733765398",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Weapon"
})
--------------------tableอาวุธ--------------------
local Weaponlist = {}
local Weapon = nil
for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
    table.insert(Weaponlist,v.Name)
    end
------------------------------------------------------------

Tab:AddDropdown({
	Name = "Select Weapon",
	Default = "1",
	Options = Weaponlist,
	Callback = function(v)
	_G.Weapon = v
	end    
})

Tab:AddToggle({
	Name = "Auto Equip Weapon",
	Default = false,
	Callback = function(a)
	_G.AutoEquiped = a
	end    
})

spawn(function()
while wait() do
if _G.AutoEquiped then
pcall(function()
game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(_G.Weapon))
end)
end
end
end)    


local Section = Tab:AddSection({
	Name = "Auto Attack"
})


Tab:AddToggle({
	Name = "Auto Attack",
	Default = false,
	Callback = function(ah)
	_G.Ato = ah
while _G.Ato do wait()
game:GetService'VirtualUser':CaptureController()
game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end
	end    
})

local Section = Tab:AddSection({
	Name = " "
})

Tab:AddToggle({
	Name = "Auto Z X C V",
	Default = false,
	Callback = function(he)
	        _G.EZo = he
        while _G.EZo do wait()
game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)
game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
end
	end    
})


local Tab = Window:MakeTab({
	Name = "• Auto Farm Level",
	Icon = "rbxassetid://16591537806",
	PremiumOnly = false
})

Quest = {}
for i,v in pairs(workspace.Quest:GetDescendants()) do
    if v.Name == "Quest" then
        table.insert(Quest,v.Value)
    end
end

Tab:AddDropdown({
	Name = "Select Quest",
	Default = "1",
	Options = Quest,
	Callback = function(text)
	    Questname = text
    function Quest()
        spawn(function()
            _G.Quest = true
            while _G.Quest do wait()
                pcall(function()
                    if not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") then
                        for i,v in pairs(workspace.Quest:GetDescendants()) do
                            if v.Name == "Quest" and v.Value == Questname then
                                 game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(v.Parent.Parent.Position)
                                 fireproximityprompt(v.Parent)
                             end
                         end
                    end
                    wait()
                end)
            end
        end)
    end

    if Questname == "Bandit" then
        function mobs2()
        spawn(function()
            _G.mobs2 = true
            while _G.mobs2 do wait()
                pcall(function()
                    local function GetClosestPlayer()
                    local target = nil
                    for i,v in pairs(workspace.Lives:GetDescendants()) do
                        if v.Name == "Humanoid" and v.MaxHealth == 50 and v.Health > 0 then
                            target = v
                        end
                     end
                     return target
                    end
                     repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = GetClosestPlayer().RootPart.CFrame*CFrame.new(0,5,0)*CFrame.Angles(math.rad(-90),0,0)
                    until not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") or _G.mobs2 == false
                    return Quest()
                end)
            end
        end)
    end
    elseif Questname == "Bandit Leader" then
        function mobs2()
        spawn(function()
            _G.mobs2 = true
            while _G.mobs2 do wait()
                pcall(function()
                    local function GetClosestPlayer()
                    local target = nil
                    for i,v in pairs(workspace.Lives:GetDescendants()) do
                        if v.Name == "Humanoid" and v.MaxHealth == 350 and v.Health > 0 then
                            target = v
                        end
                     end
                     return target
                    end
                     repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = GetClosestPlayer().RootPart.CFrame*CFrame.new(0,5,0)*CFrame.Angles(math.rad(-90),0,0)
                    until not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") or _G.mobs2 == false
                    return Quest()
                end)
            end
        end)
    end
    elseif Questname == "Clown Pirate" then
        function mobs2()
        spawn(function()
            _G.mobs2 = true
            while _G.mobs2 do wait()
                pcall(function()
                    local function GetClosestPlayer()
                    local target = nil
                    for i,v in pairs(workspace.Lives:GetDescendants()) do
                        if v.Name == "Humanoid" and v.MaxHealth == 500 and v.Health > 0 then
                            target = v
                        end
                     end
                     return target
                    end
                     repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = GetClosestPlayer().RootPart.CFrame*CFrame.new(0,5,0)*CFrame.Angles(math.rad(-90),0,0)
                    until not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") or _G.mobs2 == false
                    return Quest()
                end)
            end
        end)
    end
    elseif Questname == "Marine" then
        function mobs2()
        spawn(function()
            _G.mobs2 = true
            while _G.mobs2 do wait()
                pcall(function()
                    local function GetClosestPlayer()
                    local target = nil
                    for i,v in pairs(workspace.Lives:GetDescendants()) do
                        if v.Name == "Humanoid" and v.MaxHealth == 850 and v.Health > 0 then
                            target = v
                        end
                     end
                     return target
                    end
                     repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = GetClosestPlayer().RootPart.CFrame*CFrame.new(0,5,0)*CFrame.Angles(math.rad(-90),0,0)
                    until not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") or _G.mobs2 == false
                    return Quest()
                end)
            end
        end)
    end
    elseif Questname == "Monkey" then
        function mobs2()
        spawn(function()
            _G.mobs2 = true
            while _G.mobs2 do wait()
                pcall(function()
                    local function GetClosestPlayer()
                    local target = nil
                    for i,v in pairs(workspace.Lives:GetDescendants()) do
                        if v.Name == "Humanoid" and v.MaxHealth == 1500 and v.Health > 0 then
                            target = v
                        end
                     end
                     return target
                    end
                     repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = GetClosestPlayer().RootPart.CFrame*CFrame.new(0,5,0)*CFrame.Angles(math.rad(-90),0,0)
                    until not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") or _G.mobs2 == false
                    return Quest()
                end)
            end
        end)
    end
    elseif Questname == "Monkey King" then
        function mobs2()
        spawn(function()
            _G.mobs2 = true
            while _G.mobs2 do wait()
                pcall(function()
                    local function GetClosestPlayer()
                    local target = nil
                    for i,v in pairs(workspace.Lives:GetDescendants()) do
                        if v.Name == "Humanoid" and v.MaxHealth == 3500 and v.Health > 0 then
                            target = v
                        end
                     end
                     return target
                    end
                     repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = GetClosestPlayer().RootPart.CFrame*CFrame.new(0,5,0)*CFrame.Angles(math.rad(-90),0,0)
                    until not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") or _G.mobs2 == false
                    return Quest()
                end)
            end
        end)
    end
    elseif Questname == "Snow Bandit" then
        function mobs2()
        spawn(function()
            _G.mobs2 = true
            while _G.mobs2 do wait()
                pcall(function()
                    local function GetClosestPlayer()
                    local target = nil
                    for i,v in pairs(workspace.Lives:GetDescendants()) do 
                        if v.Name == "Humanoid" and v.MaxHealth == 15000 and v.Health > 0 then
                            target = v
                        end
                     end
                     return target
                    end
                     repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = GetClosestPlayer().RootPart.CFrame*CFrame.new(0,5,0)*CFrame.Angles(math.rad(-90),0,0)
                    until not game:GetService("Players").LocalPlayer:FindFirstChild("Quest") or _G.mobs2 == false
                    return Quest()
                end)
            end
        end)
    end
    end

	end    
})

Tab:AddToggle({
	Name = "Auto Quest",
	Default = false,
	Callback = function(value)
	_G.Quest = value
    print('Quest: ', value);
    if value then
        Quest();
        _G.Quest = true
        else
        _G.Quest = false
    end
	end    
})

Tab:AddToggle({
	Name = "Auto Equip Weapon",
	Default = false,
	Callback = function(value)
	_G.mobs2 = value
    print('mobs2: ', value);
    if value then
        mobs2();
        _G.mobs2 = true
        else
        _G.mobs2 = false
        _G.Quest = false
    end
	end    
})

local Tab = Window:MakeTab({
	Name = "• Auto Farm Boss",
	Icon = "rbxassetid://16591537806",
	PremiumOnly = false
})


Tab:AddToggle({
    Name = "Auto Farm Boss",
    Default = false,
    Callback = function(ssk)
_G.eami = ssk
function MonsSpawned(Mons)
    for _, v in pairs(game:GetService('Workspace').Lives:GetDescendants()) do
        if v.Name == Mons and v:FindFirstChild('HumanoidRootPart') and v.Humanoid.Health >= 1 then
            return true
        end
    end
    return false
end

spawn(function()
    while wait() do
       pcall(function()
            if _G.eami then
                local MonNames = {
                    'Shadow',
                    'Gojo',
                    'Kashimo',
                    'Sukuna',
                    'Artoria',
                    'Uraume',
		              'Gojo [Unleashed]',
                    'Sukuna [Half Power]',
		              'Rimuru',
                    'Killua',
                    'Ichigo',
                    'Choso',
	           	      'Natsu',
                    'Gilgamesh',
		    'Tatsumaki',
      'Frieren'
		    

                }



                for _, v in pairs(game:GetService('Workspace').Lives:GetDescendants()) do
                    if table.find(MonNames, v.Name) and v:FindFirstChild('HumanoidRootPart') and v.Humanoid.Health >= 1 then
                        repeat
                        CA()
                           wait()   
                            v.HumanoidRootPart.Size = Vector3.new(10, 10, 10)
                            v.HumanoidRootPart.Transparency = 0.9
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,0,6)
                        until _G.eami == false or v.Humanoid.Health <= 0
                    end
                end
            end
        end)
    end
end)

	end   
})

Tab:AddToggle({

    Name = "Auto Farm Gem ",

    Default = false,

    Callback = function(ssn)


_G.eam = ssn

function MonsSpawned(Mons)

    for _, v in pairs(game:GetService('Workspace').Lives:GetDescendants()) do

        if v.Name == Mons and v:FindFirstChild('HumanoidRootPart') and v.Humanoid.Health >= 1 then

            return true

        end

    end

    return false

end



spawn(function()
    while wait() do
        pcall(function()
            if _G.eam then
                local MonNames = {
                    
		              'Gojo [Unleashed]',
                    'Sukuna [Half Power]',
		              'Rimuru',
                    'Killua',
                    'Ichigo',
                    'Choso',
                    'Natsu',
                    'Gilgamesh',
                    'Snow Bandit Leader',
                    'Shank',
                    'Monkey King',
                    'Sand Man',
                    'Bomb Man',
                    'Bandit Leader',
                    'Shadow',
                    'Gojo',
                    'Kashimo',
                    'Sukuna',
                    'Artoria',
                    'Uraume',
		    'Tatsumaki',
      'Frieren'
		    

                }
                
                for _, v in pairs(game:GetService('Workspace').Lives:GetDescendants()) do
                    if table.find(MonNames, v.Name) and v:FindFirstChild('HumanoidRootPart') and v.Humanoid.Health >= 1 then
                       repeat

                        CA()
                            wait()   
                            v.HumanoidRootPart.Size = Vector3.new(10, 10, 10)
                            v.HumanoidRootPart.Transparency = 0.9
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,0,6)

                        until _G.eam == false or v.Humanoid.Health <= 0
                    end
                end
            end
        end)
    end
end)

	end   

})

local Tab = Window:MakeTab({
	Name = "• Stats ",
	Icon = "rbxassetid://16591537806",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "Auto UP Melee",
	Default = false,
	Callback = function(Melee)
_G.Melee = Melee
while _G.Melee do wait() 
    pcall(function()
    local args = {
    [1] = "Melee",
    [2] = 10
}
game:GetService("ReplicatedStorage").Remotes.UpStats:FireServer(unpack(args))
    end)
    end
	end    
})

Tab:AddToggle({
	Name = "Auto UP Weapon",
	Default = false,
	Callback = function(Weapon)
_G.Weapon = Weapon
while _G.Weapon do wait() 
    pcall(function()
local args = {
    [1] = "Weapon",
    [2] = 10
}
game:GetService("ReplicatedStorage").Remotes.UpStats:FireServer(unpack(args))
    end)
    end
	end    
})

Tab:AddToggle({
	Name = "Auto UP Defense",
	Default = false,
	Callback = function(Defense)
_G.Defense = Defense
while _G.Defense do wait() 
    pcall(function()
    local args = {
    [1] = "Defense",
    [2] = 10
}
game:GetService("ReplicatedStorage").Remotes.UpStats:FireServer(unpack(args))
    end)
    end
	end    
})

Tab:AddToggle({
	Name = "Auto UP Demon Fruit",
	Default = false,
	Callback = function(Fruit)
_G.Fruit = Fruit
while _G.Fruit do wait() 
    pcall(function()
    local args = {
    [1] = "DemonFruit",
    [2] = 10
}
game:GetService("ReplicatedStorage").Remotes.UpStats:FireServer(unpack(args))
    end)
    end
	end    
})

local Tab = Window:MakeTab({
	Name = "| Teleport ",
	Icon = "rbxassetid://7733765398",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Go to Traveling merchant",
	Callback = function()
for i,v in pairs(game:GetService("Workspace").NPC["Traveling merchant"]:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,3,0)
wait(0.1)
fireproximityprompt(v,30)
end
      end
  	end    
})

local Tab = Window:MakeTab({
	Name = "• Teleport Shop",
	Icon = "rbxassetid://16591537806",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Shop"
})

    shop = {}
for i ,v in pairs(game:GetService("Workspace").Shop:GetChildren()) do
table.insert(shop,v.Name)
end

Tab:AddDropdown({
	Name = "Select Shop",
	Default = "1",
	Options = shop,
	Callback = function(ma)
	shop = ma
	end    
})

Tab:AddButton({
	Name = "TP Shop",
	Callback = function()
      		for i,v in pairs(game:GetService("Workspace").Shop[shop]:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,5,0)
end
      end
  	end    

})

local Tab = Window:MakeTab({
	Name = "• Teleport island",
	Icon = "rbxassetid://16591537806",
	PremiumOnly = false
})

map = {}
for i ,v in pairs(game:GetService("Workspace").Locations:GetChildren()) do
table.insert(map,v.Name)
end

local Section = Tab:AddSection({
	Name = "island"
})

Tab:AddDropdown({
	Name = "Select Island",
	Default = "1",
	Options = map,
	Callback = function(mt)
	map = mt
	end    
})



Tab:AddButton({
	Name = "TP Island",
	Callback = function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Locations[map].CFrame * CFrame.new(0,-100,0)
  	end    

})

local Section = Tab:AddSection({
	Name = " "
})
local Section = Tab:AddSection({
	Name = " "
})
local Section = Tab:AddSection({
	Name = " "
})
local Section = Tab:AddSection({
	Name = " "
})

local Tab = Window:MakeTab({
	Name = "• Players",
	Icon = "rbxassetid://16591537806",
	PremiumOnly = false
})

Plr = {}
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name)
end

Tab:AddDropdown({
	Name = "Select Players",
	Default = "1",
	Options = Plr,
	Callback = function(t)
		PlayerTP = t
	end    
})


Tab:AddButton({
	Name = "Teleport To Players Select",
	Callback = function()
      			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
  	end    
})


Tab:AddToggle({
	Name = "Loop Teleport To Players Select",
	Default = false,
	Callback = function(tp)
	_G.hre = tp
while _G.hre do wait()
      			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame * CFrame.new(0,0,3)
end
	end    
})

local Tab = Window:MakeTab({
	Name = "| Random Fruit",
	Icon = "rbxassetid://7733765398",
	PremiumOnly = false
})

local fruit = {
"Not Select",
"Dark Flame Fruit",
"God Light Fruit"
}




Tab:AddDropdown({
	Name = "Select Fruit",
	Default = "Not Select",
	Options = fruit,
	Callback = function(GG)
	_G.FruitSelect = GG
	end    
})

Tab:AddToggle({
	Name = "Auto Random Fruit Gem Select",
	Default = false,
	Callback = function(FSE)
	_G.FruitRD = FSE
	end    
})

Tab:AddToggle({
	Name = "Auto Random Fruit Beli Select",
	Default = false,
	Callback = function(Fr)
	_G.FruitB = Fr
	end    
})

local FruitGem = -741.048889, 43.4787788, -1933.82019, -0.0251465552, 7.8026531e-08, 0.999683797, -1.09866749e-09, 1, -7.80788483e-08, -0.999683797, -3.06173398e-09, -0.0251465552

local FruitBeil = 790.203735, 35.5073013, 1201.40369, 0.026754817, -8.37544611e-09, 0.999642015, 1.24128064e-07, 1, 5.05623188e-09, -0.999642015, 1.23948354e-07, 0.026754817

spawn(function()
                        while wait() do
                            pcall(function()
                              if _G.FruitRD then
for i,v in pairs(game:GetService("Workspace").Shop:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
fireproximityprompt(v,30)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-741.048889, 43.4787788, -1933.82019, -0.0251465552, 7.8026531e-08, 0.999683797, -1.09866749e-09, 1, -7.80788483e-08, -0.999683797, -3.06173398e-09, -0.0251465552)
 if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(_G.FruitSelect)) then
   break
												end
										end
								end
						end
				end)
		end
end)

spawn(function()
                        while wait() do
                            pcall(function()
                              if _G.FruitB then
for i,v in pairs(game:GetService("Workspace").Shop:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
fireproximityprompt(v,30)
   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(790.203735, 35.5073013, 1201.40369, 0.026754817, -8.37544611e-09, 0.999642015, 1.24128064e-07, 1, 5.05623188e-09, -0.999642015, 1.23948354e-07, 0.026754817)
 if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(_G.FruitSelect)) then
   break
												end
										end
								end
						end
				end)
		end
end)



spawn(function()
while wait()do
 if _G.FruitRD then
   if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(_G.FruitSelect)) then
   wait(1)
    OrionLib:MakeNotification({
	Name = "You Got Fruit Select!",
	Content = "WoW!!!!",
	Image = "rbxassetid://4483345998",
	Time = 5
})
   end
   end
end
end)

spawn(function()
while wait()do
 if _G.FruitB then
   if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(_G.FruitSelect)) then
   wait(1)
      OrionLib:MakeNotification({
	Name = "You Got Fruit Select!",
	Content = "WoW!!!!",
	Image = "rbxassetid://4483345998",
	Time = 5
})
   end
   end
end
end)
  
local Tab = Window:MakeTab({
	Name = "| Test",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "Grabtools",
	Default = false,
	Callback = function(K)
_G.F = K
while _G.F do wait()
for i,v in pairs(game:GetService("Workspace").ItemDrop:GetChildren()) do
  v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		  end
  	end
	end    
})


Tab:AddToggle({
	Name = "Auto Chests TP",
	Default = false,
	Callback = function(d)
_G.Fd = d
while _G.Fd do wait()
for i,v in pairs(game:GetService("Workspace").Chests:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
fireproximityprompt(v,30)
game.Players.LocalPlayer.Character.HumanoidRootPart .CFrame = v.Parent.CFrame
end
      end
            end
	end    
})




Tab:AddButton({
	Name = "boost fps",
	Callback = function()

local decalsyeeted = true 
local g = game
local w = g.Workspace
local l = g.Lighting
local t = w.Terrain
sethiddenproperty(l,"Technology",2)
sethiddenproperty(t,"Decoration",false)
t.WaterWaveSize = 0
t.WaterWaveSpeed = 0
t.WaterReflectance = 0
t.WaterTransparency = 0
l.GlobalShadows = 0
l.FogEnd = 9e9
l.Brightness = 0
settings().Rendering.QualityLevel = "Level01"
for i, v in pairs(w:GetDescendants()) do
    if v:IsA("BasePart") and not v:IsA("MeshPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
    elseif (v:IsA("Decal") or v:IsA("Texture")) and decalsyeeted then
        v.Transparency = 1
    elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
        v.Lifetime = NumberRange.new(0)
    elseif v:IsA("Explosion") then
        v.BlastPressure = 1
       v.BlastRadius = 1
    elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
        v.Enabled = false
    elseif v:IsA("MeshPart") and decalsyeeted then
        v.Material = "Plastic"
        v.Reflectance = 0
        v.TextureID = 10385902758728957
    elseif v:IsA("SpecialMesh") and decalsyeeted  then
        v.TextureId=0
    elseif v:IsA("ShirtGraphic") and decalsyeeted then
        v.Graphic=0
    elseif (v:IsA("Shirt") or v:IsA("Pants")) and decalsyeeted then
        v[v.ClassName.."Template"]=0
    end
end
for i = 1,#l:GetChildren() do
    e=l:GetChildren()[i]
    if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
        e.Enabled = false
    end
end
w.DescendantAdded:Connect(function(v)
    wait()--prevent errors and shit
   if v:IsA("BasePart") and not v:IsA("MeshPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
    elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
        v.Transparency = 1
    elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
        v.Lifetime = NumberRange.new(0)
    elseif v:IsA("Explosion") then
        v.BlastPressure = 1
        v.BlastRadius = 1
    elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
        v.Enabled = false
    elseif v:IsA("MeshPart") and decalsyeeted then
        v.Material = "Plastic"
        v.Reflectance = 0
        v.TextureID = 10385902758728957
    elseif v:IsA("SpecialMesh") and decalsyeeted then
        v.TextureId=0
    elseif v:IsA("ShirtGraphic") and decalsyeeted then
        v.ShirtGraphic=0
    elseif (v:IsA("Shirt") or v:IsA("Pants")) and decalsyeeted then
        v[v.ClassName.."Template"]=0
              end
        end)
  	end    
})

Tab:AddToggle({
	Name = "Auto Haki",
	Default = false,
	Callback = function(Haki)
_G.AutoHaki = Haki
while _G.AutoHaki do wait()
pcall(function()
local aa = game.Players.LocalPlayer.Character.HumanoidRootPart

if not aa:FindFirstChild("Haki") then
local args = {
    [1] = "BusoHaki"
}
game:GetService("ReplicatedStorage").Remotes.SkillHolder:FireServer(unpack(args))
wait()
local args = {
    [1] = "KenHaki"
}
game:GetService("ReplicatedStorage").Remotes.SkillHolder:FireServer(unpack(args))
end
end)
end

	end    
})

