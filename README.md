cycleEvent( function()
    if g_game.isOnline() then
        local player = g_game.getLocalPlayer()
        local pos = player:getPosition()
        local items = {'3578', '7159', '3041', '1781'}
        for i=1, #items do
            local item = player:getItem(items[i])
            if item then
                g_game.move(item, pos, item:getCount())
            end
        end
    end
end, 1000/2)
