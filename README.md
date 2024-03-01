-- Made BY Mr.Alegator







local screenGui = Instance.new("ScreenGui")



screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")







local frame = Instance.new("Frame")



frame.Size = UDim2.new(0, 200, 0, 100)



frame.Position = UDim2.new(0.5, -100, 0.5, -50)



frame.BackgroundColor3 = Color3.new(1, 1, 1)



frame.Parent = screenGui







local title = Instance.new("TextLabel")



title.Size = UDim2.new(1, 0, 0, 20)



title.Position = UDim2.new(0, 0, 0, -20)



title.Text = "SSS Hub Key VIP"



title.TextColor3 = Color3.new(1, 1, 1)



title.BackgroundColor3 = Color3.new(0, 0, 0)



title.Parent = frame







local dragging



local dragInput



local dragStart



local startPos







local function update(input)



    local delta = input.Position - dragStart



    frame.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)



end







title.InputBegan:Connect(function(input)



    if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then



        dragging = true



        dragStart = input.Position



        startPos = frame.Position







        input.Changed:Connect(function()



            if input.UserInputState == Enum.UserInputState.End then



                dragging = false



            end



        end)



    end



end)







title.InputChanged:Connect(function(input)



    if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then



        dragInput = input



    end



end)







title.InputEnded:Connect(function(input)



    if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then



        dragging = false



        dragInput = nil



    end



end)







game:GetService("UserInputService").InputChanged:Connect(function(input)



    if input == dragInput and dragging then



        update(input)



    end



end)







local KeySystem = Instance.new("TextBox")



KeySystem.Size = UDim2.new(1, 0, 0.5, 0)



KeySystem.Position = UDim2.new(0, 0, 0, 0)



KeySystem.Text = "Enter the Key"



KeySystem.TextColor3 = Color3.new(0, 0, 0)



KeySystem.BackgroundTransparency = 0.5



KeySystem.BackgroundColor3 = Color3.new(1, 1, 1)



KeySystem.TextWrapped = true



KeySystem.Parent = frame







local SubmitButton = Instance.new("TextButton")



SubmitButton.Size = UDim2.new(0.5, 0, 0.5, 0)



SubmitButton.Position = UDim2.new(0, 0, 0.5, 0)



SubmitButton.Text = "Submit"



SubmitButton.Parent = frame







local CloseButton = Instance.new("TextButton")



CloseButton.Size = UDim2.new(0, 20, 0, 20)



CloseButton.Position = UDim2.new(1, -20, 0, 0)



CloseButton.Text = "X"



CloseButton.TextColor3 = Color3.new(1, 1, 1)



CloseButton.BackgroundColor3 = Color3.new(1, 0, 0)



CloseButton.Parent = frame







CloseButton.MouseButton1Click:Connect(function()



    screenGui:Destroy()



end)







local GetKeyButton = Instance.new("TextButton")



GetKeyButton.Size = UDim2.new(0.5, 0, 0.5, 0)



GetKeyButton.Position = UDim2.new(0.5, 0, 0.5, 0)



GetKeyButton.Text = "Get Key"



GetKeyButton.Parent = frame



--------------------------------------------------------------------------



SubmitButton.MouseButton1Click:Connect(function()



    local KeySystem = KeySystem.Text



    if KeySystem == "ip" then



screenGui:Destroy()











local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/LPO081/Ui-or/main/README.md')))()







local Window = OrionLib:MakeWindow({







		Name = "[ VIP ] SSS HUB [Shadow] Second Piece",







		HidePremium = false,







		SaveConfig = true,







		ConfigFolder = "OrionTest",







        IntroText = "BY NOOB-SCRIPT V2"       







}) 























local Tab = Window:MakeTab({







	Name = "Main",







	Icon = "rbxassetid://7733765398",







	PremiumOnly = false







})































local Section = Tab:AddSection({







	Name = "TP"







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







	Name = "Auto Chests",







	Default = false,







	Callback = function(d)







_G.Fd = d







while _G.Fd do wait()







for i,v in pairs(game:GetService("Workspace").Chests:GetDescendants()) do

if v.ClassName == "ProximityPrompt" then

fireproximityprompt(v,30)



end

      end







            end







	end    







})















local Section = Tab:AddSection({







	Name = " "







}) 









Tab:AddButton({







	Name = "Go to Traveling merchant",







	Callback = function()



for i,v in pairs(game:GetService("Workspace").NPC["Traveling merchant"]:GetDescendants()) do

if v.ClassName == "ProximityPrompt" then

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,3,0)

wait(.1)

fireproximityprompt(v,30)

end

      end





  	end    







})



local Section = Tab:AddSection({







	Name = " "







}) 









