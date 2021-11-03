local CoastingLibrary = loadstring(game:HttpGet("https://pastebin.com/raw/3gQQtaKX"))()

local AimbotTab = CoastingLibrary:CreateTab("Main")
local MainSection = AimbotTab:CreateSection("Main")
local ConfigSection = AimbotTab:CreateSection("Config")

MainSection:CreateButton("Click Me!", function()
   print("Boo!")
end)

MainSection:CreateLabel("Namey", "Auto farm")

MainSection:CreateToggle("Fastattack", function(value)
   _G.FastAttk = value
local RigC = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework) 
	local VirtualUser = game:GetService('VirtualUser')
				kkii = require(game.ReplicatedStorage.Util.CameraShaker)
				spawn(function()
					game:GetService('RunService').Heartbeat:connect(function()
						if _G.FastAttk then
							pcall(function()
								pcall(function ()
										kkii:Stop()
								end)  
							end)
						end
					end)
				end)
				---------------------------------
				spawn(function()
					game:GetService('RunService').Heartbeat:connect(function()
						if _G.FastAttk then
							pcall(function()
								pcall(function ()
										RigC.activeController.timeToNextAttack = 0
								end)  
							end)
						end
					end)
				end)

				spawn(function()
					game:GetService('RunService').Heartbeat:connect(function()
						if _G.FastAttk then
							pcall(function()
								pcall(function ()
										RigC.activeController.hitboxMagnitude = 25
									wait(.05)
								end)  
							end)
						end
					end)
				end)

				spawn(function()
					game:GetService('RunService').Heartbeat:connect(function()
						if _G.FastAttk then
							pcall(function()
								pcall(function ()
										
										RigC.activeController.increment = 3
								end)
							end)
						end
					end)
				end)

				spawn(function()
					game:GetService('RunService').Heartbeat:connect(function()
						if _G.FastAttk then
							pcall(function()
								pcall(function ()
									game:GetService'VirtualUser':CaptureController()
									game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
									wait(.05)
								end)
							end)
						end
					end)
				end)
				spawn(function()
					game:GetService('RunService').Heartbeat:connect(function()
						if _G.FastAttk then
							pcall(function()
								pcall(function ()
									game:GetService'VirtualUser':CaptureController()
									game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
									wait(.05)
								end)
							end)
						end
					end)
				end)
end)

MainSection:CreateToggle("Auto Yama", function(boolean)
   _G.YamaHop = false
spawn(function()
			while wait() do
				pcall(function()
					if _G.YamaHop then
						if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter","Progress") >= 30 then
							fireclickdetector(game:GetService("Workspace").Map.Waterfall.SealedKatana.Handle.ClickDetector)
						else
							if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-5418.892578125, 313.74130249023, -2826.2260742188)
								wait(.9)
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter")
							else
								if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat  Diablo (0/1)" then
									if game:GetService("Workspace").Enemies:FindFirstChild("Diablo [Lv. 1750]") then
										for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
											if v.Name == "Diablo [Lv. 1750]" then
												repeat wait()
													if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
													end
													EquipWeapon(_G.SelectWeapon)
													game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(1,10,1)
													sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
													v.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
													v.HumanoidRootPart.CanCollide = false
													v.HumanoidRootPart.Size = Vector3.new(50,50,50)
													v.Humanoid:ChangeState(11)
                                                    _G.FastBoss = true
												until _G.YamaHop == false or v.Humanoid.Health <= 0
												_G.FastBoss = false
											end
										end
									else
										spawn(function()
											game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("ReplicatedStorage")["Diablo [Lv. 1750]"].HumanoidRootPart.CFrame *CFrame.new(0,0,15)
										end)
									end
								elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat  Deandre (0/1)" then
									if game:GetService("Workspace").Enemies:FindFirstChild("Deandre [Lv. 1750]") then
										for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
											if v.Name == "Deandre [Lv. 1750]" then
												repeat wait()
													if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
													end
													EquipWeapon(_G.SelectWeapon)
													game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(1,10,1)
													sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
													v.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
													v.HumanoidRootPart.CanCollide = false
													v.HumanoidRootPart.Size = Vector3.new(50,50,50)
													v.Humanoid:ChangeState(11)
                                                    _G.FastBoss = true
												until _G.YamaHop == false or v.Humanoid.Health <= 0
												_G.FastBoss = false
											end
										end
									else
										spawn(function()
											game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("ReplicatedStorage")["Deandre [Lv. 1750]"].HumanoidRootPart.CFrame *CFrame.new(0,0,15)
										end)
									end
								elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text == "Defeat  Urban (0/1)" then
									if game:GetService("Workspace").Enemies:FindFirstChild("Urban [Lv. 1750]") then
										for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
											if v.Name == "Urban [Lv. 1750]" then
												repeat wait()
													if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
													end
													EquipWeapon(_G.SelectWeapon)
													game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(1,10,1)
													sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
													v.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
													v.HumanoidRootPart.CanCollide = false
													v.HumanoidRootPart.Size = Vector3.new(50,50,50)
													v.Humanoid:ChangeState(11)
                                                    _G.FastBoss = true
												until _G.YamaHop == false or v.Humanoid.Health <= 0
												_G.FastBoss = false
											end
										end
									else
										spawn(function()
											game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("ReplicatedStorage")["Urban [Lv. 1750]"].HumanoidRootPart.CFrame *CFrame.new(0,0,15)
										end)
									end
								end
							end
						end
					end
				end)
			end
		end)
		
    spawn(function()
		while wait() do
			if _G.YamaHop then
				pcall(function()
					if game:GetService("Workspace").Enemies:FindFirstChild("Diablo [Lv. 1750]") or game:GetService("Workspace").Enemies:FindFirstChild("Deandre [Lv. 1750]") or game:GetService("Workspace").Enemies:FindFirstChild("Urban [Lv. 1750]") then
					else
						wait(12)
						if not game:GetService("Workspace").Enemies:FindFirstChild("Diablo [Lv. 1750]") or game:GetService("Workspace").Enemies:FindFirstChild("Deandre [Lv. 1750]") or game:GetService("Workspace").Enemies:FindFirstChild("Urban [Lv. 1750]") then
							local PlaceID = game.PlaceId
							local AllIDs = {}
							local foundAnything = ""
							local actualHour = os.date("!*t").hour
							local Deleted = false
							function TPReturner()
								local Site;
								if foundAnything == "" then
									Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
								else
									Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
								end
								local ID = ""
								if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
									foundAnything = Site.nextPageCursor
								end
								local num = 0;
								for i,v in pairs(Site.data) do
									local Possible = true
									ID = tostring(v.id)
									if tonumber(v.maxPlayers) > tonumber(v.playing) then
										for _,Existing in pairs(AllIDs) do
											if num ~= 0 then
												if ID == tostring(Existing) then
													Possible = false
												end
											else
												if tonumber(actualHour) ~= tonumber(Existing) then
													local delFile = pcall(function()
														-- delfile("NotSameServers.json")
														AllIDs = {}
														table.insert(AllIDs, actualHour)
													end)
												end
											end
											num = num + 1
										end
										if Possible == true then
											table.insert(AllIDs, ID)
											wait()
											pcall(function()
												-- writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
												wait()
												game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
											end)
											wait(4)
										end
									end
								end
							end
							function Teleport() 
								while wait() do
									pcall(function()
										TPReturner()
										if foundAnything ~= "" then
											TPReturner()
										end
									end)
								end
							end
							Teleport()
						end
					end
				end) 
			end
		end
	end)
