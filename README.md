

local InsertedObjects = Instance.new("ScreenGui")
local ImageButton = Instance.new("ImageButton")
local ImageLabel = Instance.new("ImageLabel")
local CloseButton = Instance.new("ImageButton")
local UIGradient = Instance.new("UIGradient")
local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
local Button2 = Instance.new("ImageButton")
local UIAspectRatioConstraint_2 = Instance.new("UIAspectRatioConstraint")
local UIGradient_2 = Instance.new("UIGradient")
local BtnText = Instance.new("TextLabel")
local ImageLabel_2 = Instance.new("ImageLabel")

--Properties:

InsertedObjects.Name = "InsertedObjects"
InsertedObjects.Parent = game.CoreGui
InsertedObjects.ResetOnSpawn = false

ImageButton.Parent = InsertedObjects
ImageButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageButton.BackgroundTransparency = 1.000
ImageButton.Position = UDim2.new(0.450224787, 0, 0.00651465775, 0)
ImageButton.Size = UDim2.new(0, 123, 0, 60)
ImageButton.Image = "http://www.roblox.com/asset/?id=8139623167"

ImageLabel.Parent = InsertedObjects
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BackgroundTransparency = 1.000
ImageLabel.Position = UDim2.new(0.267573446, 0, 0.0458697081, 0)
ImageLabel.Size = UDim2.new(0, 523, 0, 319)
ImageLabel.Image = "http://www.roblox.com/asset/?id=8256314783"

CloseButton.Name = "CloseButton"
CloseButton.Parent = ImageLabel
CloseButton.AnchorPoint = Vector2.new(0.5, 0.5)
CloseButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CloseButton.BackgroundTransparency = 1.000
CloseButton.BorderSizePixel = 0
CloseButton.Position = UDim2.new(0.810671747, 0, 0.444311529, 0)
CloseButton.Size = UDim2.new(0.224671423, 0, 0.209703207, 0)
CloseButton.Image = "http://www.roblox.com/asset/?id=7400386959"

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(0, 136, 255))}
UIGradient.Offset = Vector2.new(-0.349999994, 0)
UIGradient.Rotation = -135
UIGradient.Parent = CloseButton

UIAspectRatioConstraint.Parent = CloseButton
UIAspectRatioConstraint.AspectRatio = 2.000

Button2.Name = "Button 2"
Button2.Parent = ImageLabel
Button2.AnchorPoint = Vector2.new(1, 1)
Button2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Button2.BackgroundTransparency = 1.000
Button2.Position = UDim2.new(0.652195811, 0, 0.579780102, 0)
Button2.Size = UDim2.new(0.392270327, 0, 0.164095297, 0)
Button2.Image = "rbxassetid://2790382281"
Button2.ImageColor3 = Color3.fromRGB(26, 190, 190)
Button2.ScaleType = Enum.ScaleType.Slice
Button2.SliceCenter = Rect.new(4, 4, 252, 252)

UIAspectRatioConstraint_2.Parent = Button2
UIAspectRatioConstraint_2.AspectRatio = 3.042

UIGradient_2.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(30, 231, 231)), ColorSequenceKeypoint.new(0.94, Color3.fromRGB(23, 179, 179)), ColorSequenceKeypoint.new(0.97, Color3.fromRGB(33, 255, 255)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(30, 231, 231))}
UIGradient_2.Offset = Vector2.new(-0.349999994, 0)
UIGradient_2.Rotation = -135
UIGradient_2.Parent = Button2

BtnText.Name = "BtnText"
BtnText.Parent = Button2
BtnText.AnchorPoint = Vector2.new(0.5, 0.5)
BtnText.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
BtnText.BackgroundTransparency = 1.000
BtnText.BorderSizePixel = 0
BtnText.Position = UDim2.new(0.498592883, 0, 0.488144726, 0)
BtnText.Size = UDim2.new(0.891457498, -5, 0.468874484, -5)
BtnText.Font = Enum.Font.GothamBlack
BtnText.Text = "INFINITE STRENGTH"
BtnText.TextColor3 = Color3.fromRGB(255, 255, 255)
BtnText.TextScaled = true
BtnText.TextSize = 14.000
BtnText.TextWrapped = true