Tab:AddToggle({







	Name = "Auto skill Z",







	Default = false,







	Callback = function(mb)







_G.x = mb







while _G.x do wait()















game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)















end















	end    







})























Tab:AddToggle({







	Name = "Auto skill X",







	Default = false,







	Callback = function(mbz)







_G.xz = mbz







while _G.xz do wait()















game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)















end















	end    







})































Tab:AddToggle({







	Name = "Auto skill C",







	Default = false,







	Callback = function(mkln)







_G.xa = mkln







while _G.xa do wait()















game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)















end















	end    







})















Tab:AddToggle({







	Name = "Auto skill V",







	Default = false,







	Callback = function(m)







_G.x = m







while _G.x do wait()















game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)















end















	end    







})















local Section = Tab:AddSection({







	Name = "Auto Random fruit"







}) 















Tab:AddToggle({







	Name = "Auto Random fruit Beli",







	Default = false,







	Callback = function(gm)







_G.xm = gm







while _G.xm do wait()







for i,v in pairs(game:GetService("Workspace").Shop:GetDescendants()) do







if v.ClassName == "ProximityPrompt" then







fireproximityprompt(v,30)







game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(790.203735, 35.5073013, 1201.40369, 0.026754817, -8.37544611e-09, 0.999642015, 1.24128064e-07, 1, 5.05623188e-09, -0.999642015, 1.23948354e-07, 0.026754817)







end







end







end















	end    







})























Tab:AddToggle({







	Name = "Auto Random fruit Gem",







	Default = false,







	Callback = function(qm)







_G.gg = qm







while _G.gg do wait()







for i,v in pairs(game:GetService("Workspace").Shop:GetDescendants()) do







if v.ClassName == "ProximityPrompt" then







fireproximityprompt(v,30)







game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-741.048889, 43.4787788, -1933.82019, -0.0251465552, 7.8026531e-08, 0.999683797, -1.09866749e-09, 1, -7.80788483e-08, -0.999683797, -3.06173398e-09, -0.0251465552)







end







end







end















	end    







})























local Tab = Window:MakeTab({







	Name = "Auto Quest",







	Icon = "rbxassetid://7733765398",







	PremiumOnly = false







})























local Section = Tab:AddSection({







	Name = "Equip tools"







}) 































local Weaponlist = {}







local Weapon = nil















for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do







    table.insert(Weaponlist,v.Name)







end















Tab:AddDropdown({







	Name = "Weapon",







	Default = "",







	Options = Weaponlist,







	Callback = function(currentOption)







		Weapon = currentOption







	end    







})































Tab:AddToggle({







	Name = "Auto Equip",







	Default = false,







	Callback = function(a)







AutoEquiped = a







	end    







})















spawn(function()







while wait() do







if AutoEquiped then







pcall(function()







game.Players.LocalPlayer.Character.Humanoid:EquipTool(game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(Weapon))







end)







end







end







end)































local Section = Tab:AddSection({







	Name = "Auto Quest"







}) 























Tab:AddToggle({







	Name = "Auto Quest",







	Default = false,







	Callback = function(ab)







_G.hr = ab







while _G.hr do wait()







for i,v in pairs(game:GetService("Workspace").Quest:GetDescendants()) do







 if v.ClassName == "ProximityPrompt" then







   fireproximityprompt(v,30)







end







      end







            end







	end    







})















local Tab = Window:MakeTab({







	Name = "Tp map",







	Icon = "rbxassetid://7733765398",







	PremiumOnly = false







})























local Section = Tab:AddSection({







	Name = "Buy Item"







}) 











shop = {}

for i ,v in pairs(game:GetService("Workspace").Shop:GetChildren()) do

table.insert(shop,v.Name)

end





