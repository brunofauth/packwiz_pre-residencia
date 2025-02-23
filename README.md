<!--
vim: nospell
-->

# Modpack Pré-residência

Um Modpack que eu crieir para jogar Minecraft 1.21.1 logo antes de ingressar na
residência médica.  Ele usa o [packwiz][intro-1] como gerenciador e pode ser
instalado com o [packwiz-installer][intro-2].

[intro-1]: https://packwiz.infra.link/
[intro-2]: https://github.com/packwiz/packwiz-installer


# Instalação

Tu tem que ter o `packwiz-installer` para baixar esse modpack. Pode [baixar ele
aqui][install-1], na forma de um JAR bootstrapper, que é um wrapper que baixa e
atualiza o próprio `packwiz-installer`, ou, no Arch Linux, [pelo AUR](install-2).

Depois tu vai até o diretório que tu quer popular com os conteúdos do modpack
(se tu usa o launcher original da mojang, esse diretório tem que ser o teu
`.minecraft`) e executa o `packwiz-installer` dando a URL da versão *pages*
deste mesmo repositório, assim:

```bash
# Esse comando instala só os mods server-sided
java -jar packwiz-installer-bootstrapper.jar \
    --side=server "https://brunofauth.github.io/packwiz_pre-residencia/pack.toml"

# Esse comando instala só os mods client-sided
java -jar packwiz-installer-bootstrapper.jar \
    --side=client "https://brunofauth.github.io/packwiz_pre-residencia/pack.toml"

# Esse comando instala mods ambos client- e server-sided
java -jar packwiz-installer-bootstrapper.jar \
    --side=both   "https://brunofauth.github.io/packwiz_pre-residencia/pack.toml"

# Outras opções de CLI do packwiz-installer (cf. código-fonte):
# --side              <"client"|"server"|"both">  (default="client")
# --pack-folder       <file path>                 (default=cwd)
# --multimc-folder    <file path>
# --manifest-file     <file path>                 (default="packwiz.json")
# --timeout           <seconds>                   (default=10)
```

Esse diretório onde tu tá pode, agora, ser usado diretamente pelo launcher
[*portablemc*][install-3] (ou, se tu instalou no `.minecraft`, pode usar pelo
launcher normal da Mojang também).

```bash
portablemc \
    --main-dir "${XDG_DATA_HOME:-$HOME/.local/share}/portablemc-main/" \
    --work-dir <DIRETORIO/POPULADO/PELO/PACKWIZ-INSTALLER> \
    start \
        --login <EMAIL-MICROSOFT> \
        --jvm-args="-Djava.io.tmpdir='${XDG_CACHE_HOME:-$HOME/.cache}/portablemc'" \
        fabric:1.21.1
```


[install-1]: https://github.com/packwiz/packwiz-installer-bootstrap/releases
[install-2]: https://aur.archlinux.org/packages/packwiz-installer
[install-3]: https://github.com/mindstorm38/portablemc


# Avisos

## Mods e Recursos com Versões Fixadas

O resourcepack [Hyper Realistic Sky][hrs-1] está fixado na versão 2.2 porque
ela é a mais recente que funciona com o mod `fabricskyboxes`.  Talvez, no
futuro, outras versões desse resourcepack funcionem com esse mesmo mod. Para
saber se esse é o caso, tem que conferir as últimas linhas do Changelog de cada
versão nova (por exemplo [aqui embaixo][hrs-2]).

[hrs-1]: https://modrinth.com/resourcepack/hyper-realistic-sky/
[hrs-2]: https://modrinth.com/resourcepack/hyper-realistic-sky/version/2.2


# Conteúdos

Bibliotecas (coremods) não estão incluidos aqui.


## Mods

### Otimização
- Clumps
- Concurrent Chunk Management Engine (Fabric)
- Cull Leaves
- Debugify
- Dynamic FPS
- Enhanced Block Entities
- Entity Culling
- FerriteCore
- ImmediatelyFast
- Lithium
- ModernFix
- More Culling
- Noisium
- Reese's Sodium Options
- Sodium
- Sodium Extra


### Beleza
- AmbientSounds
- CIT Resewn
- Continuity
- Distant Horizons
- FabricSkyboxes
- FabricSkyBoxes Interop
- Model Gap Fix


### Qualidade de Vida
- AppleSkin
- Better Mount HUD
- Better Third Person
- BetterF3
- Carry On
- Client Tweaks
- Controlling
- Crafting Tweaks
- FastQuit
- Inventory Essentials
- Just Enough Items
- KISS (Keep Inventories Sorted, Simple)
- Mod Menu
- More Chat History
- Paginated Advancements & Custom Frames
- Remove Reloading Screen
- Replanting Crops
- Shulkerbox Tooltip


### Outras Ferramentas
- Carpet
- Carpet Extra
- Chunky
- e4mc
- Fabrishot
- FallingTree
- Fire Spread Tweaks
- Lighty
- MiniHUD
- Mob Explosion Griefing Gamerule
- No Chat Reports
- Ping Wheel
- Reacharound
- Xaero's Minimap
- Xaero's World Map
- You're in Grave Danger
- Zoomify


## Resourcepacks

- [Better Leaves](https://modrinth.com/resourcepack/better-leaves)
- [Default Dark Mode](https://modrinth.com/resourcepack/default-dark-mode)
- [Fast Better Grass](https://modrinth.com/resourcepack/fast-better-grass)
- [Hyper Realistic Sky](https://modrinth.com/resourcepack/hyper-realistic-sky)
- [Low On Fire](https://modrinth.com/resourcepack/low-on-fire)
- [Unique Enchanted Books](https://modrinth.com/resourcepack/unique-enchanted-books)

