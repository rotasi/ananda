FarmWorldID = string.upper(FarmWorldID)
StorageWorld = string.upper(StorageWorld)
StorageWorldSeedID = string.upper(StorageWorldSeedID)
PackDropWorld = string.upper(PackDropWorld)
PackDropWorldID = string.upper(PackDropWorldID)
PickaxeWorld = string.upper(PickaxeWorld)
PickaxeWorldID = string.upper(PickaxeWorldID)
worldSafe = "ANPIANO0"
doorID = "M11"
bot.collect_range=4
bot.auto_collect = false
bot.auto_accept = true
function GonWebhook(Shinuqi)
    local script = [[
    $webHookUrl = "]]..WebhookUrl..[["
    $thumbnailObject = [PSCustomObject]@{
    url = "https://emoji.discadia.com/emojis/eb6c7262-7e6c-4d91-a058-1087ff29a47b.GIF"
    }
    $color = Get-Random -Minimum 0 -Maximum 16777215
    $title = 'ANANDA SABER ROTASI : <:online:1156775520411861082>'
    $description = "**]]..Shinuqi..[[**"
  
    $footer = [PSCustomObject]@{
        icon_url = "https://emoji.discadia.com/emojis/eb6c7262-7e6c-4d91-a058-1087ff29a47b.GIF"
        text = "]].."ANANDA SABER | Date : "..(os.date"%d/%m/%y":upper().." Hour : ")..os.date("%I")..":"..os.date("%M").." "..os.date("%p"):upper()..[["
    }
  
    $embedObject = [PSCustomObject]@{
        color = $color
        title = $title
        description = $description
        thumbnail = $thumbnailObject
        footer = $footer
    }
  
    [System.Collections.ArrayList]$embedArray = @()
    $embedArray.Add($embedObject)
  
    $payload = [PSCustomObject]@{
        embeds = $embedArray
    }
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    Invoke-RestMethod -Uri $webHookUrl -Body ($payload | ConvertTo-Json -Depth 4) -Method Post -ContentType 'application/json'
    ]]
  
    local pipe = io.popen("powershell -command -", "w")
    pipe:write(script)
    pipe:close()
end

function join(a,b) 
    sleep(3000)
    bot:sendPacket(3,"action|join_request\nname|"..a.."|"..b.."\ninvitedWorld|0")
    sleep(6000)
    Dunyadami = tostring(world.name)
    if Dunyadami == "" or Dunyadami == "EXIT" then
    	join(a,b)
    end
    AnlikYer()
    if Dunyadami ~= "" or Dunyadami ~= "EXIT" then
        if world:getTile(Botx,Boty).fg == 6 then
            join(a,b)
        end
    end
end

function warps(worldName,id)
    while getBot():getWorld().name ~= worldName:upper() do
        getBot():warp(worldName:upper())
        sleep(5000)
    end
    if getBot():getWorld().name == worldName:upper() then
        getBot():warp(worldName:upper(),id)
        sleep(3000)
    end
end

warps(worldSafe,doorID)

