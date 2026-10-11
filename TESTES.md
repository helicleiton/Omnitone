# Roteiro de testes do Omnitone

O Omnitone foi desenvolvido e verificado em um único computador (Windows 10,
interface Steinberg UR22mkII, teclado controlador USB). Este roteiro serve para
quem quiser testá-lo em outra máquina. Leva de 15 a 20 minutos.

Ao relatar um problema em <https://github.com/helicleiton/Omnitone/issues>,
informe: versão do Windows, interface de áudio e driver, tipo de áudio
escolhido (ASIO, Windows Audio...), tamanho do buffer e o passo em que falhou.

## 1. Abrir

- [ ] `Omnitone.exe` abre (depois do aviso do SmartScreen, se aparecer).
- [ ] A janela cabe na tela e pode ser redimensionada.
- [ ] Em **Options > Audio/MIDI Settings**, a saída de áudio aparece e o botão **Test** produz som.
- [ ] Com um driver ASIO instalado, o tipo **ASIO** aparece na lista.

## 2. Tocar

- [ ] Clicar no teclado da tela produz som.
- [ ] Um controlador MIDI ligado por USB toca sem precisar marcar nada.
- [ ] Tocar forte e fraco muda o volume ou o timbre.
- [ ] As rodas de pitch bend e de modulação do controlador movem as da tela e alteram o som.
- [ ] O pedal de sustain funciona.

## 3. Timbres de fábrica (não precisam de nenhuma biblioteca)

Na tela **TONES**, carregue pelo menos um de cada e confira se há som:

- [ ] Sintetizadores
- [ ] Teclados Lendários > Analógicos
- [ ] Pianos e Teclados > Órgão (os "Tonewheel ...")
- [ ] Um timbre com origem "Yamaha DX7 (vozes do Omnitone)", pela aba ORIGEM

## 4. Camadas e mesa

- [ ] Carregar timbres em duas camadas e ouvir os dois juntos.
- [ ] Fader, **M** (mute) e **S** (solo) de cada canal funcionam; os VUs se movem.
- [ ] O fader **MASTER** muda o volume geral.
- [ ] Arrastar as pontas da barra acima do teclado limita a faixa de teclas da camada (split).
- [ ] Os botões **−** e **+** de oitava transpõem a camada.

## 5. Controles e efeitos

- [ ] Cutoff e Resonance alteram o timbre; os knobs de uma camada não mudam a outra.
- [ ] Equalizador (Low, Mid, High) altera o som.
- [ ] Modulação: Chorus, Phaser, Tremolo e Leslie são audíveis.
- [ ] Delay e Reverb são audíveis.
- [ ] Trocar de timbre não deixa os controles "herdados" do anterior.

## 6. Salvar

- [ ] **Salvar > Salvar ajustes do tone**: mexer em um knob, salvar, trocar de timbre e voltar; o ajuste retorna.
- [ ] **Salvar > Salvar como nova performance**: a performance aparece no topo da tela TONES e recarrega as camadas.
- [ ] O botão da **estrela** marca o timbre; ele aparece em **Favoritos**.
- [ ] Fechar e reabrir o app mantém camadas, controles e configuração de áudio.

## 7. Controlador MIDI

- [ ] Botão direito em um knob > **Endereçar...** e mover um controle do teclado: o knob passa a responder.
- [ ] O endereçamento continua depois de reabrir o app.

## 8. Bibliotecas

- [ ] **TONES > Importar...** com um arquivo `.sf2`: os presets aparecem na lista e tocam.
- [ ] Uma pasta com instrumento `.sfz` copiada para `Documentos\Omnitone\Libraries` aparece depois de reabrir.

## 9. Plugin VST3

- [ ] Com `Omnitone.vst3` copiado para `C:\Program Files\Common Files\VST3`, a DAW encontra o plugin.
- [ ] Ele toca, e salvar e reabrir o projeto restaura camadas e controles.
- [ ] O delay em modo **Sync** acompanha o andamento do projeto.

## 10. Estabilidade

- [ ] Uso de CPU em repouso baixo (alguns por cento).
- [ ] Sem estalos ao tocar acordes com 2 ou 3 camadas.
- [ ] Trocar de timbre várias vezes seguidas não trava o app.
