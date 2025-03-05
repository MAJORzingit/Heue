-- ══════════════════════════════════════
--               Core				
-- ══════════════════════════════════════
local Find = function(Table) 
    for i, v in pairs(Table or {}) do 
        if typeof(v) == 'table' then return v end 
    end 
end

local Options = Find(({...})) or {
	Keybind = 'Home',

	Language = {
		UI = 'pt-br',
		Words = 'pt-br'
	},

	Experiments = {},

	Tempo = 1, 0,
	Rainbow = false,
}

local Version = '1.5'
local Parent = gethui() or game:GetService('CoreGui')
local require = function(Name)
	return loadstring(game:HttpGet(('https://raw.githubusercontent.com/thzx7hz/AutoJJs/main/%s.lua'):format(Name)))()
end

-- ══════════════════════════════════════
--              Services				
-- ══════════════════════════════════════
local TweenService = game:GetService('TweenService')
local Players = game:GetService('Players')
local LP = Players.LocalPlayer

-- ══════════════════════════════════════
--              Modules				
-- ══════════════════════════════════════
local UI = require("UI")
local Notification = require("Notification")
local Extenso = require("Modules/Extenso")
local Character = require("Modules/Character")
local RemoteChat = require("Modules/RemoteChat")
local Request = require("Modules/Request")

-- ══════════════════════════════════════
--  	        Constants				
-- ══════════════════════════════════════
local Char = Character.new(LP)
local UIElements = UI.UIElements
-- O restante permanece inalterado...
