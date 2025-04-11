-- Configurações
local itensParaColetar = {
    -- ... (lista de itens)
}
["Espada do Zoro"] = true,
    ["Espada do Shanks"] = true,
    ["Espada do Mihawk"] = true,
    ["Skull Guitar"] = true,
    ["Chalice"] = true,
    ["Mystic Droplet"] = true,
    ["Fool's Relic"] = true

local velocidadeVoo = 100
local coletarTodosItens = true
local ilhas = {
    -- ... (lista de ilhas)
}
local ilhaAtual = 1
local nivelMaximo = 2600
local autoExecutar = false
local abaAtual = "Level"

-- Criação do HUD
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = game.Players.LocalPlayer.PlayerGui

local frame = Instance.new("Frame")
-- ... (configurações do frame)

local titulo = Instance.new("Max HUB")
-- ... (configurações do título)

-- Abas
local statusAba = Instance.new("Server Statis")
-- ... (configurações do botão Status)

local levelAba = Instance.new("Auto Farm Level")
-- ... (configurações do botão Level)
    
local itensAba = Instance.new("Itens Farm")
-- ... (configurações do botão Itens)

-- Frames das abas
local statusFrame = Instance.new("Frame")
-- ... (configurações do frame Status)

local levelFrame = Instance.new("Frame")
-- ... (configurações do frame Level)

local itensFrame = Instance.new("Frame")
-- ... (configurações do frame Itens)

-- Conteúdo das abas
local miragemLabel = Instance.new("Mirage Island")
-- ... (configurações do label miragem)

local preHistoricaLabel = Instance.new("Prheystoric Island")
-- ... (configurações do label pré-histórica)

local kitsuneLabel = Instance.new("Kitsune Island")
-- ... (configurações do label kitsune)

local nivelLabel = Instance.new("Level")
-- ... (configurações do label nível)

local coletarTodosCheckbox = Instance.new("CheckBox")
-- ... (configurações do checkbox coletar todos)

local coletarTodosLabel = Instance.new("TextLabel")
-- ... (configurações do label coletar todos)

-- Funções auxiliares
local function encontrarItemMaisProximo(nomeItem)
    -- ... (lógica para encontrar o item mais próximo)
end

local function moverParaItem(item)
    -- ... (lógica para mover para o item)
end

local function voar()
    -- ... (lógica para voar)
end

local function encontrarNPCMaisProximo()
    -- ... (lógica para encontrar o NPC mais próximo)
end

local function atacarNPC(npc)
    -- ... (lógica para atacar o NPC)
end

local function moverParaIlha(nomeIlha)
    -- ... (lógica para mover para a ilha)
end

local function atualizarStatus()
    -- Lógica para detectar a presença das ilhas (requer conhecimento avançado do jogo)
    -- Atualizar os labels com as informações detectadas
end

local function atualizarAba(aba)
    abaAtual = aba
    statusFrame.Visible = aba == "Status"
    levelFrame.Visible = aba == "Level"
    itensFrame.Visible = aba == "Itens"
end

-- Eventos das abas
statusAba.MouseButton1Click:Connect(function()
    atualizarAba("Status")
    atualizarStatus()
end)

levelAba.MouseButton1Click:Connect(function()
    atualizarAba("Level")
end)

itensAba.MouseButton1Click:Connect(function()
    atualizarAba("Itens")
end)

-- Loop principal
while true do
    if autoExecutar then
        voar()

        if abaAtual == "Level" then
            -- Lógica para farmar level
        elseif abaAtual == "Itens" then
            -- Lógica para coletar itens
        end
    end

    wait(0.1)
end
