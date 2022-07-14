	if script.Parent.Text == "Anti-Bag" then
		script.Parent.Text = "UnAnti-Bag"
		script.Parent.Check.Image = "rbxassetid://10221330509"



		--start
		_G.drop = true
		repeat wait()
			if _G.drop == true then

				local LocalPlayer = game:GetService("Players").LocalPlayer
				local char = LocalPlayer.Character
				char.ChildAdded:Connect(function(sock)
					if sock:IsA("MeshPart") then do
							wait(0)
							sock:Destroy()
						end
					end
				end)

			end
		until _G.drop == false



	else
		script.Parent.Text = "Anti-Bag"
		script.Parent.Check.Image = "rbxassetid://10221453823"
		_G.drop = false
	end
