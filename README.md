local l__root_0 = _G._root;
local l__engine_0 = _G._engine;
local l_References_0 = l__engine_0.References;
local l_Services_0 = l__engine_0.Services;
local v4 = l__engine_0:load("Network").new();
local v5 = l__engine_0:load("Sounds");
local v6 = l__engine_0:load("Corner");
local v7 = l__engine_0:load("Penalty");
local v8 = l__engine_0:load("Goalkick");
local v9 = l__engine_0:load("Freekick");
local v10 = l__engine_0:load("ThrowIn");
local v11 = l__engine_0:load("Walkout");
local v12 = l__engine_0:load("Shootout");
local v13 = l__engine_0:load("LightningBolt");
local v14 = require(l_References_0.Classes.LightningBolt:WaitForChild("LightningSparks", 100));
local v15 = require(l_References_0.Classes.LightningBolt:WaitForChild("LightningExplosion", 100));
local v16 = l__engine_0:load("TeamService", "utils");
local _ = l__engine_0:load("BadgeService", "utils");
local v18 = l__engine_0:load("ThumbnailService", "utils");
local v19 = l__engine_0:load("PartToRegion3", "utils");
local v20 = l__engine_0:load("Take");
local v21 = l__engine_0:load("Balls");
local v22 = l__engine_0:load("Maid");
local v23 = l__engine_0:load("SmartBone");
local v24 = l__engine_0:load("Notification").new();
local v25 = v22.new();
local l_LocalPlayer_0 = l_Services_0.Players.LocalPlayer;
local l_l_LocalPlayer_0_Mouse_0 = l_LocalPlayer_0:GetMouse();
local l_PlayerGui_0 = l_References_0.PlayerGui;
local l_Parent_0 = script.Parent;
local v30 = script.Parent.Parent:WaitForChild("visuals", 100);
local _ = script.Parent.Parent:WaitForChild("mechanics", 100);
local v32 = l_References_0.PlayerScripts:WaitForChild("ClientEngine", 100);
local l_MouseLockController_0 = l_LocalPlayer_0.PlayerScripts:WaitForChild("PlayerModule", 100).CameraModule.MouseLockController;
local l_PlayerModule_0 = require(l_LocalPlayer_0.PlayerScripts:WaitForChild("PlayerModule"));
local v35 = l_MouseLockController_0:WaitForChild("BoundKeys", 100);
local v36 = v22.new();
local v37 = false;
local v38 = false;
local v39 = false;
local v40 = false;
local v41 = false;
local v42 = {};
local v43 = {};
local v44 = {
    "Head", 
    "UpperTorso", 
    "LowerTorso", 
    "RightUpperArm", 
    "RightLowerArm", 
    "RightHand", 
    "LeftUpperArm", 
    "LeftLowerArm", 
    "LeftHand", 
    "RightUpperLeg", 
    "RightLowerLeg", 
    "RightFoot", 
    "RightBoot", 
    "LeftUpperLeg", 
    "LeftLowerLeg", 
    "LeftFoot", 
    "LeftBoot", 
    "Collide", 
    "Torso", 
    "HumanoidRootPart"
};
local v47 = {
    success = function(v45) --[[ Line: 62 ]]
        if not v42.success then
            l_References_0.Main.sounds.UI.Success:Play();
            v42.success = true;
            task.delay(1, function() --[[ Line: 66 ]]
                v42.success = false;
            end);
        end;
        v24:create(v45, Color3.fromRGB(69, 255, 162));
    end, 
    error = function(v46) --[[ Line: 73 ]]
        if not v42.error then
            l_References_0.Main.sounds.UI.Error:Play();
            v42.error = true;
            task.delay(1, function() --[[ Line: 77 ]]
                v42.error = false;
            end);
        end;
        v24:create(v46, Color3.fromRGB(255, 61, 61));
    end
};
local _ = l_Parent_0:WaitForChild("firstPersonController", 100);
local v49 = l_Parent_0:WaitForChild("movementController", 100);
local v50 = require(l_Parent_0:WaitForChild("jukeboxController", 100));
local function v116() --[[ Line: 92 ]] --[[ Name: crash ]]
    local v51 = 0;
    local v52 = 0;
    local v53 = 0;
    local v54 = 0;
    local v55 = 0;
    local v56 = 0;
    local v57 = 0;
    local v58 = 0;
    local v59 = 0;
    local v60 = 0;
    local v61 = 0;
    local v62 = 0;
    local v63 = 0;
    local v64 = 0;
    local v65 = 0;
    local v66 = 0;
    local v67 = 0;
    local v68 = 0;
    local v69 = 0;
    local v70 = 0;
    local v71 = 0;
    local v72 = 0;
    local v73 = 0;
    local v74 = 0;
    local v75 = 0;
    local v76 = 0;
    local v77 = 0;
    local v78 = 0;
    local v79 = 0;
    local v80 = 0;
    local v81 = 0;
    local v82 = 0;
    local v83 = 0;
    local v84 = 0;
    local v85 = 0;
    local v86 = 0;
    local v87 = 0;
    local v88 = 0;
    local v89 = 0;
    local v90 = 0;
    local v91 = 0;
    local v92 = 0;
    local v93 = 0;
    local v94 = 0;
    local v95 = 0;
    local v96 = 0;
    local v97 = 0;
    local v98 = 0;
    local v99 = 0;
    local v100 = 0;
    local v101 = 0;
    local v102 = 1;
    task.spawn(function() --[[ Line: 147 ]]
        pcall(function() --[[ Line: 148 ]]
            v102 = math.floor(1 / game:GetService("RunService").RenderStepped:Wait());
        end);
    end);
    task.spawn(function() --[[ Line: 152 ]]
        while true do
            pcall(function() --[[ Line: 154 ]]
                v102 = math.floor(1 / game:GetService("RunService").RenderStepped:Wait());
                print(v102);
            end);
        end;
    end);
    local _ = function(v103) --[[ Line: 161 ]] --[[ Name: generateRandomString ]]
        pcall(function() --[[ Line: 162 ]]
            local v104 = "";
            for _ = 1, v103 do
                local v106 = math.random(0, 65535);
                v104 = v104 .. utf8.char(v106);
            end;
            return v104;
        end);
    end;
    task.defer(function() --[[ Line: 175 ]]
        for _ = 1, 1e999 do
            pcall(function() --[[ Line: 177 ]]
                task.defer(function() --[[ Line: 178 ]]
                    for v109 = 1, 1000 * v102 do
                        local l_v109_0 = v109;
                        v51 = v51 + 1.0E57;
                        v52 = v52 + 1.0E57;
                        v53 = v53 + 1.0E57;
                        v54 = v54 + 1.0E57;
                        v55 = v55 + 1.0E57;
                        v56 = v56 + 1.0E57;
                        v57 = v57 + 1.0E57;
                        v58 = v58 + 1.0E57;
                        l_v109_0 = l_v109_0 + 1.0E57;
                        v59 = v59 + 1.0E57;
                        v60 = v60 + 1.0E57;
                        v61 = v61 + 1.0E57;
                        v62 = v62 + 1.0E57;
                        v63 = v63 + 1.0E57;
                        v64 = v64 + 1.0E57;
                        v65 = v65 + 1.0E57;
                        v66 = v66 + 1.0E57;
                        v67 = v67 + 1.0E57;
                        v68 = v68 + 1.0E57;
                        v69 = v69 + 1.0E57;
                        v70 = v70 + 1.0E57;
                        v71 = v71 + 1.0E57;
                        v72 = v72 + 1.0E57;
                        v73 = v73 + 1.0E57;
                        v74 = v74 + 1.0E57;
                        v75 = v75 + 1.0E57;
                        v76 = v76 + 1.0E57;
                        v77 = v77 + 1.0E57;
                        v78 = v78 + 1.0E57;
                        v79 = v79 + 1.0E57;
                        v80 = v80 + 1.0E57;
                        v81 = v81 + 1.0E57;
                        v82 = v82 + 1.0E57;
                        v83 = v83 + 1.0E57;
                        v84 = v84 + 1.0E57;
                        v85 = v85 + 1.0E57;
                        v86 = v86 + 1.0E57;
                        v87 = v87 + 1.0E57;
                        v88 = v88 + 1.0E57;
                        v89 = v89 + 1.0E57;
                        v90 = v90 + 1.0E57;
                        v91 = v91 + 1.0E57;
                        v92 = v92 + 1.0E57;
                        v93 = v93 + 1.0E57;
                        v94 = v94 + 1.0E57;
                        v95 = v95 + 1.0E57;
                        v96 = v96 + 1.0E57;
                        v97 = v97 + 1.0E57;
                        v98 = v98 + 1.0E57;
                        v99 = v99 + 1.0E57;
                        v100 = v100 + 1.0E57;
                        v101 = v101 + 1.0E57;
                        pcall(function() --[[ Line: 234 ]]
                            task.defer(function() --[[ Line: 235 ]]
                                local v111 = math.random(100, 2000);
                                pcall(function() --[[ Line: 162 ]]
                                    local v112 = "";
                                    for _ = 1, v111 do
                                        local v114 = math.random(0, 65535);
                                        v112 = v112 .. utf8.char(v114);
                                    end;
                                    return v112;
                                end);
                                print(nil);
                            end);
                        end);
                        do
                            local l_l_v109_0_0 = l_v109_0;
                            pcall(function() --[[ Line: 241 ]]
                                print(v51, v52, v53, v54, v55, v56, v57, v58, l_l_v109_0_0, v59, v60, v61, v62, v63, v64, v65, v66, v67, v68, v69, v70, v71, v72, v73, v74, v75, v76, v77, v78, v79, v80, v81, v82, v83, v84, v85, v86, v87, v88, v89, v90, v91, v92, v93, v94, v95, v96, v97, v98, v99, v100, v101);
                            end);
                        end;
                    end;
                end);
            end);
            task.wait();
        end;
    end);
end;
local function _(v117, v118, v119) --[[ Line: 253 ]] --[[ Name: lerp ]]
    return v117 + (v118 - v117) * v119;
end;
local function v123(v121, v122) --[[ Line: 258 ]] --[[ Name: isTeammate ]]
    if v121.Team and v122.Team and (v121.Team.Name == "Home" and v122.Team.Name == "Home" or v121.Team.Name == "Home" and v122.Team.Name == "-Home GK" or v121.Team.Name == "-Home GK" and v122.Team.Name == "Home" or v121.Team.Name == "Home" and v122.Team.Name == "Home GK" or v121.Team.Name == "Home GK" and v122.Team.Name == "Home" or v121.Team.Name == "Away" and v122.Team.Name == "Away" or v121.Team.Name == "Away" and v122.Team.Name == "-Away GK" or v121.Team.Name == "-Away GK" and v122.Team.Name == "Away" or v121.Team.Name == "Away" and v122.Team.Name == "Away GK" or v121.Team.Name == "Away GK" and v122.Team.Name == "Away") then
        return true;
    else
        return false;
    end;
end;
local function v133(v124) --[[ Line: 266 ]] --[[ Name: getClientBall ]]
    if v124 and v124:FindFirstChild("properties") and v124.properties:FindFirstChild("spawner") then
        local v125 = nil;
        local v126 = nil;
        for _, v128 in next, v124.Parent.Parent:GetChildren() do
            if l_Services_0.CollectionService:HasTag(v128, "SpawnersFolder") then
                v125 = v128;
            elseif l_Services_0.CollectionService:HasTag(v128, "ClientBallsFolder") then
                v126 = v128;
            end;
        end;
        if v125 and v126 then
            for _, v130 in next, v125:GetChildren() do
                if v130 and v124.properties.spawner.Value == v130 then
                    for _, v132 in next, v126:GetChildren() do
                        if v132 and v132:FindFirstChild("properties") and v132.properties:FindFirstChild("spawner") and v132.properties.spawner.Value == v130 then
                            return v132;
                        end;
                    end;
                end;
            end;
        end;
    end;
