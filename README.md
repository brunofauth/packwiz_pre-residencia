# Modpack Pré-residência

Um Modpack que eu crieir para jogar Minecraft 1.21.1 logo antes de ingressar na residência médica.

Ele usa o [packwiz](https://packwiz.infra.link/) como gerenciador e pode ser instalado com o [packwiz-installer](https://github.com/packwiz/packwiz-installer).


# Instalação

Tu tem que ter o `packwiz-installer` para baixar esse modpack. Pode baixar ele
[aqui](https://github.com/packwiz/packwiz-installer-bootstrap/releases), na
forma de bootstrapper, que é um wrapper que baixa e atualiza o próprio
`packwiz-installer`, ou pelo AUR:

    yay -S packwiz-installer

Depois tu vai até o diretório que tu quer popular com os conteúdos do modpack
(se tu usa o launcher original da mojang, esse diretório tem que ser o teu
`.minecraft`) e executa o `packwiz-installer` dando a URL da versão *pages*
deste mesmo repositório, assim:

    packwiz-installer "https://brunofauth.github.io/packwiz_pre-residencia/pack.toml"

Esse diretório onde tu tá pode, agora, ser usado diretamente pelo launcher
`portablemc`

    portablemc \
        --main-dir ~/.local/share/portablemc-main/ \
        --work-dir <DIRETORIO POPULADO PELO PACKWIZ-INSTALLER> \
        start \
            --login <EMAIL MICROSOFT> \
            --jvm-args="-Djava.io.tmpdir=$HOME/.cache/portablemc" \
            fabric:1.21.1

