# AcrylicUI

Uma biblioteca de UI moderna para Roblox, com efeito acrílico (blur),
animações suaves e sistema completo de componentes.

------------------------------------------------------------------------

## ✨ Destaques

-   **Design Moderno** -- Fundo com efeito acrílico (blur) e animações
    suaves\
-   **Suporte para Mobile** -- Botão móvel automático para dispositivos
    com toque\
-   **Arrastar e Redimensionar** -- Janela totalmente arrastável e
    redimensionável\
-   **Sistema de Notificações** -- Notificações bonitas com ícones e
    tempo automático\
-   **Componentes Completos** -- Button, Toggle, Slider, Dropdown,
    Keybind, ColorPicker, TextBox e Paragraph\
-   **Personalizável** -- Cores, tamanhos, fontes e animações
    ajustáveis\
-   **Sistema de Keybind** -- Atalhos configuráveis\
-   **Sections & Tabs** -- Organização por seções recolhíveis\
-   **Sistema de Config** -- Salvar, carregar e gerenciar perfis com
    auto-save

------------------------------------------------------------------------

## 📦 Instalação

### Método 1: Loadstring (Recomendado)

``` lua
local Library = loadstring(game:HttpGet("COLOQUE_AQUI_SEU_LINK_RAW"))()
```

### Método 2: Como módulo local

Coloque o arquivo da biblioteca dentro do seu projeto (ex:
ReplicatedStorage) e use:

``` lua
local Library = require(game.ReplicatedStorage.AcrylicUI)
```

------------------------------------------------------------------------

## 🚀 Início Rápido

``` lua
local Library = loadstring(game:HttpGet("COLOQUE_AQUI_SEU_LINK_RAW"))()

local window = Library.new("Meu Hub", "ConfigsDoMeuHub")

window:SetToggleKey(Enum.KeyCode.RightControl)

window:Notify({
    Title = "Bem-vindo!",
    Description = "Hub carregado com sucesso",
    Duration = 3,
    Icon = "rbxassetid://10709775704"
})

local CombatSection = window:CreateSection("Combat")
local AimbotTab = CombatSection:CreateTab("Aimbot", "rbxassetid://10723407389")

AimbotTab:CreateToggle({
    Name = "Ativar Aimbot",
    Default = false,
    Callback = function(state)
        print("Aimbot:", state)
    end
})
```

------------------------------------------------------------------------

## 📚 Principais Funções

### Criar Janela

``` lua
local window = Library.new("Titulo", "NomeDaPastaConfig")
```

-   `title` → Título da janela\
-   `configFolder` → Nome da pasta onde as configs serão salvas

------------------------------------------------------------------------

### Notificação

``` lua
window:Notify({
    Title = "Titulo",
    Description = "Mensagem",
    Duration = 3,
    Icon = "rbxassetid://ID"
})
```

------------------------------------------------------------------------

### Criar Section

``` lua
local section = window:CreateSection("Nome")
```

------------------------------------------------------------------------

### Criar Tab

``` lua
local tab = section:CreateTab("NomeDaTab", "rbxassetid://IconID")
```

------------------------------------------------------------------------

## 🧩 Componentes Disponíveis

### Toggle

``` lua
tab:CreateToggle({
    Name = "Nome",
    Default = false,
    Callback = function(value)
    end
})
```

### Slider

``` lua
tab:CreateSlider({
    Name = "Velocidade",
    Min = 0,
    Max = 100,
    Default = 50,
    Callback = function(value)
    end
})
```

### Dropdown

``` lua
tab:CreateDropdown({
    Name = "Selecionar",
    Options = {"Opção 1", "Opção 2"},
    Default = "Opção 1",
    Callback = function(selected)
    end
})
```

### Keybind

``` lua
tab:CreateKeybind({
    Name = "Tecla",
    Default = Enum.KeyCode.F,
    Callback = function()
    end
})
```

### Button

``` lua
tab:CreateButton({
    Name = "Clique Aqui",
    Callback = function()
    end
})
```

------------------------------------------------------------------------

## 📱 Recursos

### Suporte Mobile

Se for detectado dispositivo touch, um botão móvel aparece
automaticamente no canto da tela.

### Janela Redimensionável

Arraste o canto inferior direito para redimensionar a janela.

### Sistema de Configuração

Permite: - Salvar configurações - Carregar perfis - Deletar configs -
Auto-save automático

------------------------------------------------------------------------

## ⚙ Requisitos do Executor

Para o sistema de config funcionar, o executor deve suportar:

-   writefile
-   readfile
-   isfile
-   makefolder
-   isfolder
-   listfiles
-   delfile

A maioria dos executores modernos suporta essas funções.

------------------------------------------------------------------------

## 📄 Licença

MIT License -- Livre para uso e modificação.

------------------------------------------------------------------------

## 👤 Créditos

v0rtexd