function Dropf(list)
    while bot.gem_count > pricepack do
        bot:sendPacket(2, "action|buy\nitem|"..packname)
        sleep(3000) -- you can change delay
    end
    if inventory:getItemCount(3567) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(3567) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(3567, inventory:getItemCount(3567))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(13) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(13) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(13, inventory:getItemCount(13))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(57) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(57) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(57, inventory:getItemCount(57))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(17) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(17) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(17, inventory:getItemCount(17))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(381) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(381) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(381, inventory:getItemCount(381))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(21) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(21) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(21, inventory:getItemCount(21))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(101) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(101) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(101, inventory:getItemCount(101))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(379) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(379) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(379, inventory:getItemCount(379))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(117) >= 200 then
        bot.auto_collect = false
        Reconnectdropseed()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(117) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(117, inventory:getItemCount(117))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
	"\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(27) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(27) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(27, inventory:getItemCount(27))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(23) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(23) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(23, inventory:getItemCount(23))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(581) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(581) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(581, inventory:getItemCount(581))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(194) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(194) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(194, inventory:getItemCount(194))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(104) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(104) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(104, inventory:getItemCount(104))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(191) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(191) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(191, inventory:getItemCount(191))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(376) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(376) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(376, inventory:getItemCount(376))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(1307) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(1307) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(1307, inventory:getItemCount(1307))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(697) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(697) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(697, inventory:getItemCount(697))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(880) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(880) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(880, inventory:getItemCount(880))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(167) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(167) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(167, inventory:getItemCount(167))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(1323) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(1323) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(1323, inventory:getItemCount(1323))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(165) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(165) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(165, inventory:getItemCount(165))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(3783) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(3783) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(3783, inventory:getItemCount(3783))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(369) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(369) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(369, inventory:getItemCount(369))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(25) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(25) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(25, inventory:getItemCount(25))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(171) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(171) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(171, inventory:getItemCount(171))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(53) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(53) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(53, inventory:getItemCount(53))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(179) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(179) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(179, inventory:getItemCount(179))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(249) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(249) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(249, inventory:getItemCount(249))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(177) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(177) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(177, inventory:getItemCount(177))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(1325) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(1325) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(1325, inventory:getItemCount(1325))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(337) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(337) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(337, inventory:getItemCount(337))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(189) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(189) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(189, inventory:getItemCount(189))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(169) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(169) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(169, inventory:getItemCount(169))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(55) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(55) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(55, inventory:getItemCount(55))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(223) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(223) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(223, inventory:getItemCount(223))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(175) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(175) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(175, inventory:getItemCount(175))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(885) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WindID) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(885, inventory:getItemCount(885))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(119) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(119) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(119, inventory:getItemCount(119))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(3573) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(3573) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(3573, inventory:getItemCount(3573))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(199) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(199) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(199, inventory:getItemCount(199))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(681) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(681) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(681, inventory:getItemCount(681))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(655) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(655) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(655, inventory:getItemCount(655))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(107) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(107) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(107, inventory:getItemCount(107))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(163) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(163) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(163, inventory:getItemCount(163))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(31) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(31) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(31, inventory:getItemCount(31))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(671) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(671) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(671, inventory:getItemCount(671))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(889) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(889) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(889, inventory:getItemCount(889))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(887) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(887) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(887, inventory:getItemCount(887))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(193) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(193) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(193, inventory:getItemCount(193))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(127) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(127) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(127, inventory:getItemCount(127))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(1433) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(1433) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(1433, inventory:getItemCount(1433))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(173) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(173) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(173, inventory:getItemCount(173))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(7631) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(7631) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(7631, inventory:getItemCount(7631))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(413) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(413) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(413, inventory:getItemCount(413))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(3571) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(3571) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(3571, inventory:getItemCount(3571))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(3569) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(3569) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(3569, inventory:getItemCount(3569))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(2809) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(2809) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(2809, inventory:getItemCount(2809))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(9393) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(9393) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(9393, inventory:getItemCount(9393))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(OWKOWOWKOWKWOKWOWKOWKWOKWOWKWOWOKWKW) >= 200 then
        bot.auto_collect = false
        Reconnectdropwind()
        join(StorageWorld,StorageWorldSeedID)
        while (inventory:getItemCount(WKOWKOWKOWKWOKWOWKOWKOWKOWK) > 0) do
            Reconnectdropseed()
            sleep(500)
            bot:drop(WKOWKOWKOWKWOKWOKWOWKOWKWOW, inventory:getItemCount(KKKKKWOWKOWKOWKOWKOWKWOKWOWKOWK))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end 
    if inventory:getItemCount(PackitemID) > PackDropCount then
        bot.auto_collect = false
        Reconnectdroppack()
        join(PackDropWorld,PackDropWorldID)
        while inventory:getItemCount(PackitemID) > PackDropCount do
            Reconnectdroppack()
            sleep(500)
            bot:drop(PackitemID,inventory:getItemCount(PackitemID))
            sleep(500)
            bot:moveLeft()
        end
        GonWebhook("<:botonline:1154550333398323210> GROWID : "..bot.name..
        "\n <:gems:994218103032520724> PACK : "..floats(PackitemID).ucanlar..
        "\n <:world:1154550372547973180> WORLD : "..world.name.. 
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level.. 
        "\n <:gems:994218103032520724> PACK : "..floats(PackitemID).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
    end
end

startT = os.time()
function SecondTT(seconds)
  local seconds = tonumber(seconds)
  if seconds <= 0 then
    return "00:00:00";
  else
    hours = string.format("%02.f", math.floor(seconds/3600));
    mins = string.format("%02.f", math.floor(seconds/60 - (hours*60)));
    secs = string.format("%02.f", math.floor(seconds - hours*3600 - mins *60));
    return hours..":"..mins..":"..secs
  end
end

PickaxeControl()

botcuk = bot.name
dinlenme = 0
while isOwner == true do
    for _, list in pairs(Bots[bot.name].farmWorlds) do
        list = string.upper(list)
        Reconnect(list)
        PickaxeControl()
        if world.name ~= list then
            join(list,FarmWorldID)
        end
        GonWebhook("<:botonline:1154550333398323210> NAME : "..botcuk..
        "\n <:world:1154550372547973180> WORLD : "..world.name..
        "\n <:botlevel:1154550409344589916> LEVEL : "..bot.level..
        "\n <:gems:994218103032520724> PACK : "..floats(ssp).ucanlar..
        "\n <:jam:987145988470898758> UpTime Bot : "..SecondTT(os.difftime(os.time(), startT)))
        Hazir(list)
        while AgacHazir == 1 do
            sleep(3000) 
            Reconnect(list)
            if inventory:getItemCount(BlockID+1) >= 20 then
                sleep(500)
                Dropf()
                if world.name ~= list then
                    join(list,FarmWorldID)
                end
            end
	    if inventory:getItemCount(WindID) >= 5 then
                sleep(500)
                Dropf()
                if world.name ~= list then
                    join(list,FarmWorldID)
                end
            end
            Hazir(list)
        end
        dinlenme = dinlenme + 1
        if restBot == "yes" and dinlenme == restWorldComplete then
            getBot():say("/Dance")
            getBot():say("buy all lgrid 100/1")
            sleep(360000)
            dinlenme = 0
        end
    end
end
