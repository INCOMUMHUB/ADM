# ADM--[=[
 d888b  db    db d888888b      .d888b.      db      db    db  .d8b.  
88' Y8b 88    88   `88'        VP  `8D      88      88    88 d8' `8b 
88      88    88    88            odD'      88      88    88 88ooo88 
88  ooo 88    88    88          .88'        88      88    88 88~~~88 
88. ~8~ 88b  d88   .88.        j88.         88booo. 88b  d88 88   88    @uniquadev
 Y888P  ~Y8888P' Y888888P      888888D      Y88888P ~Y8888P' YP   YP  CONVERTER 

designed using localmaze gui creator
]=]

-- Instances: 8 | Scripts: 0 | Modules: 1 | Tags: 1
local CollectionService = game:GetService("CollectionService");
local G2L = {};

-- Players.darkizinho9910.PlayerGui.ScreenGui
G2L["ScreenGui_1"] = Instance.new("ScreenGui", game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui"));
G2L["ScreenGui_1"]["ZIndexBehavior"] = Enum.ZIndexBehavior.Sibling;

-- Tags
CollectionService:AddTag(G2L["ScreenGui_1"], [[main]]);

-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame
G2L["Frame_2"] = Instance.new("Frame", G2L["ScreenGui_1"]);
G2L["Frame_2"]["BorderSizePixel"] = 0;
G2L["Frame_2"]["BackgroundColor3"] = Color3.fromRGB(75, 75, 75);
G2L["Frame_2"]["Size"] = UDim2.new(0, 174, 0, 194);
G2L["Frame_2"]["Position"] = UDim2.new(0, 654, 0, 16);


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.UICorner
G2L["UICorner_3"] = Instance.new("UICorner", G2L["Frame_2"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextBox2
G2L["TextBox2_4"] = Instance.new("TextBox", G2L["Frame_2"]);
G2L["TextBox2_4"]["CursorPosition"] = -1;
G2L["TextBox2_4"]["Name"] = [[TextBox2]];
G2L["TextBox2_4"]["BorderSizePixel"] = 0;
G2L["TextBox2_4"]["TextWrapped"] = true;
G2L["TextBox2_4"]["BackgroundColor3"] = Color3.fromRGB(193, 193, 193);
G2L["TextBox2_4"]["ClipsDescendants"] = true;
G2L["TextBox2_4"]["Size"] = UDim2.new(0, 138, 0, 20);
G2L["TextBox2_4"]["Position"] = UDim2.new(0, 18, 0, 54);
G2L["TextBox2_4"]["Text"] = [[KICK]];
G2L["TextBox2_4"]["SelectionGroup"] = true;


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextBox2.ModuleScript
G2L["ModuleScript_5"] = Instance.new("ModuleScript", G2L["TextBox2_4"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextBox2.UICorner
G2L["UICorner_6"] = Instance.new("UICorner", G2L["TextBox2_4"]);



-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextBox
G2L["TextBox_7"] = Instance.new("TextBox", G2L["Frame_2"]);
G2L["TextBox_7"]["CursorPosition"] = -1;
G2L["TextBox_7"]["BorderSizePixel"] = 0;
G2L["TextBox_7"]["TextWrapped"] = true;
G2L["TextBox_7"]["BackgroundColor3"] = Color3.fromRGB(161, 161, 161);
G2L["TextBox_7"]["ClipsDescendants"] = true;
G2L["TextBox_7"]["Size"] = UDim2.new(0, 176, 0, 48);
G2L["TextBox_7"]["Text"] = [[PAINEL ADMIN]];


-- Players.darkizinho9910.PlayerGui.ScreenGui.Frame.TextBox.UICorner
G2L["UICorner_8"] = Instance.new("UICorner", G2L["TextBox_7"]);



-- Require G2L wrapper


G2L_MODULES[G2L["ModuleScript_5"]] = {
Closure = function()
    local script = G2L["ModuleScript_5"];
	
	local KickModule = require(script:WaitForChild("KickModule"))	
	local KickModule = require(script:WaitForChild("KickModule"))	
	local Players = game:GetService("Players")	
	local kickReason = "This is a test" -- This would be your kick reason, the "You were kicked for:" is in the reason by default	
	local HasKickSound = true -- This chooses whether you want a kick sound that plays on the player's client, change this to false if you don't want any sound	
	
	-- HasKickSound = true (This would play a sound on the player's client)	
	-- HasKickSound = false (This wouldn't play anything)	
	
	Players.PlayerAdded:Connect(function(Plr) -- Plr = Player To Kick	
	KickModule.kick(Plr,kickReason,HasKickSound)	
	end)	
end;
};

return G2L["ScreenGui_1"], require;
