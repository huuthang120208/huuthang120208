if game:GetService("Players").localPlayer.Data.Stats.Melee.Level.Value and game:GetService("Players").localPlayer.Data.Stats.Defense.Level.Value and game:GetService("Players").localPlayer.Data.Stats["Demon Fruit"].Level.Value ~= 2550 then
 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam","Pirates")
 wait(5)
 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon")
 _G.PointStats = 9999
 _G.PointStatsSmall = 2550
 spawn(function()
    while wait() do
        pcall(function()
            if game:GetService("Players").localPlayer.Data.Stats.Melee.Level.Value ~= 2550 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee",_G.PointStats)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                end
        end)
    end
end)
spawn(function()
     while wait() do
         pcall(function()
            if game:GetService("Players").localPlayer.Data.Stats.Defense.Level.Value ~= 2550 then
                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense",_G.PointStats)
                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                 end
         end)
     end
 end)

 spawn(function() -- demon fruit
     while wait() do
         pcall(function()
            if game:GetService("Players").localPlayer.Data.Stats["Demon Fruit"].Level.Value ~= 2550 then
                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","1")
                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
                     game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit",_G.PointStatsSmall) 
                 end
         end)
     end
 end)
end