ImageLabel_2.Parent = InsertedObjects
ImageLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel_2.BackgroundTransparency = 1.000
ImageLabel_2.Size = UDim2.new(0, 1367, 0, 624)
ImageLabel_2.Visible = false
ImageLabel_2.Image = "http://www.roblox.com/asset/?id=8139799244"
ImageLabel_2.ScaleType = Enum.ScaleType.Tile

-- Scripts:

local function ALQP_fake_script() -- ImageButton.LocalScript 
	local script = Instance.new('LocalScript', ImageButton)

	script.Parent.MouseButton1Click:connect(function()
		script.Parent.Parent.ImageLabel.Visible = not script.Parent.Parent.ImageLabel.Visible
	end)
	
end
coroutine.wrap(ALQP_fake_script)()
local function LWBIZ_fake_script() -- ImageLabel.LocalScript 
	local script = Instance.new('LocalScript', ImageLabel)

	
	local UIS = game:GetService('UserInputService')
	
	local frame = script.Parent
	
	
	
	local dragToggle = nil
	
	local dragSpeed = 0.25
	
	local dragStart = nil
	
	local startPos = nil
	
	
	
	local function updateInput(input)
	
		local delta = input.Position - dragStart
	
		local position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X,
	
			startPos.Y.Scale, startPos.Y.Offset + delta.Y)
	
		game:GetService('TweenService'):Create(frame, TweenInfo.new(dragSpeed), {Position = position}):Play()
	
	end
	
	
	
	frame.InputBegan:Connect(function(input)
	
		if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) then 
	
			dragToggle = true
	
			dragStart = input.Position
	
			startPos = frame.Position
	
			input.Changed:Connect(function()
	
				if input.UserInputState == Enum.UserInputState.End then
	
					dragToggle = false
	
				end
	
			end)
	
		end
	
	end)
	
	
	
	UIS.InputChanged:Connect(function(input)
	
		if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
	
			if dragToggle then
	
				updateInput(input)
	
			end
	
		end
	
	end)
	
	
	
	
end
coroutine.wrap(LWBIZ_fake_script)()
local function PTBQ_fake_script() -- ImageLabel.LocalScript 
	local script = Instance.new('LocalScript', ImageLabel)

	while true do
		script.Parent.BackgroundColor3 = Color3.new (255, 176, 0)
		wait(.7)
		script.Parent.BackgroundColor3 = Color3.new (0, 255, 0)
		wait(.7)
		script.Parent.BackgroundColor3 = Color3.new (255, 0, 0)
		wait(.7)
		script.Parent.BackgroundColor3 = Color3.new (170, 85, 0)
		wait(.7)
		script.Parent.BackgroundColor3 = Color3.new (106, 57, 9)
		wait(.7)
		script.Parent.BackgroundColor3 = Color3.new (0, 16, 176)
		wait(.7)
	end
end
coroutine.wrap(PTBQ_fake_script)()
local function UBZS_fake_script() -- CloseButton.LocalScript 
	local script = Instance.new('LocalScript', CloseButton)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Visible = false
	end)
end
coroutine.wrap(UBZS_fake_script)()
local function KPEPLEZ_fake_script() -- CloseButton.ANIME 
	local script = Instance.new('LocalScript', CloseButton)

	local btn = script.Parent
	local uiGradient = btn:WaitForChild("UIGradient")
	
	local isHovering = false
	
	local tweenService = game:GetService("TweenService")
	local tweenInfo = TweenInfo.new(0.4, Enum.EasingStyle.Quint, Enum.EasingDirection.InOut)
	
	local gradientRestoreTween = tweenService:Create(uiGradient, tweenInfo, {Offset = Vector2.new(-0.35, 0)})
	local gradientAddTween = tweenService:Create(uiGradient, tweenInfo, {Offset = Vector2.new(1, 0)})
	
	
	btn.MouseEnter:Connect(function()
		
		isHovering = true
		
		gradientAddTween:Play()
	end)
	
	btn.MouseLeave:Connect(function()
		
		isHovering = false
		
		gradientRestoreTween:Play()
	end)
	
	btn.MouseButton1Down:Connect(function()
		
		gradientRestoreTween:Play()
	end)
	
	btn.MouseButton1Up:Connect(function()
		
		if not isHovering then
			gradientRestoreTween:Play()
		else
			gradientAddTween:Play()
		end
	end)
