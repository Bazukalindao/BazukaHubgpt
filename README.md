while true do
    local player = game.Players.LocalPlayer
    local level = player.Data.Level.Value
    if level < 2550 then
        -- Aqui, o script procuraria pela missão mais próxima para o nível atual
        local quest = getBestQuestForLevel(level)
        -- Aceita a missão automaticamente
        acceptQuest(quest)
        
        -- Encontra os inimigos necessários para completar a missão
        local enemies = findEnemies(quest)
        
        -- Ataca os inimigos até completar a missão
        for _, enemy in pairs(enemies) do
            autoAttack(enemy)
        end
        
        -- Completa a missão e recebe a recompensa
        completeQuest(quest)
    else
        print("Nível máximo atingido!")
        break
    end
    wait(1)  -- Adiciona uma pausa para evitar sobrecarregar o servidor
end

-- Funções auxiliares que precisariam ser criadas para automatizar o processo
function getBestQuestForLevel(level)
    -- Lógica para encontrar a melhor missão com base no nível
end

function acceptQuest(quest)
    -- Lógica para aceitar a missão
end

function findEnemies(quest)
    -- Lógica para encontrar os inimigos necessários
end

function autoAttack(enemy)
    -- Lógica para atacar os inimigos automaticamente
end

function completeQuest(quest)
    -- Lógica para completar a missão e pegar a recompensa
end
