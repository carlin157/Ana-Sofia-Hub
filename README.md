-- biblioteca
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

-- janela principal

local Window = Fluent:CreateWindow({
    Title = "Ana Sofia Hub" .. Fluent.Version,
    SubTitle = "by Carl",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 460),
    Acrylic = true, -- The blur may be detectable, setting this to false disables blur entirely
    Theme = "Dark",
    MinimizeKey = Enum.KeyCode.LeftControl -- Used when theres no MinimizeKeybind
})

--Fluent provides Lucide Icons https://lucide.dev/icons/ for the tabs, icons are optional
local Tabs = {
    Main = Window:AddTab({ Title = "Scripts", Icon = "" }),
    Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

-- botao

Tabs.MainSection:NewButton("NAME ESP", "Q to toggle on and off", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Exunys/ESP-Script/main/ESP.lua"))()
end)

Tabs.Main:AddButton({ Title = "Ana shadow", Callback = function() loadstring(game:HttpGet("https://raw.githubusercontent.com/xscripts7/XScripts/refs/heads/XScript/ShadowHub", true))() end })
Tabs.Main:AddButton({ Title = "Ana dopamina", Callback = function() loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Dopamina-Hub-17894"))() end })
Tabs.Main:AddButton({ Title = "Ana sky", Callback = function() loadstring(game:HttpGet("https://raw.githubusercontent.com/yofriendfromschool1/Sky-Hub/main/SkyHub.txt"))()end })
Tabs.Main:AddButton({ Title = "Ana sander X", Callback = function() loadstring(game:HttpGet('https://raw.githubusercontent.com/kigredns/SanderXV4.2.2/refs/heads/main/New.lua'))() end })
Tabs.Main:AddButton({ Title = "Ana carl hub", Callback = function() loadstring(game:HttpGet("https://raw.githubusercontent.com/carlosdaniel987/Carlos/refs/heads/main/README.md"))() end })

-- notificacao

    Fluent:Notify({
        Title = "Notification",
        Content = "This is a notification",
        SubContent = "SubContent", -- Optional
        Duration = 5 -- Set to nil to make the notification not disappear
    })

-- paragrafo

    Tabs.Main:AddParagraph({
        Title = "Executado",
        Content = "Script executado com sucesso"
    })

-- paragrafo

    Tabs.Main:AddParagraph({
        Title = "Key do Dopamina",
        Content = "Graciasporseleccionarnos"
    })
    
    -- paragrafo

    Tabs.Main:AddParagraph({
        Title = "Key do Shadow",
        Content = "</>FaseTesting"
    })
