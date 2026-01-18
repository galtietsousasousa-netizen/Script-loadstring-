# Script-loadstring--- Menu simples em Lua (educacional)

local Menu = {
    aberto = true,
    funcoes = {
        desync = false,
        speed = false,
        fly = false
    }
}

local function toggle(nome)
    Menu.funcoes[nome] = not Menu.funcoes[nome]
    print(nome .. ": " .. tostring(Menu.funcoes[nome]))
end

while Menu.aberto do
    print("\n=== MOD MENU (EDUCACIONAL) ===")
    print("1 - Toggle Desync (fake)")
    print("2 - Toggle Speed (fake)")
    print("3 - Toggle Fly (fake)")
    print("4 - Fechar Menu")

    local escolha = io.read()

    if escolha == "1" then
        toggle("desync")
    elseif escolha == "2" then
        toggle("speed")
    elseif escolha == "3" then
        toggle("fly")
    elseif escolha == "4" then
        Menu.aberto = false
    end
end
