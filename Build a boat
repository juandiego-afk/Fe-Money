-- // Script: Auto-Coins (Build A Boat for Treasure)
-- // Ejecutar con Delta Executor
-- // Recoge monedas automáticamente cada 5 segundos

print("🔄 Auto-Coins activado cada 5 segundos...")

-- Variables
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Verificar si el RemoteEvent existe
local remoteEvent = ReplicatedStorage:FindFirstChild("g_") or ReplicatedStorage:WaitForChild("g_")

if not remoteEvent then
    warn("❌ No se encontró el RemoteEvent 'g_'")
    return
end

-- Bucle infinito para recoger monedas
while true do
    wait(5) -- Espera 5 segundos

    pcall(function()
        -- Simulamos que recogemos una moneda
        -- El RemoteEvent 'g_' suele manejar la recogida
        remoteEvent:FireServer("c", "Coin")
        print("💰 Moneda recogida automáticamente")
    end)
end