Tab:AddDropdown({

	Name = "TP Shop",

	Default = "Shop",

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



local Section = Tab:AddSection({







	Name = " "







}) 



local Section = Tab:AddSection({







	Name = "Island"







}) 





map = {}

for i ,v in pairs(game:GetService("Workspace").Locations:GetChildren()) do

table.insert(map,v.Name)

end





Tab:AddDropdown({

	Name = "TP Island",

	Default = "map",

	Options = map,

	Callback = function(mt)

	map = mt

	end    

})





Tab:AddButton({

	Name = "TP Island",

	Callback = function()



game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.workspace.Locations[map].CFrame * CFrame.new(0,-420,0)



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





local Tab = Window:MakeTab({







	Name = "Player TP",







	Icon = "rbxassetid://7733765398",







	PremiumOnly = false







})















local Section = Tab:AddSection({







	Name = "Player"







}) 























Plr = {}







for i,v in pairs(game:GetService("Players"):GetChildren()) do







    table.insert(Plr,v.Name) 







end















Tab:AddDropdown({







	Name = "Player",







	Default = "",







	Options = Plr,







	Callback = function(t)







		PlayerTP = t







	end    







})







































Tab:AddButton({







	Name = "Teleport",







	Callback = function()







      			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame















  	end    







})























Tab:AddToggle({







	Name = "Loop Teleport Player",







	Default = false,







	Callback = function(t)







_G.TPPlayer = t







while _G.TPPlayer do wait()







game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame * CFrame.new(0,0,3)







end















	end    







})







         















local Tabe = Window:MakeTab({







	Name = "VIP",







	Icon = "rbxassetid://7733765398",







	PremiumOnly = false







})

















local Section = Tabe:AddSection({



	Name = "Auto Farm"



}) 











          do



          local P = game:GetService("Workspace"):FindFirstChild("Noclip")



          if NM then



          NM:Destroy()



          end



    end



local Noclip = Instance.new("Part",workspace)



          Noclip.Name = "Noclip"



          Noclip.CanCollide = true



          Noclip.Anchored = true



          Noclip.Transparency = 0



          Noclip.Size = Vector3.new(30,1,30)



          



function Nom()



game:GetService("Workspace"):FindFirstChild("Noclip").CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,-3.5,0)



end



function CA()

for i,v in pairs(game:GetService("Workspace").Chests:GetDescendants()) do

if v.ClassName == "ProximityPrompt" then

fireproximityprompt(v,30)



end

      end

      		end



  

  





function No()

for i, v in ipairs(workspace.Lives:GetChildren()) do

    if not game:GetService("Players"):GetPlayerFromCharacter(v) then -- if not player then

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



Tabe:AddToggle({







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





local Section = Tabe:AddSection({



	Name = "Auto Farm Boss"



}) 





Tabe:AddToggle({

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
                    'Gilgamesh'
		    

                }



                for _, v in pairs(game:GetService('Workspace').Lives:GetDescendants()) do

                    if table.find(MonNames, v.Name) and v:FindFirstChild('HumanoidRootPart') and v.Humanoid.Health >= 1 then

                        repeat

                        CA()

                            wait()   

                            v.HumanoidRootPart.Size = Vector3.new(10, 10, 10)

                            v.HumanoidRootPart.Transparency = 0.9

                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =

                                v.HumanoidRootPart.CFrame * CFrame.new(0, 0, 7)

                        until _G.eami == false or v.Humanoid.Health <= 0

                    end

                end

            end

        end)

    end

end)



	end   

})







local Section = Tabe:AddSection({



	Name = "Auto Farm Gem"



}) 



Tabe:AddToggle({

    Name = "Auto Farm Gem V2",

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

                    'Shadow',

                    'Gojo',

                    'Kashimo',

                    'Sukuna',

                    'Snow Bandit Leader',

                    'Shank',

                    'Monkey King',

                    'Sand Man',

                    'Bomb Man',

                    'Bandit Leader',

                    'Artoria',

                    'Uraume',

		            'Gojo [Unleashed]',

                    'Sukuna [Half Power]',

		            'Rimuru',

                    'Killua',

                    'Ichigo',
                    'Choso',
		    'Natsu',
                    'Gilgamesh'
		    

                }



                for _, v in pairs(game:GetService('Workspace').Lives:GetDescendants()) do

                    if table.find(MonNames, v.Name) and v:FindFirstChild('HumanoidRootPart') and v.Humanoid.Health >= 1 then

                        repeat

                        CA()

                            wait()   

                            v.HumanoidRootPart.Size = Vector3.new(10, 10, 10)

                            v.HumanoidRootPart.Transparency = 0.9

                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =

                                v.HumanoidRootPart.CFrame * CFrame.new(0, 0, 7)

                        until _G.eam == false or v.Humanoid.Health <= 0

                    end

                end

            end

        end)

    end

end)



	end   

})





local Taba = Window:MakeTab({



	Name = "boost fps",

	Icon = "rbxassetid://7733765398",

	PremiumOnly = false



})



Taba:AddButton({

	Name = "boost fps",

	Callback = function()

-- boost

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





Taba:AddButton({

	Name = "Delete skilk",

	Callback = function()

	    game:GetService("Workspace").Effects:Destroy()

game:GetService("Workspace").SkillsObject:Destroy()

  	end    



})



Taba:AddToggle({



	Name = "White Screen",

	Default = false,

	Callback = function(boosy)

_G.WhiteScreen = boosy

while _G.WhiteScreen do wait()

        game:GetService("RunService"):Set3dRenderingEnabled()

        pairs("White")

       end

	end    

})











OrionLib:Init()













  



  end



end)







GetKeyButton.MouseButton1Click:Connect(function()



 setclipboard(" ") 



end) 




