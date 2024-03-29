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

function TP(CFrame)
    pcall(function()
        game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").CFrame = CFrame
    end)
end

No()
local redzlib = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/RedzLibV5/main/Source.Lua"))()

local Window = redzlib:MakeWindow({
  Title = "Siron Hub : Second piece",
  SubTitle = "Dev : Siron Hub",
  SaveFolder = "testando | redz lib v5.lua"
})

local Tab1 = Window:MakeTab({"Settings", "swords"}) -- ok
local Tab3 = Window:MakeTab({"Auto Farm Raid", "swords"}) --ok
local Tab2 = Window:MakeTab({"Auto Farm", "swords"}) -- ok
local Tab4 = Window:MakeTab({"Up Stats", "swords"}) -- ok
local Tab6 = Window:MakeTab({"Players", "swords"}) -- ok
local Tab7 = Window:MakeTab({"Random Fruit","swords"})
local Tab5 = Window:MakeTab({"Teleport", "swords"}) -- ok


local Section1 = Tab1:AddSection({"Boots FPS"})
Tab1:AddButton({"Boots FPS",function()
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

local Se2 = Tab1:AddSection({"Function skill"})
local Toggle = Tab1:AddToggle({
  Name = "Z",
  Default = false,
  Callback = function(po)
  _G.hr = po
  while _G.hr do wait ()
  game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
  end
  end
})
local Toggle = Tab1:AddToggle({
  Name = "X",
  Default = false,
  Callback = function(ho)
  _G.t = ho
  while _G.t do wait()
  game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
  end
  end
})
local Toggle = Tab1:AddToggle({
  Name = "C",
  Default = false,
  Callback = function(fo)
  _G.mk = fo
  while _G.t do wait()
  game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)
  end
  end
})
local Toggle = Tab1:AddToggle({
  Name = "V",
  Default = false,
  Callback = function(mo)
  _G.uim = mo
  while _G.uim do wait()
  game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
  end
  end
})
local Seos = Tab1:AddSection({"Haki"})
local Toggle2 = Tab1:AddToggle({
  Name = "Auto Haki",
  Default = false,
  Callback = function(dd)
  _G.AutoHaki = Haki
while _G.AutoHaki do wait()
pcall(function()
local aa = game.Players.LocalPlayer.Character.HumanoidRootPart

if not aa:FindFirstChild("Haki") then
local args = {
    [1] = "BusoHaki"
}
game:GetService("ReplicatedStorage").Remotes.SkillHolder:FireServer(unpack(args))
end
end)
end
  end
})
local Seos = Tab1:AddSection({"Chest"})
local Toggle2 = Tab1:AddToggle({
  Name = "Auto Chest",
  Default = false,
  Callback = function(dd)
  _G.Fdd = dd
    while _G.Fdd do 
        wait()
        for i,v in pairs(game:GetService("Workspace").Chests:GetDescendants()) do
            if v.ClassName == "ProximityPrompt" then
                fireproximityprompt(v,30)
            end
        end
    end
  end
})
local Toggle2 = Tab1:AddToggle({
  Name = "Auto Chest TP",
  Default = false,
  Callback = function(d)
  _G.Fd = d
    while _G.Fd do 
        wait()
        for i,v in pairs(game:GetService("Workspace").Chests:GetDescendants()) do
            if v.ClassName == "ProximityPrompt" then
                fireproximityprompt(v,30)
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame
            end
        end
    end
  end
})

local Se2 = Tab3:AddSection({"Raid"})
Tab3:AddSlider({
  Name = "Distance",
  Min = 1,
  Max = 50,
  Increase = 1,
  Default = 5,
  Callback = function(joo)
    _G.Di = joo
  end
})

Tab3:AddButton({"Teleprot to Portal",function()
for i,v in pairs(game:GetService("Workspace").World.Portal:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
game.Players.LocalPlayer.Character.HumanoidRootPart .CFrame = v.Parent.CFrame
wait(0.1)
fireproximityprompt(v,30)
end
      end
   end
})
local Toggle2 = Tab3:AddToggle({
  Name = "Auto Raid",
  Default = false,
  Callback = function(aii)
  _G.Raid = aii
  end
})

spawn(function()
    while wait() do 
        pcall(function()
            if _G.Raid then
                for _,v in pairs(game:GetService("Workspace").Lives:GetDescendants()) do
                    if v.ClassName == "Model" and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health >= 1 then
                        local player = game:GetService("Players"):GetPlayerFromCharacter(v)
                        if not player then
                            repeat 
                                wait()
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,0,_G.Di)
                            until _G.Raid == false or v.Humanoid.Health <= 0
                        end
                    end
                end
            end
        end)
    end
end)

local Section = Tab2:AddSection({"Weapon"})


-- local Paragraph = Tab2:AddParagraph({"Paragraph", "This is a Paragraph\nSecond Line"})
local Weaponlist = {}
local Weapon = nil
for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
    table.insert(Weaponlist,v.Name)
    end

local Dropdown = Tab2:AddDropdown({
  Name = "Select Weapon",
  Description = "เลือกอาวุธที่ต้องการใช้",
  Options = Weaponlist,
  Default = nil,
  Flag = "...",
  Callback = function(vu)
    _G.Weapon = vu
  end
})

local Toggle2 = Tab2:AddToggle({
  Name = "Auto Equip",
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


local Attacking = false
local AutoAttackToggle = false
local Toggle2 = Tab2:AddToggle({
  Name = "Auto Attack [ Fix Bug ]",
  Default = false,
  Callback = function(autoattack)
  Attacking = autoattack
        AutoAttackToggle = autoattack
  end
})
local function PerformAutoAttack()
    while true do
        if AutoAttackToggle and Attacking then
            game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 672))
            wait(0.3)
        end
        wait(0.1)
    end
end

spawn(PerformAutoAttack)

local function HandleCharacterAdded()
    game.Players.LocalPlayer.CharacterAdded:Connect(function()
        Attacking = false
    end)
end

local function HandleCharacterRemoving()
    game.Players.LocalPlayer.CharacterRemoving:Connect(function()
        Attacking = false
    end)
end

HandleCharacterAdded()
HandleCharacterRemoving()

spawn(function()
    while true do
        if game.Players.LocalPlayer.Character then
            local humanoid = game.Players.LocalPlayer.Character:FindFirstChild("Humanoid")
            if humanoid then
                if humanoid.Health <= 0 then
                    Attacking = false
                elseif humanoid.Health > 0 then
                    wait(1.5)
                    Attacking = true
                end
            end
        end
        wait(0.1)
    end
end)

game.Players.LocalPlayer.CharacterAdded:Connect(function(character)
    if Attacking then
        toggleAutoAttack(true)
    end
end)
local Section = Tab2:AddSection({"Auto Farm Quest"})
Quest = {}
for i,v in pairs(workspace.Quest:GetDescendants()) do
    if v.Name == "Quest" then
        table.insert(Quest,v.Value)
    end
end
local Dropdown = Tab2:AddDropdown({
  Name = "Select Quest",
  Description = "เลือกเควสที่ต้องการจะฟาม",
  Options = Quest,
  Default = nil,
  Flag = "...",
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
local Toggle = Tab2:AddToggle({
  Name = "Auto Farm Quest",
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

local Section = Tab2:AddSection({"Auto Farm All"})
local Toggle = Tab2:AddToggle({
  Name = "Auto Farm Gem",
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
                            TP(v.HumanoidRootPart.CFrame * CFrame.new(0,0,5))
                        until _G.eam == false or v.Humanoid.Health <= 0
                    end
                end
            end
        end)
    end
end)

  end
})

local Toggle = Tab2:AddToggle({
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
local MonNamess = {
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
                    if table.find(MonNamess, v.Name) and v:FindFirstChild('HumanoidRootPart') and v.Humanoid.Health >= 1 then
                        repeat
                        CA()
                           wait()   
                            TP(v.HumanoidRootPart.CFrame * CFrame.new(0,0,5))
                        until _G.eami == false or v.Humanoid.Health <= 0
                    end
                end
            end
        end)
    end
end)
  end
})



Window:SelectTab(Tab4)
local Section1 = Tab4:AddSection({"Stats"})

local Toggle2 = Tab4:AddToggle({
  Name = "Melee",
  Default = false,
  Callback = function(ii)
  _G.iii = ii
while _G.iii do wait() 
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
local Toggle2 = Tab4:AddToggle({
  Name = "Weapon",
  Default = false,
  Callback = function(ooo)
  _G.oo = ooo
while _G.oo do wait() 
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
local Toggle2 = Tab4:AddToggle({
  Name = "Defense",
  Default = false,
  Callback = function(kk)
  _G.kkk = kk
while _G.kkk do wait() 
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
local Toggle2 = Tab4:AddToggle({
  Name = "Demon Fruit",
  Default = false,
  Callback = function(xxx)
  _G.xx = xxx
while _G.xx do wait() 
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


Window:SelectTab(Tab5)
local Section1 = Tab5:AddSection({"Teleport island"})
map = {}
for i ,v in pairs(game:GetService("Workspace").Locations:GetChildren()) do
table.insert(map,v.Name)
end
local Dropdown = Tab5:AddDropdown({
  Name = "Select island",
  Description = "เลือกเกาะที่ต้องการจะวาปไป",
  Options = map,
  Default = nil,
  Flag = "...",
  Callback = function(mp)
    map = mp
  end
}) 

Tab5:AddButton({"TP island",function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Locations[map].CFrame * CFrame.new(0,-100,0)
	end
})
    shop = {}
for i ,v in pairs(game:GetService("Workspace").Shop:GetChildren()) do
table.insert(shop,v.Name)
end
local Section1 = Tab5:AddSection({"Teleport Shop"})

local Dropdown = Tab5:AddDropdown({
  Name = "Select Shop",
  Description = "เลือกร้านค้าที่ต้องการจะวาปไป",
  Options = shop,
  Default = nil,
  Flag = "...",
  Callback = function(hp)
    shop = hp
  end
}) 

Tab5:AddButton({"TP Shop",function()
for i,v in pairs(game:GetService("Workspace").Shop[shop]:GetDescendants()) do
if v.ClassName == "ProximityPrompt" then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,5,0)
end
      end
	end
})

Window:SelectTab(Tab6)
local Section1 = Tab6:AddSection({"Players"})
Plr = {}
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name)
end
local Dropdown = Tab6:AddDropdown({
  Name = "Select Players",
  Description = "เลือกผู้เล่นที่ต้องการจะวาปไป",
  Options = Plr,
  Default = nil,
  Flag = "...",
  Callback = function(t)
    PlayerTP = t
  end
}) 

Tab6:AddButton({"Teleport To Players",function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
	end
})

local hee = Tab6:AddToggle({
	Name = "Loop Teleport To Players Select",
	Default = false,
	Callback = function(tp)
	_G.hre = tp
while _G.hre do wait()
      			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame * CFrame.new(0,0,3)
end
	end    
})

Window:SelectTab(Tab7)
local Section1 = Tab7:AddSection({"Random fruit"})
local Fruit = {
    "Gem",
    "Beli"
}
local Dropdown = Tab6:AddDropdown({
  Name = "Select Random",
  Description = "เลือกว่าจะสุ่มผลด้วยการใช้อะไร",
  Options = Fruit,
  Default = nil,
  Flag = "...",
  Callback = function(selectedFruit)
    _G.FT = selectedFruit 
  end
}) 

local hee = Tab7:AddToggle({
	Name = "Random Fruit",
	Default = false,
	Callback = function(randomFruit)
	_G.Random = randomFruit
   while _G.Random do
        wait()
      			        for i, v in pairs(game:GetService("Workspace").Shop:GetDescendants()) do
            if v.ClassName == "ProximityPrompt" then
                if _G.FT == "Beli" then
                    fireproximityprompt(v, 30)
                elseif _G.FT == "Gem" then
                    fireproximityprompt(v, 30)game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-589.146118, 36.5146637, -1950.28296, 0.0316599086, 1.00091079e-07, -0.999498725, -2.31954509e-08, 1, 9.94065417e-08, 0.999498725, 2.00366213e-08, 0.0316599086)
                end
            end
        end
    end
	end    
})

Tab99:AddDiscordInvite({
  Name = "Siron Hub",
  Logo = "rbxassetid://15793473802",
  Invite = "https://discord.gg/7aR7kNVt4g"
})


-- Simple example ;)
-- More in soon...