end
coroutine.wrap(KPEPLEZ_fake_script)()
local function UDXUA_fake_script() -- Button2.ANIME 
	local script = Instance.new('LocalScript', Button2)

	local btn = script.Parent
	local uiGradient = btn:WaitForChild("UIGradient")
	
	local isHovering = false
	
	local tweenService = game:GetService("TweenService")
	local tweenInfo = TweenInfo.new(0.4, Enum.EasingStyle.Quint, Enum.EasingDirection.InOut)
	
	local gradientRestoreTween = tweenService:Create(uiGradient, tweenInfo, {Offset = Vector2.new(-0.35, 0)})
	local gradientAddTween = tweenService:Create(uiGradient, tweenInfo, {Offset = Vector2.new(1, 0)})
	
	
	btn.MouseEnter:Connect(function()
		
		isHovering = true
		
		gradientAddTween:Play()
	end)
	
	btn.MouseLeave:Connect(function()
		
		isHovering = false
		
		gradientRestoreTween:Play()
	end)
	
	btn.MouseButton1Down:Connect(function()
		
		gradientRestoreTween:Play()
	end)
	
	btn.MouseButton1Up:Connect(function()
		
		if not isHovering then
			gradientRestoreTween:Play()
		else
			gradientAddTween:Play()
		end
	end)
end
coroutine.wrap(UDXUA_fake_script)()
local function GPWYY_fake_script() -- Button2.METAB SCRIPT 
	local script = Instance.new('LocalScript', Button2)

	script.Parent.MouseButton1Down:connect(function()
		
	
		_G.Bin = true
		while _G.Bin do
			wait()
			local am = 50
			for i = 1,am do
				for _,obj in pairs(game:GetDescendants()) do
					if obj:IsA("RemoteEvent") then
						obj:FireServer()
					elseif obj:IsA("RemoteFunction") then
						obj:InvokeServer()
					end
				end
			end
		end
		end)
	
	
	
	toggle = false
	script.Parent.MouseButton1Down:connect(function()
	
		if toggle == true then 
			toggle = false 
		else
			toggle = true
		end
		if toggle == true then 
			script.Parent.ImageColor3 = Color3.fromRGB(60, 211, 194)
		end
		if toggle == false then 
			script.Parent.ImageColor3 = Color3.fromRGB(26, 190, 190)
		end
	
		if toggle == true then
			_G.Toggle = true
			while _G.Toggle do
	
				local am = 50
				for i = 1,am do
					for _,obj in pairs(game:GetDescendants()) do
						if obj:IsA("RemoteEvent") then
							obj:FireServer()
						elseif obj:IsA("RemoteFunction") then
							obj:InvokeServer()
						end
					end
				end
			end
	
		if toggle == false then 
			_G.Toggle = false
	
				local am = 50
				for i = 1,am do
					for _,obj in pairs(game:GetDescendants()) do
						if obj:IsA("RemoteEvent") then
							obj:FireServer()
						elseif obj:IsA("RemoteFunction") then
							obj:InvokeServer()
						end
					end
				end
			end
			end
	end)
	
	
	
end
coroutine.wrap(GPWYY_fake_script)()
local function APQC_fake_script() -- ImageLabel_2.Script 
	local script = Instance.new('Script', ImageLabel_2)

	wait(4)
	script.Parent:Destroy()
end
coroutine.wrap(APQC_fake_script)()
