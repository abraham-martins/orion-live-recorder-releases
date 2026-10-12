# Orion Live Recorder para Windows

[Baixar a versão mais recente](https://github.com/abraham-martins/orion-live-recorder-releases/releases/latest)

Este repositório distribui os instaladores e pacotes de atualização oficiais. O código-fonte é mantido em repositório privado.

## Instalar

1. Encerre gravações e conversões na versão antiga.
2. Abra a página de releases e baixe **OrionLiveRecorder.Desktop-win-x64-Setup.exe**.
3. Execute o Setup e abra o Orion pelo atalho. O .NET está incluído; não é necessário extrair arquivos.

Na primeira instalação, conserve a pasta da versão antiga até validar uma gravação. Preferências, componentes e histórico permanecem em `%LOCALAPPDATA%\OrionLiveRecorder`; os vídeos permanecem na pasta escolhida por você.

## Atualizar

No Orion instalado, abra **Atualizações → Verificar atualizações → Baixar, instalar e reiniciar**. O programa solicita confirmação, verifica tamanho e SHA-256, fecha com segurança, aplica e reabre. A instalação fica bloqueada durante gravação, remux e outras operações. O download pode ser cancelado.

A v0.1.7 antiga precisa desta primeira execução do Setup, pois não contém o novo updater. Use o Setup para receber autoatualizações; o ZIP Portable é opcional e não participa desse fluxo.

## Integridade e suporte

Compare o hash do instalador com `SHA256SUMS.txt` da mesma release:

```powershell
Get-FileHash .\OrionLiveRecorder.Desktop-win-x64-Setup.exe -Algorithm SHA256
```

O instalador ainda não é assinado com certificado de editor. O Windows pode mostrar SmartScreen. SHA-256 verifica integridade, não substitui assinatura de editor. Baixe somente desta página oficial.

Se uma atualização falhar, mantenha suas gravações e dados. Tente novamente ou execute o Setup oficial com o Orion fechado. Ao relatar um problema, não envie cookies, tokens, links assinados ou bancos de dados pessoais.

Compatibilidade: Windows x64; homologação recomendada no Windows 11. A captura usa yt-dlp e FFmpeg para transmissões acessíveis e não contorna DRM ou acesso restrito.