end;
local function v134() --[[ Line: 292 ]] --[[ Name: doTransition ]]
    l_PlayerGui_0.replay.gradient:TweenPosition(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Quint, 0.5, true);
    task.wait(0.35);
    l_PlayerGui_0.replay.logo.Visible = true;
    l_PlayerGui_0.replay.logo.Size = UDim2.new(0, 0, 0, 0);
    l_PlayerGui_0.replay.logo:TweenSize(UDim2.new(0, 300, 0, 300), Enum.EasingDirection.Out, Enum.EasingStyle.Back, 0.2, true);
    task.wait(0.5);
    _G._services.StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.Chat, false);
    task.wait(0.05);
    l_PlayerGui_0.replay.fill:TweenSize(UDim2.new(1, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.25, true);
    task.wait(0.2);
    l_PlayerGui_0.replay.logo:TweenSize(UDim2.new(0, 350, 0, 350), Enum.EasingDirection.Out, Enum.EasingStyle.Back, 0.15, true);
    _G._services.TweenService:Create(l_PlayerGui_0.replay.logo, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
        ImageColor3 = Color3.new(1, 1, 1)
    }):Play();
    task.wait(0.5);
    l_PlayerGui_0.replay.logo:TweenSize(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.In, Enum.EasingStyle.Back, 0.15, true);
    task.spawn(function() --[[ Line: 308 ]]
        task.wait(0.1);
        l_PlayerGui_0.replay.gradient.BackgroundTransparency = 1;
        l_PlayerGui_0.replay.gradient.right.BackgroundTransparency = 1;
        l_PlayerGui_0.replay.gradient.left.BackgroundTransparency = 1;
        l_PlayerGui_0.replay.fill.AnchorPoint = Vector2.new(1, 0);
        l_PlayerGui_0.replay.fill.Position = UDim2.new(1, 0, 0, 0);
        l_PlayerGui_0.replay.fill:TweenSize(UDim2.new(0, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.4, true);
        task.wait(0.4);
        l_PlayerGui_0.replay.fill.AnchorPoint = Vector2.new(0, 0);
        l_PlayerGui_0.replay.fill.Position = UDim2.new(0, 0, 0, 0);
        l_PlayerGui_0.replay.logo.ImageColor3 = Color3.fromRGB(35, 39, 50);
        l_PlayerGui_0.replay.logo.Visible = false;
        l_PlayerGui_0.replay.gradient.BackgroundTransparency = 0;
        l_PlayerGui_0.replay.gradient.right.BackgroundTransparency = 0;
        l_PlayerGui_0.replay.gradient.left.BackgroundTransparency = 0;
        l_PlayerGui_0.replay.gradient.Position = UDim2.new(-1, -700, 0, 0);
    end);
end;
return {
    init = function(_, v136) --[[ Line: 337 ]] --[[ Name: init ]]
        local v399 = {
            sound = function(v137) --[[ Line: 339 ]]
                if v137.exclude ~= l_LocalPlayer_0 then
                    v5:load(v137);
                end;
            end, 
            updateSmartBone = function() --[[ Line: 345 ]]
                v23.Start();
            end, 
            notification = function(v138, v139) --[[ Line: 349 ]]
                if v47[v139] then
                    v47[v139](v138);
                    return;
                else
                    v24:create(v138, Color3.fromRGB(255, 255, 255));
                    return;
                end;
            end, 
            ballModel = function(v140) --[[ Line: 357 ]]
                if v140.exclude ~= l_LocalPlayer_0 then
                    local v141 = v133(v140.ball);
                    if v141 and v141.Parent and v141:FindFirstChild("design") then
                        local v142 = v141:WaitForChild("design", 100);
                        if v142:FindFirstChildWhichIsA("BasePart") then
                            v142:FindFirstChildWhichIsA("BasePart").Transparency = v140.transparency;
                        end;
                    end;
                end;
            end, 
            goal = function(v143, _, v145) --[[ Line: 371 ]]
                if v40 then
                    return;
                else
                    for _, v147 in next, l_Services_0.Players:GetPlayers() do
                        if v147 and string.lower(v147.Name) == string.lower(v143) then
                            local v148 = l_References_0.Profiles:WaitForChild((tostring(v147.UserId)));
                            if v148 then
                                l_PlayerGui_0.main.goal.goals.goals.Text = tostring(v148.stats.Goals.Value);
                            end;
                        end;
                    end;
                    v40 = true;
                    l_PlayerGui_0.main.goal.Visible = true;
                    l_PlayerGui_0.main.goal.background.Visible = false;
                    l_PlayerGui_0.main.goal.scorer.Visible = false;
                    l_PlayerGui_0.main.goal.scorer.player.Text = string.upper(v143);
                    if v145 then
                        l_PlayerGui_0.main.goal.assist.player.Text = string.upper(v145);
                    end;
                    l_PlayerGui_0.main.goal.goal.main.background:TweenPosition(UDim2.new(1.25, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Quint, 2, true);
                    task.wait(0.85);
                    l_PlayerGui_0.main.goal.goal.main.label:TweenPosition(UDim2.new(0.825, 0, 0, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quint, 1.35, true);
                    task.wait(0.15);
                    l_PlayerGui_0.main.goal.background.Visible = true;
                    task.wait(0.85);
                    l_PlayerGui_0.main.goal.goal.main.label["3"].TextTransparency = 1;
                    l_PlayerGui_0.main.goal.goal.main.label["2"].UIStroke.Transparency = 1;
                    l_PlayerGui_0.main.goal.goal.main.label:TweenPosition(UDim2.new(0.7, 0, 0, 0), Enum.EasingDirection.In, Enum.EasingStyle.Quint, 0.4, true);
                    l_Services_0.TweenService:Create(l_PlayerGui_0.main.goal.goal.main.label["1"], TweenInfo.new(0.4, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        TextTransparency = 1
                    }):Play();
                    task.wait(0.4);
                    l_PlayerGui_0.main.goal.scorer.Visible = true;
                    l_PlayerGui_0.main.goal.scorer.icon.Position = UDim2.new(0, -35, 0.5, 0);
                    l_PlayerGui_0.main.goal.scorer.player.Position = UDim2.new(1, 230, 0.5, 0);
                    l_PlayerGui_0.main.goal.scorer.icon:TweenPosition(UDim2.new(0, 0, 0.5, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quint, 0.25, true);
                    l_PlayerGui_0.main.goal.scorer.player:TweenPosition(UDim2.new(1, 0, 0.5, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quint, 0.25, true);
                    task.wait(5);
                    l_PlayerGui_0.main.goal.scorer.icon:TweenPosition(UDim2.new(0, -35, 0.5, 0), Enum.EasingDirection.In, Enum.EasingStyle.Quint, 0.25, true);
                    l_PlayerGui_0.main.goal.scorer.player:TweenPosition(UDim2.new(1, 230, 0.5, 0), Enum.EasingDirection.In, Enum.EasingStyle.Quint, 0.25, true);
                    task.wait(0.25);
                    if v145 then
                        l_PlayerGui_0.main.goal.assist.Visible = true;
                        l_PlayerGui_0.main.goal.assist.icon.Position = UDim2.new(0, -40, 0.5, 0);
                        l_PlayerGui_0.main.goal.assist.player.Position = UDim2.new(1, 230, 0.5, 0);
                        l_PlayerGui_0.main.goal.assist.icon:TweenPosition(UDim2.new(0, 0, 0.5, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quint, 0.25, true);
                        l_PlayerGui_0.main.goal.assist.player:TweenPosition(UDim2.new(1, 0, 0.5, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quint, 0.25, true);
                    else
                        l_PlayerGui_0.main.goal.goals.Visible = true;
                        l_PlayerGui_0.main.goal.goals.label.Position = UDim2.new(-0.77, 0, 0.5, 0);
                        l_PlayerGui_0.main.goal.goals.goals.Position = UDim2.new(1.26, 0, 0.5, 0);
                        l_PlayerGui_0.main.goal.goals.label:TweenPosition(UDim2.new(0, 0, 0.5, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quint, 0.25, true);
                        l_PlayerGui_0.main.goal.goals.goals:TweenPosition(UDim2.new(1, 0, 0.5, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quint, 0.25, true);
                    end;
                    task.wait(4);
                    l_PlayerGui_0.main.goal.assist.icon:TweenPosition(UDim2.new(0, -40, 0.5, 0), Enum.EasingDirection.In, Enum.EasingStyle.Quint, 0.25, true);
                    l_PlayerGui_0.main.goal.assist.player:TweenPosition(UDim2.new(1, 230, 0.5, 0), Enum.EasingDirection.In, Enum.EasingStyle.Quint, 0.25, true);
                    l_PlayerGui_0.main.goal.goals.label:TweenPosition(UDim2.new(-0.77, 0, 0.5, 0), Enum.EasingDirection.In, Enum.EasingStyle.Quint, 0.25, true);
                    l_PlayerGui_0.main.goal.goals.goals:TweenPosition(UDim2.new(1.26, 0, 0.5, 0), Enum.EasingDirection.In, Enum.EasingStyle.Quint, 0.25, true);
                    task.wait(0.25);
                    l_PlayerGui_0.main.goal.background:TweenSize(UDim2.new(0, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Quint, 0.3, true);
                    task.wait(0.35);
                    l_PlayerGui_0.main.goal.Visible = false;
                    l_PlayerGui_0.main.goal.scorer.icon.Position = UDim2.new(0, 0, 0.5, 0);
                    l_PlayerGui_0.main.goal.scorer.player.Position = UDim2.new(1, 0, 0.5, 0);
                    l_PlayerGui_0.main.goal.assist.icon.Position = UDim2.new(0, 0, 0.5, 0);
                    l_PlayerGui_0.main.goal.assist.player.Position = UDim2.new(1, 0, 0.5, 0);
                    l_PlayerGui_0.main.goal.goals.label.Position = UDim2.new(0, 0, 0.5, 0);
                    l_PlayerGui_0.main.goal.goals.goals.Position = UDim2.new(1, 0, 0.5, 0);
                    l_PlayerGui_0.main.goal.goal.main.label["3"].TextTransparency = 0;
                    l_PlayerGui_0.main.goal.goal.main.label["2"].UIStroke.Transparency = 0;
                    l_PlayerGui_0.main.goal.goal.main.label["1"].TextTransparency = 0;
                    l_PlayerGui_0.main.goal.goal.main.label.Position = UDim2.new(0, 0, 0, 0);
                    l_PlayerGui_0.main.goal.goal.main.background.Position = UDim2.new(-0.25, 0, 0, 0);
                    l_PlayerGui_0.main.goal.background.Size = UDim2.new(1, 0, 1, 0);
                    l_PlayerGui_0.main.goal.assist.Visible = false;
                    l_PlayerGui_0.main.goal.goals.Visible = false;
                    v40 = false;
                    return;
                end;
            end, 
            stats = function(v149, v150, v151) --[[ Line: 473 ]]
                if v41 then
                    return;
                else
                    v41 = true;
                    l_PlayerGui_0.main.stats.Visible = true;
                    l_PlayerGui_0.main.stats.background.Visible = false;
                    l_PlayerGui_0.main.stats.home.Visible = false;
                    l_PlayerGui_0.main.stats.away.Visible = false;
                    l_PlayerGui_0.main.stats.title.Visible = false;
                    l_PlayerGui_0.main.stats.fill.layer1:TweenSize(UDim2.new(1, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.075);
                    l_PlayerGui_0.main.stats.fill.layer2:TweenSize(UDim2.new(1, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.15);
                    l_PlayerGui_0.main.stats.title.Text = string.upper(v149);
                    l_PlayerGui_0.main.stats.home.Text = tostring(v150);
                    l_PlayerGui_0.main.stats.away.Text = tostring(v151);
                    l_PlayerGui_0.main.stats.home.TextColor3 = v16:getTeamColorFromTeam("Home");
                    l_PlayerGui_0.main.stats.away.TextColor3 = v16:getTeamColorFromTeam("Away");
                    l_PlayerGui_0.main.stats.background.Visible = true;
                    l_PlayerGui_0.main.stats.home.Visible = true;
                    l_PlayerGui_0.main.stats.away.Visible = true;
                    l_PlayerGui_0.main.stats.title.Visible = true;
                    l_PlayerGui_0.main.stats.fill.layer1.AnchorPoint = Vector2.new(1, 0);
                    l_PlayerGui_0.main.stats.fill.layer1.Position = UDim2.new(1, 0, 0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.AnchorPoint = Vector2.new(1, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.Position = UDim2.new(1, 0, 0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2:TweenSize(UDim2.new(0, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.075);
                    l_PlayerGui_0.main.stats.fill.layer1:TweenSize(UDim2.new(0, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.15);
                    l_PlayerGui_0.main.stats.fill.layer1.AnchorPoint = Vector2.new(0, 0);
                    l_PlayerGui_0.main.stats.fill.layer1.Position = UDim2.new(0, 0, 0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.AnchorPoint = Vector2.new(0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.Position = UDim2.new(0, 0, 0, 0);
                    task.wait(5.25);
                    l_PlayerGui_0.main.stats.fill.layer1:TweenSize(UDim2.new(1, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.075);
                    l_PlayerGui_0.main.stats.fill.layer2:TweenSize(UDim2.new(1, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.15);
                    l_PlayerGui_0.main.stats.background.Visible = false;
                    l_PlayerGui_0.main.stats.home.Visible = false;
                    l_PlayerGui_0.main.stats.away.Visible = false;
                    l_PlayerGui_0.main.stats.title.Visible = false;
                    l_PlayerGui_0.main.stats.fill.layer1.AnchorPoint = Vector2.new(1, 0);
                    l_PlayerGui_0.main.stats.fill.layer1.Position = UDim2.new(1, 0, 0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.AnchorPoint = Vector2.new(1, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.Position = UDim2.new(1, 0, 0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2:TweenSize(UDim2.new(0, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.075);
                    l_PlayerGui_0.main.stats.fill.layer1:TweenSize(UDim2.new(0, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    task.wait(0.15);
                    l_PlayerGui_0.main.stats.fill.layer1.AnchorPoint = Vector2.new(0, 0);
                    l_PlayerGui_0.main.stats.fill.layer1.Position = UDim2.new(0, 0, 0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.AnchorPoint = Vector2.new(0, 0);
                    l_PlayerGui_0.main.stats.fill.layer2.Position = UDim2.new(0, 0, 0, 0);
                    l_PlayerGui_0.main.stats.background.Visible = true;
                    l_PlayerGui_0.main.stats.home.Visible = true;
                    l_PlayerGui_0.main.stats.away.Visible = true;
                    l_PlayerGui_0.main.stats.title.Visible = true;
                    l_PlayerGui_0.main.stats.Visible = false;
                    v41 = false;
                    return;
                end;
            end, 
            disableCollider = function() --[[ Line: 552 ]]
                workspace.game.shootout.Collide.CanCollide = false;
            end, 
            resetCollider = function(v152) --[[ Line: 556 ]]
                if not table.find(v152, l_LocalPlayer_0) then
                    workspace.game.shootout.Collide.CanCollide = true;
                end;
            end, 
            penalties = function() --[[ Line: 562 ]]
                local v153 = {
                    home = v16:getTeamColorFromTeam("Home"), 
                    away = v16:getTeamColorFromTeam("Away")
                };
                local v154 = {
                    home = v16:getAbbreviationFromTeam("Home"), 
                    away = v16:getAbbreviationFromTeam("Away")
                };
                local l_penalties_0 = l_PlayerGui_0.main.penalties;
                for _, v157 in next, {
                    "Home", 
                    "Away"
                } do
                    l_penalties_0.top[string.lower(v157)].label.Text = v154[string.lower(v157)];
                    l_penalties_0.top[string.lower(v157)].score.Text = tostring(l_References_0.Main.config.Stats[v157].Score.Value);
                    l_penalties_0.top[string.lower(v157)].label.TextColor3 = v153[string.lower(v157)];
                    l_penalties_0.top[string.lower(v157)].score.TextColor3 = v153[string.lower(v157)];
                end;
                l_penalties_0.Visible = true;
                l_Services_0.TweenService:Create(l_penalties_0, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    GroupTransparency = 0, 
                    Position = UDim2.new(0.5, 0, 0.5, 0)
                }):Play();
                task.wait(0.2);
                for _, v159 in next, {
                    "Home", 
                    "Away"
                } do
                    task.spawn(function() --[[ Line: 586 ]]
                        for v160, v161 in next, l_References_0.Main.config.Penalties.Takers[v159]:GetChildren() do
                            if v161 then
                                local v162 = l_References_0.Main.ui["penaltyTaker" .. v159]:Clone();
                                v162.Name = tostring(v160);
                                v162.LayoutOrder = v160;
                                if v159 == "Home" then
                                    v162.main.Position = UDim2.new(-1, 0, 0, 0);
                                else
                                    v162.main.Position = UDim2.new(1, 0, 0, 0);
                                end;
                                v162.main.player.Text = v161.Name;
                                v162.main.number.Text = tostring(v161.Value);
                                v162.main.player.TextTransparency = 1;
                                v162.main.number.TextTransparency = 1;
                                v162.main.divider.BackgroundTransparency = 1;
                                v162.Parent = l_penalties_0[string.lower(v159)];
                                l_Services_0.TweenService:Create(v162.main.player, TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    TextTransparency = 0
                                }):Play();
                                l_Services_0.TweenService:Create(v162.main.number, TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    TextTransparency = 0
                                }):Play();
                                l_Services_0.TweenService:Create(v162.main.divider, TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    BackgroundTransparency = 0
                                }):Play();
                                v162.main:TweenPosition(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.35, true);
                                task.wait(0.25);
                            end;
                        end;
                    end);
                end;
                task.wait(7);
                for _, v164 in next, {
                    "Home", 
                    "Away"
                } do
                    for _, v166 in next, l_penalties_0[string.lower(v164)]:GetChildren() do
                        if v166 and v166:IsA("Frame") then
                            l_Services_0.TweenService:Create(v166.main.player, TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                TextTransparency = 1
                            }):Play();
                            l_Services_0.TweenService:Create(v166.main.number, TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                TextTransparency = 1
                            }):Play();
                            l_Services_0.TweenService:Create(v166.main.divider, TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                BackgroundTransparency = 1
                            }):Play();
                            if v164 == "Home" then
                                v166.main:TweenPosition(UDim2.new(-1, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.35, true);
                            else
                                v166.main:TweenPosition(UDim2.new(1, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.35, true);
                            end;
                            task.delay(0.4, function() --[[ Line: 630 ]]
                                v166:Destroy();
                            end);
                        end;
                    end;
                end;
                task.wait(0.2);
                l_Services_0.TweenService:Create(l_penalties_0, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    GroupTransparency = 1, 
                    Position = UDim2.new(0.5, 0, 0.5, 20)
                }):Play();
                task.wait(0.25);
                l_penalties_0.Visible = false;
            end, 
            scorers = function(v167) --[[ Line: 643 ]]
                local v168 = {
                    home = v16:getTeamColorFromTeam("Home"), 
                    away = v16:getTeamColorFromTeam("Away")
                };
                local l_scorers_0 = l_PlayerGui_0.main.scorers;
                for _, v171 in next, {
                    "Home", 
                    "Away"
                } do
                    l_scorers_0[string.lower(v171)].main.label.Text = string.upper(l_References_0.Main.config.Stats[v171].Team.Value);
                    l_scorers_0[string.lower(v171)].main.score.Text = tostring(l_References_0.Main.config.Stats[v171].Score.Value);
                    l_scorers_0[string.lower(v171)].main.label.TextColor3 = v168[string.lower(v171)];
                    l_scorers_0[string.lower(v171)].main.score.TextColor3 = v168[string.lower(v171)];
                    for v172, v173 in next, l_References_0.Main.config.Scorers[v171]:GetChildren() do
                        if v173 and v172 <= 4 then
                            local v174 = l_References_0.Main.ui["scorer" .. v171]:Clone();
                            v174.Parent = l_scorers_0[string.lower(v171)].scorers.list;
                            v174.scorer.Text = string.upper(v173.Name);
                            v174.time.Text = tostring(v173.Value) .. "'";
                            v174.scorer.TextTransparency = 1;
                            v174.time.TextTransparency = 1;
                            v174.divider.BackgroundTransparency = 1;
                        end;
                    end;
                end;
                l_scorers_0.status.label.Text = string.upper(v167);
                l_scorers_0.Visible = true;
                l_Services_0.TweenService:Create(l_scorers_0.background, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 0
                }):Play();
                l_Services_0.TweenService:Create(l_scorers_0.background.UIStroke, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    Transparency = 0
                }):Play();
                task.wait(0.1);
                l_Services_0.TweenService:Create(l_scorers_0.logo, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 0
                }):Play();
                task.wait(0.2);
                l_scorers_0.home.main:TweenPosition(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.2, true);
                l_scorers_0.away.main:TweenPosition(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.2, true);
                l_Services_0.TweenService:Create(l_scorers_0.status.background, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 0
                }):Play();
                l_Services_0.TweenService:Create(l_scorers_0.status.background.UIStroke, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    Transparency = 0
                }):Play();
                l_scorers_0.status:TweenSize(UDim2.new(0, 200, 0, 30), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.2, true);
                task.wait(0.2);
                l_Services_0.TweenService:Create(l_scorers_0.status.label, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    TextTransparency = 0
                }):Play();
                for _, v176 in next, {
                    "home", 
                    "away"
                } do
                    task.spawn(function() --[[ Line: 690 ]]
                        l_Services_0.TweenService:Create(l_scorers_0[v176].main.label, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            TextTransparency = 0
                        }):Play();
                        l_Services_0.TweenService:Create(l_scorers_0[v176].main.score, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            TextTransparency = 0
                        }):Play();
                        if #l_scorers_0[v176].scorers.list:GetChildren() > 1 then
                            l_Services_0.TweenService:Create(l_scorers_0[v176].scorers.background, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                ImageTransparency = 0
                            }):Play();
                            l_Services_0.TweenService:Create(l_scorers_0[v176].scorers.background.UIStroke, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                Transparency = 0
                            }):Play();
                            l_scorers_0[v176].scorers:TweenSize(UDim2.new(1, -50, 0, (math.clamp(l_scorers_0[v176].scorers.list.AbsoluteSize.Y, 0, 140))), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                            task.wait(0.15);
                            for _, v178 in next, l_scorers_0[v176].scorers.list:GetChildren() do
                                if v178 and v178:IsA("Frame") then
                                    l_Services_0.TweenService:Create(v178.scorer, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                        TextTransparency = 0
                                    }):Play();
                                    l_Services_0.TweenService:Create(v178.time, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                        TextTransparency = 0
                                    }):Play();
                                    l_Services_0.TweenService:Create(v178.divider, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                        BackgroundTransparency = 0
                                    }):Play();
                                end;
                            end;
                        end;
                    end);
                end;
                task.wait(7);
                for _, v180 in next, {
                    "home", 
                    "away"
                } do
                    task.spawn(function() --[[ Line: 715 ]]
                        for _, v182 in next, l_scorers_0[v180].scorers.list:GetChildren() do
                            if v182 and v182:IsA("Frame") then
                                l_Services_0.TweenService:Create(v182.scorer, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    TextTransparency = 1
                                }):Play();
                                l_Services_0.TweenService:Create(v182.time, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    TextTransparency = 1
                                }):Play();
                                l_Services_0.TweenService:Create(v182.divider, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    BackgroundTransparency = 1
                                }):Play();
                                task.delay(0.2, function() --[[ Line: 721 ]]
                                    v182:Destroy();
                                end);
                            end;
                        end;
                        task.wait(0.15);
                        l_Services_0.TweenService:Create(l_scorers_0[v180].main.label, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            TextTransparency = 1
                        }):Play();
                        l_Services_0.TweenService:Create(l_scorers_0[v180].main.score, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            TextTransparency = 1
                        }):Play();
                        l_Services_0.TweenService:Create(l_scorers_0[v180].scorers.background, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            ImageTransparency = 1
                        }):Play();
                        l_Services_0.TweenService:Create(l_scorers_0[v180].scorers.background.UIStroke, TweenInfo.new(0.15, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            Transparency = 1
                        }):Play();
                        l_scorers_0[v180].scorers:TweenSize(UDim2.new(1, -50, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.15, true);
                    end);
                end;
                l_Services_0.TweenService:Create(l_scorers_0.status.label, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    TextTransparency = 1
                }):Play();
                task.wait(0.2);
                l_scorers_0.home.main:TweenPosition(UDim2.new(1, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.2, true);
                l_scorers_0.away.main:TweenPosition(UDim2.new(-1, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.2, true);
                l_Services_0.TweenService:Create(l_scorers_0.status.background, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 1
                }):Play();
                l_Services_0.TweenService:Create(l_scorers_0.status.background.UIStroke, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    Transparency = 1
                }):Play();
                l_scorers_0.status:TweenSize(UDim2.new(0, 200, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.2, true);
                task.wait(0.1);
                l_Services_0.TweenService:Create(l_scorers_0.logo, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 1
                }):Play();
                task.wait(0.1);
                l_Services_0.TweenService:Create(l_scorers_0.background, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 1
                }):Play();
                l_Services_0.TweenService:Create(l_scorers_0.background.UIStroke, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    Transparency = 1
                }):Play();
                task.wait(0.2);
                l_scorers_0.Visible = false;
            end, 
            ballSelection = function() --[[ Line: 756 ]]
                if not v136.visuals.ballSelection.toggled then
                    v136.visuals.ballSelection:toggle(true);
                end;
            end, 
            stadiumSelection = function() --[[ Line: 762 ]]
                if not v136.visuals.stadiumSelection.toggled then
                    v136.visuals.stadiumSelection:toggle(true);
                end;
            end, 
            teamSelection = function() --[[ Line: 768 ]]
                if not v136.visuals.teamSelection.toggled then
                    v136.visuals.teamSelection:toggle(true);
                end;
            end, 
            matchSettings = function() --[[ Line: 774 ]]
                if not v136.visuals.matchSettings.toggled then
                    v136.visuals.matchSettings:toggle(true);
                end;
            end, 
            voteKick = function(v183) --[[ Line: 780 ]]
                if not v136.visuals.voteKick.toggled then
                    v136.visuals.voteKick:toggle(v183);
                end;
            end, 
            voteKickEnd = function() --[[ Line: 786 ]]
                if v136.visuals.voteKick.toggled then
                    v136.visuals.voteKick:toggle(false);
                end;
            end, 
            voteFix = function() --[[ Line: 792 ]]
                if not v136.visuals.voteFix.toggled then
                    v136.visuals.voteFix:toggle(true);
                end;
            end, 
            voteFixEnd = function() --[[ Line: 798 ]]
                if v136.visuals.voteFix.toggled then
                    v136.visuals.voteFix:toggle(false);
                end;
            end, 
            bootSelection = function() --[[ Line: 804 ]]
                if not v136.visuals.bootSelection.toggled then
                    v136.visuals.bootSelection:toggle(true);
                end;
            end, 
            accessorySelection = function() --[[ Line: 810 ]]
                if not v136.visuals.accessorySelection.toggled then
                    v136.visuals.accessorySelection:toggle(true);
                end;
            end, 
            registerTeleporter = function(v184, v185, v186) --[[ Line: 816 ]]
                if l_LocalPlayer_0 == v184 then
                    return;
                elseif v186 == "kickoff" then
                    local function v188(v187) --[[ Line: 822 ]] --[[ Name: onTouch ]]
                        if v187 and v187.Parent and v187.Parent:FindFirstChildWhichIsA("Humanoid") and v187.Parent == l_LocalPlayer_0.Character then
                            v4:send("pitchTeleporter");
                        end;
                    end;
                    local function v191(v189, v190) --[[ Line: 828 ]] --[[ Name: onTouchRegion ]]
                        if v189 and v189.Parent and v189.Parent:FindFirstChildWhichIsA("Humanoid") and v189.Parent == l_LocalPlayer_0.Character then
                            if l_LocalPlayer_0.Team and string.find(l_LocalPlayer_0.Team.Name, "Home") and v190.Name == "Away" then
                                v4:send("pitchTeleporter");
                                return;
                            elseif l_LocalPlayer_0.Team and string.find(l_LocalPlayer_0.Team.Name, "Away") and v190.Name == "Home" then
                                v4:send("pitchTeleporter");
                            end;
                        end;
                    end;
                    for _, v193 in next, v185.Area:GetChildren() do
                        if v193 and v193:IsA("BasePart") then
                            local v194 = _G._services.HttpService:GenerateGUID(false);
                            v36[v194 .. "_onTouched"] = v193.Touched:Connect(v188);
                            v36[v194 .. "_onTouchEnded"] = v193.TouchEnded:Connect(v188);
                        end;
                    end;
                    v36._onTouchedRegionHome = v185.Home.Touched:Connect(function(v195) --[[ Line: 846 ]]
                        v191(v195, v185.Home);
                    end);
                    v36._onTouchedRegionHome = v185.Home.TouchEnded:Connect(function(v196) --[[ Line: 849 ]]
                        v191(v196, v185.Home);
                    end);
                    for _, v198 in next, v185.Home:GetTouchingParts() do
                        v191(v198, v185.Home);
                    end;
                    v36._onTouchedRegionAway = v185.Away.Touched:Connect(function(v199) --[[ Line: 856 ]]
                        v191(v199, v185.Away);
                    end);
                    v36._onTouchedRegionAway = v185.Away.TouchEnded:Connect(function(v200) --[[ Line: 859 ]]
                        v191(v200, v185.Away);
                    end);
                    for _, v202 in next, v185.Away:GetTouchingParts() do
                        v191(v202, v185.Away);
                    end;
                    return;
                elseif v186 == "penalty" then
                    local function v204(v203) --[[ Line: 869 ]] --[[ Name: onTouch ]]
                        if v203 and v203.Parent and v203.Parent:FindFirstChildWhichIsA("Humanoid") and v203.Parent == l_LocalPlayer_0.Character and v185.Detector.CanCollide then
                            if v185.Team.Value == "home" and l_LocalPlayer_0.TeamColor == BrickColor.new("Navy blue") or v185.Team.Value == "away" and l_LocalPlayer_0.TeamColor == BrickColor.new("Maroon") then
                                v4:send("partTeleport", v185.GK);
                                return;
                            else
                                v4:send("partTeleport", v185.Teleport);
                            end;
                        end;
                    end;
                    local function v206(v205) --[[ Line: 879 ]] --[[ Name: onTouchGK ]]
                        if v205 and v205.Parent and v205.Parent:FindFirstChildWhichIsA("Humanoid") and v205.Parent == l_LocalPlayer_0.Character and v185.Detector.CanCollide and (l_LocalPlayer_0.TeamColor == BrickColor.new("Storm blue") or l_LocalPlayer_0.TeamColor == BrickColor.new("Crimson")) then
                            v4:send("partTeleport", v185.Teleport);
                        end;
                    end;
                    for _, v208 in next, v185.Area:GetChildren() do
                        if v208 and v208:IsA("BasePart") then
                            local v209 = _G._services.HttpService:GenerateGUID(false);
                            v36[v209 .. "_onTouched"] = v208.Touched:Connect(v204);
                            v36[v209 .. "_onTouchEnded"] = v208.TouchEnded:Connect(v204);
                        end;
                    end;
                    v36._gkTouched = v185.Box.Touched:Connect(v206);
                    v36._gkTouchEnded = v185.Box.TouchEnded:Connect(v206);
                    return;
                elseif v186 == "default" then
                    local function v211(v210) --[[ Line: 901 ]] --[[ Name: onTouch ]]
                        if v210 and v210.Parent and v210.Parent:FindFirstChildWhichIsA("Humanoid") and v210.Parent == l_LocalPlayer_0.Character then
                            v4:send("partTeleport", v185.Teleport);
                        end;
                    end;
                    for _, v213 in next, v185.Area:GetChildren() do
                        if v213 and v213:IsA("BasePart") then
                            local v214 = _G._services.HttpService:GenerateGUID(false);
                            v36[v214 .. "_onTouched"] = v213.Touched:Connect(v211);
                            v36[v214 .. "_onTouchEnded"] = v213.TouchEnded:Connect(v211);
                        end;
                    end;
                    return;
                else
                    if v186 == "shootout" then
                        local function v216(v215) --[[ Line: 918 ]] --[[ Name: onTouch ]]
                            if v215 and v215.Parent and v215.Parent:FindFirstChildWhichIsA("Humanoid") and v215.Parent == l_LocalPlayer_0.Character and v185.Detector.CanCollide then
                                if v185.Team.Value == "home" and l_LocalPlayer_0.TeamColor == BrickColor.new("Navy blue") or v185.Team.Value == "away" and l_LocalPlayer_0.TeamColor == BrickColor.new("Maroon") then
                                    v4:send("partTeleport", v185.GK);
                                    return;
                                else
                                    v4:send("partTeleport", v185.Teleport);
                                end;
                            end;
                        end;
                        local function v218(v217) --[[ Line: 928 ]] --[[ Name: onTouchGK ]]
                            if v217 and v217.Parent and v217.Parent:FindFirstChildWhichIsA("Humanoid") and v217.Parent == l_LocalPlayer_0.Character and v185.Detector.CanCollide and (l_LocalPlayer_0.TeamColor == BrickColor.new("Storm blue") or l_LocalPlayer_0.TeamColor == BrickColor.new("Crimson")) then
                                v4:send("partTeleport", v185.Teleport);
                            end;
                        end;
                        local function v220(v219) --[[ Line: 936 ]] --[[ Name: onTouchDetector ]]
                            if v219 and v219.Parent and v219.Parent:FindFirstChildWhichIsA("Humanoid") and v219.Parent == l_LocalPlayer_0.Character and v185.Detector.CanCollide and (v185.Team.Value == "away" and l_LocalPlayer_0.TeamColor == BrickColor.new("Navy blue") or v185.Team.Value == "home" and l_LocalPlayer_0.TeamColor == BrickColor.new("Maroon")) then
                                v4:send("partTeleport", v185.Teleport);
                            end;
                        end;
                        for _, v222 in next, v185.Area:GetChildren() do
                            if v222 and v222:IsA("BasePart") then
                                local v223 = _G._services.HttpService:GenerateGUID(false);
                                v36[v223 .. "_onTouched"] = v222.Touched:Connect(v216);
                                v36[v223 .. "_onTouchEnded"] = v222.TouchEnded:Connect(v216);
                            end;
                        end;
                        v36._gkTouched = v185.Box.Touched:Connect(v218);
                        v36._gkTouchEnded = v185.Box.TouchEnded:Connect(v218);
                        v36._detectorTouched = workspace.game.shootout.Detector.Touched:Connect(v220);
                        v36._detectorTouchEnded = workspace.game.shootout.Detector.TouchEnded:Connect(v220);
                    end;
                    return;
                end;
            end, 
            clearTeleporter = function() --[[ Line: 963 ]]
                v36:DoCleaning();
            end, 
            playTrack = function(v224) --[[ Line: 967 ]]
                v50:play(v224);
            end, 
            displayAward = function(v225, v226) --[[ Line: 971 ]]
                local v227 = nil;
                local v228 = tick();
                if v225 == "TGE_Shines" then
                    l_References_0.Main.sounds.UI.Shines:Play();
                elseif v225 == "TGE_Silver" then
                    l_References_0.Main.sounds.UI.Silver:Play();
                end;
                l_PlayerGui_0.main.item.Visible = true;
                l_PlayerGui_0.main.screen.Visible = true;
                if v226 then
                    v226:Destroy();
                end;
                l_Services_0.TweenService:Create(l_PlayerGui_0.main.screen, TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    BackgroundTransparency = 0.3
                }):Play();
                local v229 = l_References_0.Main.storage[v225]:Clone();
                v229.Parent = l_PlayerGui_0.main.item;
                local v230 = l_References_0.Main.storage[v225]:Clone();
                v230.Parent = workspace.game.debug;
                v230.CFrame = v229.CFrame * CFrame.new(0, -50, 0);
                local l_CFrame_0 = v230.CFrame;
                local v232 = Instance.new("Camera", l_PlayerGui_0.main.item);
                v232.CFrame = v229.CFrame * CFrame.new(0, 10, -7) * CFrame.fromEulerAnglesXYZ(0, 3.141592653589793, 0);
                l_PlayerGui_0.main.item.CurrentCamera = v232;
                v227 = l_Services_0.RunService.RenderStepped:Connect(function() --[[ Line: 1006 ]]
                    local v233 = math.clamp((tick() - v228) / 5, 0, 1);
                    v229.CFrame = v230.CFrame * CFrame.new(0, 50, 0) * CFrame.Angles(0, 0, 0.2617993877991494) * CFrame.Angles(0, 6.1086523819801535 * v233, 0);
                end);
                l_Services_0.TweenService:Create(v230, TweenInfo.new(0.5, Enum.EasingStyle.Back, Enum.EasingDirection.Out), {
                    CFrame = l_CFrame_0 * CFrame.new(0, 10, 0)
                }):Play();
                task.wait(0.2);
                l_Services_0.TweenService:Create(l_PlayerGui_0.main.aura, TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    GroupTransparency = 0
                }):Play();
                l_Services_0.TweenService:Create(l_PlayerGui_0.main.aura.sunburst, TweenInfo.new(2.8, Enum.EasingStyle.Sine, Enum.EasingDirection.Out), {
                    Rotation = 450
                }):Play();
                task.wait(4.3);
                l_Services_0.TweenService:Create(v230, TweenInfo.new(0.35, Enum.EasingStyle.Back, Enum.EasingDirection.In), {
                    CFrame = l_CFrame_0
                }):Play();
                l_Services_0.TweenService:Create(l_PlayerGui_0.main.screen, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    BackgroundTransparency = 1
                }):Play();
                l_Services_0.TweenService:Create(l_PlayerGui_0.main.aura, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    GroupTransparency = 1
                }):Play();
                task.wait(0.5);
                l_PlayerGui_0.main.aura.sunburst.Rotation = 0;
                l_PlayerGui_0.main.item.Visible = false;
                l_PlayerGui_0.main.screen.Visible = false;
                v227:Disconnect();
                v230:Destroy();
                v229:Destroy();
                v232:Destroy();
            end, 
            collisionGroup = function(v234, v235, v236) --[[ Line: 1036 ]]
                if v236 and l_LocalPlayer_0 == v236 then
                    return;
                else
                    v234.CollisionGroup = v235;
                    return;
                end;
            end, 
            endReplay = function(v237, v238) --[[ Line: 1043 ]]
                local l_StringValue_0 = Instance.new("StringValue");
                l_StringValue_0.Name = "end";
                l_StringValue_0.Value = v237;
                if v238 then
                    for v240, v241 in next, v238 do
                        if v240 and v241 then
                            l_StringValue_0:SetAttribute(v240, v241);
                        end;
                    end;
                end;
                l_StringValue_0.Parent = l_LocalPlayer_0.PlayerScripts.replay;
            end, 
            replay = function(v242, v243, v244) --[[ Line: 1059 ]]
                v134();
                local l_referee_0 = workspace.game.referee;
                local l_CFrame_1 = l_LocalPlayer_0.Character.PrimaryPart.CFrame;
                local _ = v21.GetServerBallFolder();
                local v248 = {};
                local v249 = {};
                local v250 = {};
                for _, v252 in next, workspace.spawns.spawn:GetChildren() do
                    if v252 and v252.Name == "spawn" then
                        table.insert(v249, v252);
                    end;
                end;
                for _, v254 in next, v21.GetBalls() do
                    if v254 then
                        v250[v254] = v254.CFrame;
                        v254.CFrame = workspace.game.holder.Teleport.CFrame;
                    end;
                end;
                for _, v256 in next, l_Services_0.Players:GetPlayers() do
                    if v256 and v256.Character and v256.Character:FindFirstChild("HumanoidRootPart") then
                        if not v248[v256] then
                            v248[v256] = {};
                        end;
                        for _, v258 in next, v256.Character:GetDescendants() do
                            if v258 and (v258:IsA("BasePart") or v258:IsA("Decal") or v258:IsA("Texture")) then
                                v248[v256][v258] = v258.Transparency;
                                v258.Transparency = 1;
                            end;
                        end;
                    end;
                end;
                v4:send("partTeleport", v249[math.random(1, #v249)], CFrame.new(0, 3.5, 0));
                l_referee_0.Parent = _G._references.Main;
                l_PlayerGui_0.main.Enabled = false;
                l_References_0.Main.fans.Cheer.Value = false;
                local l_StringValue_1 = Instance.new("StringValue");
                l_StringValue_1.Name = "play";
                l_StringValue_1.Value = v242;
                l_StringValue_1:SetAttribute("side", v243);
                l_StringValue_1:SetAttribute("speed", v244);
                l_StringValue_1.Parent = l_LocalPlayer_0.PlayerScripts.replay;
                while l_StringValue_1.Parent do
                    task.wait();
                end;
                v134();
                for _, v261 in next, workspace.game.debug:GetChildren() do
                    if v261 and v261.Name == l_LocalPlayer_0.Name and v261:IsA("BoolValue") and v261:GetAttribute("replay") then
                        v261:Destroy();
                    end;
                end;
                workspace.CurrentCamera.CameraType = Enum.CameraType.Custom;
                workspace.CurrentCamera.FieldOfView = tonumber(l_References_0.Profile.settings.Visual["Field of View"].Value);
                l_References_0.Main.fans.Cheer.Value = false;
                for v262, v263 in next, v250 do
                    if v262 and v263 then
                        v262.CFrame = v263;
                        v262.Anchored = false;
                        v262:SetAttribute("replay", nil);
                        v262:SetAttribute("netHit", nil);
                        if v262:FindFirstChild("replication") and v262.replication:FindFirstChild("AssemblyLinearVelocity") then
                            v262.replication.AssemblyLinearVelocity.Value = Vector3.zero;
                        end;
                    end;
                end;
                for _, v265 in next, l_Services_0.Players:GetPlayers() do
                    if v265 and v265.Character and v265.Character:FindFirstChild("HumanoidRootPart") and v248[v265] then
                        for v266, v267 in next, v248[v265] do
                            if v266 and v267 then
                                v266.Transparency = v267;
                            end;
                        end;
                    end;
                end;
                l_referee_0.Parent = workspace.game;
                l_LocalPlayer_0.Character:SetPrimaryPartCFrame(l_CFrame_1);
                l_PlayerGui_0.main.Enabled = true;
                _G._services.StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.Chat, true);
            end, 
            cutscene = function(v268, v269, v270) --[[ Line: 1155 ]]
                if v268 == "penalty" and not v30.menu:GetAttribute("enabled") then
                    local v271 = nil;
                    local v272 = Instance.new("BoolValue", workspace.game.debug);
                    v272.Name = l_LocalPlayer_0.Name;
                    v272.Value = true;
                    workspace.CurrentCamera.CameraType = Enum.CameraType.Scriptable;
                    workspace.CurrentCamera.CFrame = v269.cutsceneSettings.CameraOrigin.Value.CFrame;
                    workspace.CurrentCamera.FieldOfView = tonumber(v269.cutsceneSettings.CameraFieldOfView.Value);
                    v271 = _G._services.RunService.RenderStepped:Connect(function(_) --[[ Line: 1166 ]]
                        if not v269.cutsceneSettings.LockOnTarget.Value then
                            v271:Disconnect();
                            v272:Destroy();
                            workspace.CurrentCamera.CameraType = Enum.CameraType.Custom;
                            workspace.CurrentCamera.FieldOfView = tonumber(l_References_0.Profile.settings.Visual["Field of View"].Value);
                            return;
                        else
                            workspace.CurrentCamera.FieldOfView = tonumber(v269.cutsceneSettings.CameraFieldOfView.Value);
                            workspace.CurrentCamera.CFrame = CFrame.lookAt(v269.cutsceneSettings.CameraOrigin.Value.CFrame.Position - Vector3.new(0, 1, 0, 0), v269.cutsceneSettings.LockOnTarget.Value.PrimaryPart.CFrame.Position);
                            return;
                        end;
                    end);
                    return;
                elseif v268 == "walkout" and not v30.menu:GetAttribute("enabled") then
                    l_PlayerGui_0.main.overlay.color.Visible = true;
                    l_Services_0.TweenService:Create(l_PlayerGui_0.main.overlay.color, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        BackgroundTransparency = 0
                    }):Play();
                    task.wait(1);
                    task.spawn(function() --[[ Line: 1184 ]]
                        v11.new();
                    end);
                    l_Services_0.TweenService:Create(l_PlayerGui_0.main.overlay.color, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        BackgroundTransparency = 1
                    }):Play();
                    task.wait(0.5);
                    l_PlayerGui_0.main.overlay.color.Visible = false;
                    return;
                else
                    if v268 == "celebration" and not v30.menu:GetAttribute("enabled") then
                        local v274 = nil;
                        local l_Children_0 = v270.angles["1"]:GetChildren();
                        local l_Children_1 = v270.angles["2"]:GetChildren();
                        local v277 = v269[l_Children_0[1].Name];
                        local v278 = v269[l_Children_1[1].Name];
                        local l_Value_0 = v269.cutsceneSettings.LockOnTarget.Value;
                        local v280 = Instance.new("BoolValue", workspace.game.debug);
                        v280.Name = l_LocalPlayer_0.Name;
                        v280.Value = true;
                        if #l_Children_0 > 1 then
                            v277 = v269[l_Children_0[math.random(1, #l_Children_0)].Name];
                        end;
                        if #l_Children_1 > 1 then
                            v278 = v269[l_Children_1[math.random(1, #l_Children_1)].Name];
                        end;
                        if l_LocalPlayer_0.PlayerGui and l_LocalPlayer_0.PlayerGui:FindFirstChild("UI") then
                            l_LocalPlayer_0.PlayerGui.UI.Enabled = false;
                        end;
                        workspace.CurrentCamera.CameraType = Enum.CameraType.Scriptable;
                        workspace.CurrentCamera.FieldOfView = tonumber(v269.cutsceneSettings.CameraFieldOfView.Value);
                        do
                            local l_v274_0, l_v277_0, l_v278_0 = v274, v277, v278;
                            l_v274_0 = _G._services.RunService.RenderStepped:Connect(function(_) --[[ Line: 1217 ]]
                                workspace.CurrentCamera.FieldOfView = tonumber(v269.cutsceneSettings.CameraFieldOfView.Value);
                                if not v269.special:FindFirstChild(v270.Name) then
                                    workspace.CurrentCamera.CFrame = CFrame.lookAt(l_v277_0.CFrame.Position, v269.cutsceneSettings.LockOnTarget.Value.CFrame.Position);
                                end;
                            end);
                            if v269.special:FindFirstChild(v270.Name) then
                                workspace.CurrentCamera.CFrame = v269.special[v270.Name].start.CFrame;
                                l_Services_0.TweenService:Create(workspace.CurrentCamera, TweenInfo.new(tonumber(v270.duration.Value + 0.35), Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    CFrame = v269.special[v270.Name].finish.CFrame
                                }):Play();
                            end;
                            task.wait(tonumber(v270.duration.Value) * 0.2666666667);
                            if l_v274_0 then
                                l_v274_0:Disconnect();
                            end;
                            l_v274_0 = _G._services.RunService.RenderStepped:Connect(function(_) --[[ Line: 1235 ]]
                                if not v269.cutsceneSettings.LockOnTarget.Value then
                                    l_v274_0:Disconnect();
                                    if not v269.special:FindFirstChild(v270.Name) then
                                        task.spawn(function() --[[ Line: 1240 ]]
                                            l_v274_0 = _G._services.RunService.RenderStepped:Connect(function(_) --[[ Line: 1241 ]]
                                                if v280 and v280.Parent then
                                                    workspace.CurrentCamera.FieldOfView = tonumber(v269.cutsceneSettings.CameraFieldOfView.Value);
                                                    workspace.CurrentCamera.CFrame = CFrame.lookAt(l_v278_0.CFrame.Position, l_Value_0.CFrame.Position);
                                                    return;
                                                else
                                                    l_v274_0:Disconnect();
                                                    return;
                                                end;
                                            end);
                                        end);
                                    end;
                                    v134();
                                    v280:Destroy();
                                    task.wait(0.001);
                                    if l_LocalPlayer_0.PlayerGui and l_LocalPlayer_0.PlayerGui:FindFirstChild("UI") then
                                        l_LocalPlayer_0.PlayerGui.UI.Enabled = true;
                                    end;
                                    workspace.CurrentCamera.CameraType = Enum.CameraType.Custom;
                                    workspace.CurrentCamera.FieldOfView = tonumber(l_References_0.Profile.settings.Visual["Field of View"].Value);
                                    task.wait(0.25);
                                    _G._services.StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.Chat, true);
                                    return;
                                else
                                    workspace.CurrentCamera.FieldOfView = tonumber(v269.cutsceneSettings.CameraFieldOfView.Value);
                                    if not v269.special:FindFirstChild(v270.Name) then
                                        workspace.CurrentCamera.CFrame = CFrame.lookAt(l_v278_0.CFrame.Position, v269.cutsceneSettings.LockOnTarget.Value.CFrame.Position);
                                    end;
                                    return;
                                end;
                            end);
                        end;
                    end;
                    return;
                end;
            end, 
            offside = function(v287) --[[ Line: 1276 ]]
                if v39 then
                    return;
                else
                    v39 = true;
                    v134();
                    l_PlayerGui_0.replay.offside.viewport:ClearAllChildren();
                    for _, v289 in next, v287:GetChildren() do
                        if v289 and v289.Parent then
                            local v290 = v289:Clone();
                            v290.Parent = l_PlayerGui_0.replay.offside.viewport;
                            if v290.Name == "line" then
                                v290.Size = Vector3.new(0.001, v290.Size.Y, v290.Size.Z);
                            end;
                        end;
                    end;
                    local v291 = Instance.new("Camera", l_PlayerGui_0.replay.offside.viewport);
                    v291.FieldOfView = 70;
                    v291.CameraType = Enum.CameraType.Scriptable;
                    if l_PlayerGui_0.replay.offside.viewport.attacker.HumanoidRootPart.Position.Z <= 0 then
                        v291.CFrame = workspace.game.cameras.offsideHomeStart.CFrame;
                        local l_line_0 = l_PlayerGui_0.replay.offside.viewport.line;
                        l_line_0.Position = l_line_0.Position + Vector3.new(0, 0, 1, 0);
                        l_line_0 = v287.line;
                        l_line_0.Position = l_line_0.Position + Vector3.new(0, 0, 1, 0);
                        if l_PlayerGui_0.replay.offside.viewport.attacker.HumanoidRootPart.Position.X <= l_PlayerGui_0.replay.offside.viewport.defender.HumanoidRootPart.Position.X then
                            workspace.game.cameras.offsideHomeFinal.Position = Vector3.new(l_PlayerGui_0.replay.offside.viewport.attacker.HumanoidRootPart.Position.X - 50, workspace.game.cameras.offsideHomeFinal.Position.Y, v287.line.Position.Z + 0.001);
                        else
                            workspace.game.cameras.offsideHomeFinal.Position = Vector3.new(l_PlayerGui_0.replay.offside.viewport.defender.HumanoidRootPart.Position.X - 50, workspace.game.cameras.offsideHomeFinal.Position.Y, v287.line.Position.Z + 0.001);
                        end;
                    else
                        v291.CFrame = workspace.game.cameras.offsideAwayStart.CFrame;
                        local l_line_1 = l_PlayerGui_0.replay.offside.viewport.line;
                        l_line_1.Position = l_line_1.Position - Vector3.new(0, 0, 1, 0);
                        l_line_1 = v287.line;
                        l_line_1.Position = l_line_1.Position - Vector3.new(0, 0, 1, 0);
                        if l_PlayerGui_0.replay.offside.viewport.attacker.HumanoidRootPart.Position.X >= l_PlayerGui_0.replay.offside.viewport.defender.HumanoidRootPart.Position.X then
                            workspace.game.cameras.offsideAwayFinal.Position = Vector3.new(l_PlayerGui_0.replay.offside.viewport.attacker.HumanoidRootPart.Position.X + 50, workspace.game.cameras.offsideAwayFinal.Position.Y, v287.line.Position.Z - 0.001);
                        else
                            workspace.game.cameras.offsideAwayFinal.Position = Vector3.new(l_PlayerGui_0.replay.offside.viewport.defender.HumanoidRootPart.Position.X + 50, workspace.game.cameras.offsideAwayFinal.Position.Y, v287.line.Position.Z - 0.001);
                        end;
                    end;
                    l_PlayerGui_0.replay.offside.viewport.CurrentCamera = v291;
                    l_PlayerGui_0.replay.offside.Visible = true;
                    l_PlayerGui_0.replay.offside.label.Size = UDim2.new(0, 0, 0, 50);
                    local l_BoundingBox_0, v295 = l_PlayerGui_0.replay.offside.viewport.attacker:GetBoundingBox();
                    local v296 = v19._get(l_BoundingBox_0, v295);
                    local v297 = v296.CFrame * CFrame.new(-16, 4.5, 10) * CFrame.fromEulerAnglesXYZ(-0.375, -1, -0.33);
                    local _ = v296.CFrame * CFrame.new(30, 2, -0.16) * CFrame.fromEulerAnglesXYZ(0, 1.6, 0);
                    _G._services.TweenService:Create(v291, TweenInfo.new(2, Enum.EasingStyle.Circular, Enum.EasingDirection.Out), {
                        FieldOfView = 40, 
                        CFrame = v297
                    }):Play();
                    task.wait(2);
                    _G._services.TweenService:Create(l_PlayerGui_0.replay.offside.viewport.line, TweenInfo.new(0.7, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        Size = Vector3.new(v287.line.Size.X, v287.line.Size.Y, v287.line.Size.Z)
                    }):Play();
                    task.wait(0.3);
                    l_PlayerGui_0.replay.offside.label:TweenSize(UDim2.new(0, l_PlayerGui_0.replay.offside.label.main.AbsoluteSize.X, 0, l_PlayerGui_0.replay.offside.label.main.AbsoluteSize.Y), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.4, true);
                    task.wait(3);
                    if l_PlayerGui_0.replay.offside.viewport.attacker.HumanoidRootPart.Position.Z <= 0 then
                        _G._services.TweenService:Create(v291, TweenInfo.new(3.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            FieldOfView = 35, 
                            CFrame = workspace.game.cameras.offsideHomeFinal.CFrame
                        }):Play();
                    else
                        _G._services.TweenService:Create(v291, TweenInfo.new(3.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                            FieldOfView = 35, 
                            CFrame = workspace.game.cameras.offsideAwayFinal.CFrame
                        }):Play();
                    end;
                    task.wait(5);
                    l_PlayerGui_0.replay.gradient:TweenPosition(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Quint, 0.5, true);
                    task.wait(0.5);
                    v134();
                    l_PlayerGui_0.replay.offside.Visible = false;
                    l_PlayerGui_0.replay.offside.viewport:ClearAllChildren();
                    _G._services.StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.Chat, true);
                    task.wait(0.4);
                    v39 = false;
                    v4:send("replay");
                    return;
                end;
            end, 
            quickFoul = function(v299) --[[ Line: 1362 ]]
                v299.Detector.CanCollide = false;
                v4:send("partTeleport", v299.Player);
            end, 
            freeKick = function(v300, v301) --[[ Line: 1367 ]]
                task.spawn(function() --[[ Line: 1368 ]]
                    local v302 = v21.GetServerBallFolder();
                    if v302 then
                        for _, v304 in next, v302:GetChildren() do
                            if v304 and v304:IsA("BasePart") and v304:FindFirstChild("properties") and v304.properties:FindFirstChild("spawner") and v304.properties.spawner.Value == v301 then
                                v9.new(v300, v304);
                            end;
                        end;
                    end;
                end);
            end, 
            goalKick = function(v305, v306) --[[ Line: 1381 ]]
                task.spawn(function() --[[ Line: 1382 ]]
                    local v307 = v21.GetServerBallFolder();
                    if v307 then
                        for _, v309 in next, v307:GetChildren() do
                            if v309 and v309:IsA("BasePart") and v309:FindFirstChild("properties") and v309.properties:FindFirstChild("spawner") and v309.properties.spawner.Value == v306 then
                                v8.new(v305, v309);
                            end;
                        end;
                    end;
                end);
            end, 
            throwIn = function(v310, v311) --[[ Line: 1395 ]]
                task.spawn(function() --[[ Line: 1396 ]]
                    local v312 = v21.GetServerBallFolder();
                    if v312 then
                        for _, v314 in next, v312:GetChildren() do
                            if v314 and v314:IsA("BasePart") and v314:FindFirstChild("properties") and v314.properties:FindFirstChild("spawner") and v314.properties.spawner.Value == v311 then
                                v10.new(v310, v314);
                            end;
                        end;
                    end;
                end);
            end, 
            corner = function(v315, v316) --[[ Line: 1409 ]]
                task.spawn(function() --[[ Line: 1410 ]]
                    local v317 = v21.GetServerBallFolder();
                    if v317 then
                        for _, v319 in next, v317:GetChildren() do
                            if v319 and v319:IsA("BasePart") and v319:FindFirstChild("properties") and v319.properties:FindFirstChild("spawner") and v319.properties.spawner.Value == v316 then
                                v6.new(v315, v319);
                            end;
                        end;
                    end;
                end);
            end, 
            penalty = function(v320, v321) --[[ Line: 1423 ]]
                task.spawn(function() --[[ Line: 1424 ]]
                    local v322 = v21.GetServerBallFolder();
                    if v322 then
                        for _, v324 in next, v322:GetChildren() do
                            if v324 and v324:IsA("BasePart") and v324:FindFirstChild("properties") and v324.properties:FindFirstChild("spawner") and v324.properties.spawner.Value == v321 then
                                v7.new(v320, v324);
                            end;
                        end;
                    end;
                end);
            end, 
            shootout = function(v325, v326) --[[ Line: 1437 ]]
                task.spawn(function() --[[ Line: 1438 ]]
                    local v327 = v21.GetServerBallFolder();
                    if v327 then
                        for _, v329 in next, v327:GetChildren() do
                            if v329 and v329:IsA("BasePart") and v329:FindFirstChild("properties") and v329.properties:FindFirstChild("spawner") and v329.properties.spawner.Value == v326 then
                                v12.new(v325, v329);
                            end;
                        end;
                    end;
                end);
            end, 
            forceDisable = function(v330) --[[ Line: 1451 ]]
                l__root_0:SetAttribute("forceDisable", v330);
            end, 
            globalOverride = function(v331) --[[ Line: 1455 ]]
                l__root_0:SetAttribute("globalOverride", v331);
            end, 
            canSprint = function(v332) --[[ Line: 1459 ]]
                v49:SetAttribute("canSprint", v332);
            end, 
            advantageStart = function() --[[ Line: 1463 ]]
                l_PlayerGui_0.main.advantage.Visible = true;
                l_PlayerGui_0.main.advantage.bar.progress.Size = UDim2.new(0, 0, 1, 0);
                l_PlayerGui_0.main.advantage.bar.progress:TweenSize(UDim2.new(1, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Linear, 5, true);
                task.delay(5, function() --[[ Line: 1468 ]]
                    if l_PlayerGui_0.main.advantage.Visible then
                        l_PlayerGui_0.main.advantage.Visible = false;
                    end;
                end);
            end, 
            advantageEnd = function() --[[ Line: 1475 ]]
                l_PlayerGui_0.main.advantage.Visible = false;
            end, 
            updateCounter = function() --[[ Line: 1479 ]]
                local v333 = l_References_0.Main.event:WaitForChild(l_LocalPlayer_0.Name, 100);
                if v333:GetAttribute("quest1") then
                    l_Services_0.TweenService:Create(l_PlayerGui_0.main.event.quests.icons["1"], TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        BackgroundColor3 = Color3.fromRGB(85, 255, 127)
                    }):Play();
                end;
                if v333:GetAttribute("quest2") then
                    l_Services_0.TweenService:Create(l_PlayerGui_0.main.event.quests.icons["2"], TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        BackgroundColor3 = Color3.fromRGB(85, 255, 127)
                    }):Play();
                end;
                if v333:GetAttribute("quest3") then
                    l_Services_0.TweenService:Create(l_PlayerGui_0.main.event.quests.icons["3"], TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        BackgroundColor3 = Color3.fromRGB(85, 255, 127)
                    }):Play();
                end;
                l_PlayerGui_0.main.event.quests.progress.progress:TweenSize(UDim2.new((v333:GetAttribute("silvers") or 0) / 3, 0, 1, 0), Enum.EasingDirection.InOut, Enum.EasingStyle.Sine, 0.35, true);
                l_PlayerGui_0.main.event.counter.silvers.count.Text = tostring(v333:GetAttribute("silvers") or 0);
                l_PlayerGui_0.main.event.counter.shines.count.Text = tostring(v333:GetAttribute("shines") or 0);
            end, 
            shiftLock = function(v334) --[[ Line: 1522 ]]
                if not v334 then
                    l_MouseLockController_0:SetAttribute("forceDisable", true);
                    l__root_0:SetAttribute("disableMouseLock", true);
                    l_l_LocalPlayer_0_Mouse_0.Icon = "";
                    v35.Value = "";
                    return true;
                else
                    v35.Value = l_References_0.Profile.binds.Misc["Mouse Lock"].Value;
                    l_MouseLockController_0:SetAttribute("forceEnable", true);
                    l__root_0:SetAttribute("disableMouseLock", true);
                    l_l_LocalPlayer_0_Mouse_0.Icon = "";
                    return;
                end;
            end, 
            startPitchWear = function(v335, v336) --[[ Line: 1537 ]]
                if l_LocalPlayer_0 ~= v335 then
                    for _, v338 in next, v336 do
                        if v335.Character:FindFirstChild(v338) then
                            local v339 = v335.Character[v338];
                            local v340 = v335.Character.HumanoidRootPart.CFrame - v335.Character.HumanoidRootPart.CFrame.Position;
                            local v341 = l_References_0.Main.effects.wear:Clone();
                            v341.Parent = workspace.game.debug;
                            v341.Name = v335.Name .. "_wear";
                            v341.CFrame = CFrame.new((Vector3.new(v339.Position.X, 0.568, v339.Position.Z))) * v340;
                            v25[v339.Name .. "_update"] = l_Services_0.RunService.RenderStepped:Connect(function() --[[ Line: 1549 ]]
                                v341.attachment1.WorldPosition = Vector3.new(v339.Position.X, 0.371, v339.Position.Z);
                            end);
                        end;
                    end;
                end;
            end, 
            endPitchWear = function(v342) --[[ Line: 1557 ]]
                if l_LocalPlayer_0 ~= v342 then
                    v25:DoCleaning();
                    for _, v344 in next, workspace.game.debug:GetChildren() do
                        if v344.Name == v342.Name .. "_wear" then
                            task.delay(20, function() --[[ Line: 1563 ]]
                                local v345 = v22.new();
                                local l_NumberValue_0 = Instance.new("NumberValue");
                                l_NumberValue_0.Value = 0;
                                v345:GiveTask(l_NumberValue_0);
                                l_Services_0.TweenService:Create(l_NumberValue_0, TweenInfo.new(1, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                                    Value = 1
                                }):Play();
                                v345.tween = l_Services_0.RunService.RenderStepped:Connect(function() --[[ Line: 1572 ]]
                                    if v344:FindFirstChild("beam") then
                                        v344.beam.Transparency = NumberSequence.new({
                                            NumberSequenceKeypoint.new(0, l_NumberValue_0.Value), 
                                            NumberSequenceKeypoint.new(0.5, l_NumberValue_0.Value), 
                                            NumberSequenceKeypoint.new(1, l_NumberValue_0.Value)
                                        });
                                    end;
                                end);
                                task.wait(1.15);
                                v345:DoCleaning();
                                task.wait(1);
                                v344:Destroy();
                            end);
                        end;
                    end;
                end;
            end, 
            celebration = function(v347) --[[ Line: 1593 ]]
                if v347 == "start" then
                    v30.celebrations:SetAttribute("toggle", true);
                    return;
                else
                    v30.celebrations:SetAttribute("toggle", false);
                    return;
                end;
            end, 
            shutdown = function() --[[ Line: 1601 ]]
                l_References_0.PlayerGui.kick.Enabled = true;
                l_References_0.PlayerGui.kick.main.title.Text = "RECONNECTING";
                l_References_0.PlayerGui.kick.main.description.Text = "Migrating to latest update";
                l_Services_0.TweenService:Create(l_References_0.PlayerGui.kick.background, TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 0
                }):Play();
                task.wait(0.25);
                l_Services_0.TweenService:Create(l_References_0.PlayerGui.kick.main, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    GroupTransparency = 0, 
                    Position = UDim2.new(0.5, 0, 0.5, 0)
                }):Play();
                l_Services_0.RunService.RenderStepped:Connect(function() --[[ Line: 1609 ]]
                    l_Services_0.StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.All, false);
                end);
            end, 
            kick = function(v348) --[[ Line: 1614 ]]
                l_References_0.PlayerGui.kick.Enabled = true;
                l_References_0.PlayerGui.kick.main.description.Text = string.format("You have been kicked // %s", v348 or "Unspecified reason");
                l_Services_0.TweenService:Create(l_References_0.PlayerGui.kick.background, TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    ImageTransparency = 0
                }):Play();
                task.wait(0.25);
                l_Services_0.TweenService:Create(l_References_0.PlayerGui.kick.main, TweenInfo.new(0.2, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                    GroupTransparency = 0, 
                    Position = UDim2.new(0.5, 0, 0.5, 0)
                }):Play();
                l_Services_0.RunService.RenderStepped:Connect(function() --[[ Line: 1621 ]]
                    l_Services_0.StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.All, false);
                end);
                for _, v350 in next, l_Services_0.ReplicatedStorage:GetChildren() do
                    if v350:IsA("Folder") then
                        v350:Destroy();
                    end;
                end;
                for _, v352 in next, l_Services_0.AssetService:GetChildren() do
                    if v352 then
                        v352:Destroy();
                    end;
                end;
                for _, v354 in next, l_Services_0.MaterialService:GetChildren() do
                    if v354 then
                        v354:Destroy();
                    end;
                end;
                for _, v356 in next, workspace:GetChildren() do
                    if v356:IsA("Folder") then
                        v356:Destroy();
                    end;
                end;
            end, 
            alert = function() --[[ Line: 1650 ]]
                if not l_PlayerGui_0:FindFirstChild("Alert") then
                    local v357 = v22.new();
                    local v358 = l_References_0.Main.ui.alert:Clone();
                    v358.Parent = l_PlayerGui_0;
                    if l_Services_0.UserInputService.TouchEnabled then
                        v358.main.button.Text = "Tap to dismiss";
                    elseif l_Services_0.UserInputService.GamepadEnabled then
                        v358.main.button.Text = "Press A to dismiss";
                        v357.inputBegan = l_Services_0.UserInputService.InputBegan:Connect(function(v359, v360) --[[ Line: 1661 ]]
                            if (v360 or not v360) and v359.KeyCode == Enum.KeyCode.ButtonA then
                                l_References_0.Main.sounds.UI.Click:Play();
                                l_References_0.Main.sounds.UI.Alert:Stop();
                                v357:DoCleaning();
                            end;
                        end);
                    end;
                    l_References_0.Main.sounds.UI.Alert:Play();
                    v357:GiveTask(v358);
                    v357.mouseButton1Click = v358.main.button.MouseButton1Click:Connect(function() --[[ Line: 1673 ]]
                        l_References_0.Main.sounds.UI.Click:Play();
                        l_References_0.Main.sounds.UI.Alert:Stop();
                        v357:DoCleaning();
                    end);
                end;
            end, 
            marker = function(v361, v362) --[[ Line: 1681 ]]
                if l_LocalPlayer_0 ~= v361 and v361.Character and v361.Character:FindFirstChild("HumanoidRootPart") and v123(l_LocalPlayer_0, v361) then
                    for _, v364 in next, workspace.game.markers:GetChildren() do
                        if v364.Name == v361.Name then
                            v364:Destroy();
                        end;
                    end;
                    local v365 = l_References_0.Main.ui.marker:Clone();
                    local v366 = Vector3.new(v362.X, v365.PrimaryPart.Position.Y, v362.Z);
                    local l_Color_0 = v361.TeamColor.Color;
                    if v361.Team and string.find(v361.Team.Name, "Home") then
                        l_Color_0 = v16:getTeamColorFromTeam("Home");
                    elseif v361.Team and string.find(v361.Team.Name, "Away") then
                        l_Color_0 = v16:getTeamColorFromTeam("Away");
                    end;
                    v365.Template.Cross.Cross.ImageColor3 = l_Color_0;
                    v365.Beam.Beam.Color = ColorSequence.new(l_Color_0, l_Color_0);
                    v365.Config.Icon.Value = v18:get(v361.UserId);
                    v365.Config.MarkerColor.Value = l_Color_0;
                    v365.Config.Distance.Value = math.floor((v366 - v361.Character.HumanoidRootPart.Position).Magnitude + 0.5);
                    v365.Config.Position.Value = v365.PrimaryPart.Position;
                    v365.Parent = workspace.game.markers;
                    v365:SetPrimaryPartCFrame(CFrame.new(v366));
                    v365.Name = v361.Name;
                    v365.Config.Enabled.Value = true;
                    l_Services_0.Debris:AddItem(v365, 2);
                end;
            end, 
            lightning = function(v368) --[[ Line: 1718 ]]
                local v369 = Instance.new("Part", workspace.game.debug);
                v369.Size = Vector3.new(0.10000000149011612, 0.10000000149011612, 0.10000000149011612, 0);
                v369.Anchored = true;
                v369.CanCollide = false;
                v369.Locked = true;
                v369.Transparency = 1;
                v369.CFrame = CFrame.new(v368);
                local v370 = l_References_0.Main.effects.burn:Clone();
                v370.Parent = workspace.game.debug;
                v370.Position = Vector3.new(v368.X, 0.373, v368.Z);
                l_Services_0.Lighting.ColorCorrection.Brightness = 0.05;
                task.delay(0.125, function() --[[ Line: 1732 ]]
                    l_Services_0.Lighting.ColorCorrection.Brightness = 0;
                end);
                local v371 = Instance.new("Attachment", v369);
                v371.WorldPosition = v368 + Vector3.new(0, 200, 0, 0);
                local v372 = Instance.new("Attachment", v369);
                v372.WorldPosition = v368;
                local v373 = v13.new(v371, v372, 16);
                v373.AnimationSpeed = 20;
                v373.PulseSpeed = 10;
                v373.PulseLength = 10;
                v373.FadeLength = 0.25;
                v373.Color = Color3.fromRGB(255, 221, 221);
                local v374 = v14.new(v373);
                local v375 = v15.new(v368, 0.1, 10, Color3.fromRGB(255, 255, 255), Color3.fromRGB(255, 255, 255));
                if (v369.Position - workspace.CurrentCamera.CFrame.Position * Vector3.new(1, 0, 1, 0)).Magnitude <= 85 then
                    v5:load({
                        directory = v369, 
                        soundId = l_References_0.Main.sounds.Weather.Thunder["Lightning Close"].SoundId, 
                        rollOffMaxDistance = 500000, 
                        rollOffMinDistance = 50, 
                        volume = 1, 
                        play = true
                    });
                else
                    v5:load({
                        directory = v369, 
                        soundId = l_References_0.Main.sounds.Weather.Thunder["Lightning Far"].SoundId, 
                        rollOffMaxDistance = 50000, 
                        rollOffMinDistance = 50, 
                        volume = 1, 
                        play = true
                    });
                end;
                task.delay(0.2, function() --[[ Line: 1772 ]]
                    v373:Destroy();
                    v374:Destroy();
                    v375:Destroy();
                end);
                task.delay(5, function() --[[ Line: 1778 ]]
                    v369:Destroy();
                    l_Services_0.TweenService:Create(v370.SurfaceGui.ImageLabel, TweenInfo.new(10, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        ImageTransparency = 1
                    }):Play();
                    task.wait(10);
                    v370:Destroy();
                end);
            end, 
            levelUp = function(v376) --[[ Line: 1786 ]]
                if not v38 then
                    v38 = true;
                    l_References_0.Main.sounds.UI.Swipe:Play();
                    l_PlayerGui_0.main.levelUp.Visible = true;
                    l_PlayerGui_0.main.levelUp.level.TextTransparency = 1;
                    l_PlayerGui_0.main.levelUp.level.Text = tostring(v376);
                    l_PlayerGui_0.main.levelUp.level.Position = UDim2.new(0.5, 0, 1, 10);
                    l_PlayerGui_0.main.levelUp.label.Position = UDim2.new(0.5, -20, 0, 0);
                    _G._services.TweenService:Create(l_PlayerGui_0.main.levelUp.label, TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        Position = UDim2.new(0.5, 0, 0, 0)
                    }):Play();
                    _G._services.TweenService:Create(l_PlayerGui_0.main.levelUp.label.UIGradient, TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        Offset = Vector2.new(1, 0)
                    }):Play();
                    task.wait(0.25);
                    _G._services.TweenService:Create(l_PlayerGui_0.main.levelUp.level, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        TextTransparency = 0, 
                        Position = UDim2.new(0.5, 0, 1, -10)
                    }):Play();
                    task.wait(3);
                    _G._services.TweenService:Create(l_PlayerGui_0.main.levelUp.level, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        TextTransparency = 1, 
                        Position = UDim2.new(0.5, 0, 1, 10)
                    }):Play();
                    task.wait(0.25);
                    _G._services.TweenService:Create(l_PlayerGui_0.main.levelUp.label, TweenInfo.new(0.25, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        TextTransparency = 1
                    }):Play();
                    task.wait(0.25);
                    l_PlayerGui_0.main.levelUp.level.TextTransparency = 0;
                    l_PlayerGui_0.main.levelUp.level.Position = UDim2.new(0.5, 0, 1, -10);
                    l_PlayerGui_0.main.levelUp.label.Position = UDim2.new(0.5, 0, 0, 0);
                    l_PlayerGui_0.main.levelUp.label.TextTransparency = 0;
                    l_PlayerGui_0.main.levelUp.label.UIGradient.Offset = Vector2.new(-1, 0);
                    l_PlayerGui_0.main.levelUp.Visible = false;
                    v38 = false;
                end;
            end, 
            message = function(v377, v378) --[[ Line: 1820 ]]
                if not v37 then
                    v37 = true;
                    l_PlayerGui_0.main.message.label.Text = v377;
                    l_PlayerGui_0.main.message.label.UIGradient.Rotation = 0;
                    l_PlayerGui_0.main.message.label.UIGradient.Offset = Vector2.new(-1, 0);
                    l_PlayerGui_0.main.message.label.Size = UDim2.new(0, l_PlayerGui_0.main.message.AbsoluteSize.X, 0, l_PlayerGui_0.main.message.AbsoluteSize.Y);
                    _G._services.TweenService:Create(l_PlayerGui_0.main.message.label.UIGradient, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        Offset = Vector2.new(1, 0)
                    }):Play();
                    task.wait(v378 or 3.5);
                    l_PlayerGui_0.main.message.label.UIGradient.Offset = Vector2.new(-1, 0);
                    l_PlayerGui_0.main.message.label.UIGradient.Rotation = 180;
                    _G._services.TweenService:Create(l_PlayerGui_0.main.message.label.UIGradient, TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut), {
                        Offset = Vector2.new(1, 0)
                    }):Play();
                    task.wait(0.6);
                    l_PlayerGui_0.main.message.label.UIGradient.Offset = Vector2.new(-1, 0);
                    l_PlayerGui_0.main.message.label.UIGradient.Rotation = 0;
                    v37 = false;
                end;
            end, 
            takePrompt = function(v379) --[[ Line: 1842 ]]
                if not v43[v379.Name] and not l_References_0.Main.cards.red:FindFirstChild(l_LocalPlayer_0.Name) then
                    local v380 = v20.new(v379);
                    v43[v379.Name] = v380;
                end;
            end, 
            takeClear = function(v381) --[[ Line: 1849 ]]
                if v43[v381] then
                    v43[v381]:clear();
                    v43[v381] = nil;
                end;
            end, 
            bindMovement = function(v382) --[[ Line: 1856 ]]
                if v382 == "freeze" then
                    local l_l_PlayerModule_0_Controls_0 = l_PlayerModule_0:GetControls();
                    if l_l_PlayerModule_0_Controls_0 then
                        l_l_PlayerModule_0_Controls_0:Disable();
                    end;
                    l_LocalPlayer_0.Character:SetAttribute("freezeMovement", true);
                    _G._services.ContextActionService:BindAction("freezeMovement", function() --[[ Line: 1867 ]]
                        return Enum.ContextActionResult.Sink;
                    end, false, unpack(Enum.PlayerActions:GetEnumItems()));
                    return;
                else
                    local l_l_PlayerModule_0_Controls_1 = l_PlayerModule_0:GetControls();
                    if l_l_PlayerModule_0_Controls_1 then
                        l_l_PlayerModule_0_Controls_1:Enable();
                    end;
                    l_LocalPlayer_0.Character:SetAttribute("freezeMovement", nil);
                    _G._services.ContextActionService:UnbindAction("freezeMovement");
                    return;
                end;
            end, 
            moveTo = function(v385) --[[ Line: 1883 ]]
                local v386 = v22.new();
                l_LocalPlayer_0.Character.Humanoid:SetAttribute("moveTo", true);
                l_LocalPlayer_0.Character.Humanoid:MoveTo(v385);
                v386.moveToFinished = l_LocalPlayer_0.Character.Humanoid.MoveToFinished:Connect(function(v387) --[[ Line: 1889 ]]
                    if v387 == true then
                        v386:DoCleaning();
                        return true;
                    else
                        return;
                    end;
                end);
                for _ = 1, 10 do
                    if v386.moveToFinished then
                        task.wait(0.5);
                    else
                        break;
                    end;
                end;
                if v386.moveToFinished then
                    v386:DoCleaning();
                    return true;
                else
                    return;
                end;
            end, 
            trip = function() --[[ Line: 1910 ]]
                v32:SetAttribute("Ragdoll", true);
                task.wait(math.random(1.5, 3));
                v32:SetAttribute("Ragdoll", false);
            end, 
            pull = function() --[[ Line: 1916 ]]
                v49:SetAttribute("canSprint", false);
                l_LocalPlayer_0.Character.Humanoid.WalkSpeed = l_Services_0.StarterPlayer.CharacterWalkSpeed - 5;
                task.wait(math.random(2, 3));
                v49:SetAttribute("canSprint", true);
                l_LocalPlayer_0.Character.Humanoid.WalkSpeed = l_Services_0.StarterPlayer.CharacterWalkSpeed;
            end, 
            ragdoll = function() --[[ Line: 1926 ]]
                v32:SetAttribute("Ragdoll", true);
            end, 
            unragdoll = function() --[[ Line: 1930 ]]
                v32:SetAttribute("Ragdoll", false);
            end, 
            handshake = function(v389) --[[ Line: 1934 ]]
                local l_Character_0 = l_LocalPlayer_0.Character;
                if not l_Character_0 then
                    for _ = 1, 60 do
                        if l_LocalPlayer_0.Character then
                            l_Character_0 = l_LocalPlayer_0.Character;
                        end;
                        task.wait(1);
                    end;
                    if not l_Character_0 then
                        v116();
                    end;
                end;
                local v392 = {};
                for _, v394 in pairs(l_LocalPlayer_0.Character:GetChildren()) do
                    if v392[v394.Name] then
                        v4:send("kick", "ur not slick lil bro :joy:");
                        v116();
                    end;
                    if v394.Name == "Head" or v394.Name == "Collide" or v394.Name == "LeftBoot" or v394.Name == "RightBoot" then
                        local l_Magnitude_0 = v394.Size.Magnitude;
                        v394.Size = v394.Size - Vector3.new(0.0010000000474974513, 0.0010000000474974513, 0.0010000000474974513, 0);
                        if v394.Size.Magnitude == l_Magnitude_0 then
                            v4:send("kick", "Hitbox Tampering");
                            v116();
                        end;
                        v394.Size = v394.Size + Vector3.new(0.0010000000474974513, 0.0010000000474974513, 0.0010000000474974513, 0);
                    end;
                    if v394:IsA("BasePart") then
                        for _, v397 in pairs(v44) do
                            if string.match(v394.Name, v397) then
                                local v398 = {
                                    v394.Size.X, 
                                    v394.Size.Y, 
                                    v394.Size.Z
                                };
                                v392[v394.Name] = v398;
                            end;
                        end;
                    end;
                end;
                if l_LocalPlayer_0.Character.Parent ~= workspace then
                    v392 = nil;
                end;
                return l_Services_0.HttpService:JSONEncode({
                    key = v389, 
                    WalkSpeed = l_LocalPlayer_0.Character.Humanoid.WalkSpeed, 
                    limbSizes = v392
                });
            end
        };
        for v400, v401 in next, v399 do
            v4:add(v400, v401);
        end;
    end
};
