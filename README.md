-- PYyDz Hub V2

local player = game.Players.LocalPlayer

-- GUI
local gui = Instance.new("ScreenGui")
gui.Name = "pyydzHub"
gui.Parent = game.CoreGui

local main = Instance.new("Frame", gui)
main.Size = UDim2.new(0,450,0,300)
main.Position = UDim2.new(0.35,0,0.3,0)
main.BackgroundColor3 = Color3.fromRGB(25,25,25)
main.Active = true
main.Draggable = true

-- Title
local title = Instance.new("TextLabel", main)
title.Size = UDim2.new(1,0,0,40)
title.Text = "PYyDz HUB V2"
title.TextColor3 = Color3.new(1,1,1)
title.BackgroundTransparency = 1
title.TextScaled = true

-- Tab buttons
local tabs = {"Quest","Item","Fruit","Raid","Hop","Misc"}
local pages = {}

for i,name in pairs(tabs) do

    local btn = Instance.new("TextButton", main)
        btn.Size = UDim2.new(0,70,0,30)
            btn.Position = UDim2.new(0,(i-1)*70,0,45)
                btn.Text = name
                    btn.BackgroundColor3 = Color3.fromRGB(40,40,40)
                        btn.TextColor3 = Color3.new(1,1,1)

                            local page = Instance.new("Frame", main)
                                page.Size = UDim2.new(1,0,0,200)
                                    page.Position = UDim2.new(0,0,0,90)
                                        page.BackgroundTransparency = 1
                                            page.Visible = false

                                                pages[name] = page

                                                    btn.MouseButton1Click:Connect(function()

                                                            for _,v in pairs(pages) do
                                                                        v.Visible = false
                                                                                end

                                                                                        page.Visible = true

                                                                                            end)

                                                                                            end

                                                                                            -- Example content
                                                                                            local label = Instance.new("TextLabel", pages["Quest"])
                                                                                            label.Size = UDim2.new(1,0,0,50)
                                                                                            label.Text = "Quest Functions Here"
                                                                                            label.TextColor3 = Color3.new(1,1,1)
                                                                                            label.BackgroundTransparency = 1
                                                                                            label.TextScaled = true