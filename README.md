local player = game.Players.LocalPlayer

-- Função para usar uma habilidade específica
local function useSkill(skill)
    game:GetService("ReplicatedStorage").Remotes.Combat:FireServer(skill)
end

-- Função para atacar inimigos
local function attackEnemy(enemy)
    -- Ataca com habilidades da Blox Fruit
    useSkill("Z") -- Primeira habilidade da fruta
    wait(1)
    useSkill("X") -- Segunda habilidade da fruta
    wait(1)
    useSkill("C") -- Terceira habilidade da fruta

    -- Usa a espada
    useSkill("SwordSlash")
    wait(1)

    -- Usa a arma de fogo
    useSkill("GunShoot")
    wait(1)

    -- Usa combate corpo a corpo
    useSkill("CombatPunch")
    wait(1)
end

-- Script principal de caça de bounty
while true do
    for _, target in pairs(game.Players:GetPlayers()) do
        if target.Team ~= player.Team and target.Character and target.Character:FindFirstChild("Humanoid") and target.Character.Humanoid.Health > 0 then
            -- Move-se para o jogador alvo
            player.Character.HumanoidRootPart.CFrame = target.Character.HumanoidRootPart.CFrame
            wait(0.5) -- Espera para se aproximar

            -- Ataca o alvo com todas as habilidades
            attackEnemy(target.Character.Humanoid)

            -- Continua atacando até derrotar o alvo
            while target.Character.Humanoid.Health > 0 do
                attackEnemy(target.Character.Humanoid)
                wait(0.5)
            end
        end
    end
    wait(3) -- Espera 3 segundos antes de procurar outro alvo
end