end)

MainSection:CreateToggle("Auto Electro v.2", function(boolean)
   _G.Electro = false
	spawn(function()
		while wait() do wait()
			if _G.Electro then
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") or game.Players.LocalPlayer.Character:FindFirstChild("Electro") or game.Players.LocalPlayer.Backpack:FindFirstChild("Electric Claw") or game.Players.LocalPlayer.Character:FindFirstChild("Electric Claw") then
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 400 then
						local args = {
							[1] = "BuyElectricClaw"
						}
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						_G.SelectWeapon = "Electric Claw"
					end  
					if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 400 then
						local args = {
							[1] = "BuyElectricClaw"
						}
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))

						_G.SelectWeapon = "Electric Claw"
					end  
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value <= 399 then
						_G.SelectWeapon = "Electro"
					end 
				else 
					local args = {
						[1] = "BuyElectro"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end
			end
		end
	end)
	spawn(function()
		while wait() do
			pcall(function()
				if _G.Electro then
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") or game.Players.LocalPlayer.Character:FindFirstChild("Electro") then
						if (game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 400) or (game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 400) then
							if _G.AutoFarm == false then
								wait(1.1)
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-10371.4717, 330.764496, -10131.4199, -0.804111481, 0, -0.594478488, 0, 1, 0, 0.594478488, 0, -0.804111481)
								local args = {
									[1] = "BuyElectricClaw",
									[2] = "Start"
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
								wait(2)
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12550.532226563, 336.22631835938, -7510.4233398438)
								wait(1)
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-10371.4717, 330.764496, -10131.4199, -0.804111481, 0, -0.594478488, 0, 1, 0, 0.594478488, 0, -0.804111481)
								local args = {
									[1] = "BuyElectricClaw"
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
							elseif _G.AutoFarm == true then
								_G.AutoFarm = false
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-10371.4717, 330.764496, -10131.4199, -0.804111481, 0, -0.594478488, 0, 1, 0, 0.594478488, 0, -0.804111481)
								local args = {
									[1] = "BuyElectricClaw",
									[2] = "Start"
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
								wait(2)
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-12550.532226563, 336.22631835938, -7510.4233398438)
								wait(1)
								game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-10371.4717, 330.764496, -10131.4199, -0.804111481, 0, -0.594478488, 0, 1, 0, 0.594478488, 0, -0.804111481)
								local args = {
									[1] = "BuyElectricClaw"
								}
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
								_G.SelectWeapon = "Electric Claw"
								wait(.1)
								_G.AutoFarm = true
							end
						end
					end
				end
			end)
		end
	end)
end)

MainSection:CreateSlider("Field Of View", 0, 150, 50, false, function(value)
   print("Field of View: " .. value)
end)

ConfigSection:CreateColorPicker("Field of View Color", Color3.fromRGB(255, 255, 255), function(color)
   print("Field Of View Color:", color)
end)

ConfigSection:CreateDropdown("Type", {"Mouse", "Character"}, 1, function(option)
   print("Type: " .. option)
end)

ConfigSection:CreateKeybind("remove lava", Enum.KeyCode.Unknown, false, true, function(boolean)
   for i,v in pairs(game.Workspace:GetDescendants()) do
				if v.Name == "Lava" then   
					v:Destroy()
				end
			end
			for i,v in pairs(game.ReplicatedStorage:GetDescendants()) do
				if v.Name == "Lava" then   
					v:Destroy()
				end
			end
end)
