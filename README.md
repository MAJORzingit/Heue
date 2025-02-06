-- ══════════════════════════════════════
--               Core				
-- ══════════════════════════════════════
local Find = function(Table) for i, v in pairs(Table or {}) do if typeof(v) == 'table' then return v end; end; end
local Options = Find(({...})) or {
	Keybind = 'Home',

	Language = {
		UI = 'pt-br',
		Words = 'pt-br'
	},

	Experiments = { },

	Tempo = 1, 0,
	Rainbow = true,
}
local Version = '1.5'
local Parent = gethui() or game:GetService('CoreGui');
local require = function(Name)
	return loadstring(game:HttpGet(('https://raw.githubusercontent.com/thzx7hz/AutoJJs/main/%s.lua'):format(Name)))()
end

-- ══════════════════════════════════════
--              Services				
-- ══════════════════════════════════════
local TweenService = game:GetService('TweenService')
local Players = game:GetService('Players')
local LP = Players.LocalPlayer

-- Funções de interface
local function SetInterfaceColors()
	TweenService:Create(UIElements["Slide"], TweenInfo.new(0.3), { BackgroundColor3 = Color3.fromRGB(211, 211, 211) }):Play() -- Cinza claro
end

SetInterfaceColors()
