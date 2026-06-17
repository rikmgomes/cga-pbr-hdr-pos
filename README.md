# cga-pbr-hdr-pos

# Estudo Prático de PBR, HDR e Pós-Processamento na Unreal Engine 5.7.4
Este repositório contém os resultados e a documentação de um trabalho prático de computação gráfica avançada, focado na aplicação de técnicas modernas de renderização utilizadas em motores gráficos contemporâneos. O principal objetivo deste estudo é demonstrar, através de uma cena controlada, o impacto de materiais fisicamente baseados (PBR), iluminação em alta faixa dinâmica (HDR) e efeitos de pós-processamento na qualidade visual final da renderização.

## 🎓 Contexto Acadêmico
* **Curso:** Jogos Digitais
* **Disciplina:** Computação Gráfica Avançada (2026/1)
* **Professor:** Guilherme Chagas Kurtz

## 🛠️ O Que Foi Feito e Como
Foi construída uma cena de testes baseada em uma **Cornell Box aberta**, utilizando objetos simples e materiais desenvolvidos na Unreal Engine 5.7.4 para evidenciar individualmente cada técnica estudada.

### Construção da Cena

**Physically Based Rendering (PBR):**
* **Material Dielétrico:** Esfera não metálica utilizada para demonstrar o comportamento de materiais cujo aspecto visual é definido principalmente pelo albedo e por reflexões especulares reduzidas.
* **Material Metálico com Roughness Procedural:** Esfera metálica com um mapa procedural de ruído aplicado ao parâmetro Roughness, permitindo observar a influência da rugosidade na dispersão dos reflexos.
* **Material Fresnel:** Esfera dedicada à demonstração da variação da refletância conforme o ângulo de observação da superfície.

**High Dynamic Range (HDR):**
* **HDRI Backdrop:** Utilização de um ambiente HDRI como fonte de iluminação global e reflexões.
* **Exposure Control:** Testes variando a exposição da cena para analisar a percepção de brilho e contraste.
* **Tone Mapping:** Observação do comportamento do operador de tone mapping padrão da Unreal Engine na conversão de valores HDR para exibição em monitores convencionais.

**Pós-Processamento:**
* **Bloom:** Simulação do espalhamento de luz em regiões de alta intensidade luminosa.
* **Depth of Field (DOF):** Desfoque dependente da distância focal para reforçar a percepção de profundidade.
* **Chromatic Aberration:** Separação sutil dos canais de cor para reproduzir limitações ópticas observadas em lentes reais.

### Metodologia
A análise foi realizada através da comparação visual de diferentes configurações de materiais, iluminação e pós-processamento dentro da mesma cena. Foram produzidas capturas estáticas e vídeos demonstrando:

1. A diferença entre materiais metálicos e dielétricos.
2. O impacto do parâmetro Roughness sobre a nitidez dos reflexos.
3. O comportamento angular das reflexões através do efeito Fresnel.
4. A contribuição do HDRI para iluminação e reflexões do ambiente.
5. O efeito do tone mapping e da exposição na aparência final da imagem.
6. A influência dos efeitos de pós-processamento na composição visual da cena.

## 📊 Principais Resultados Observados
* **Metallic Workflow:** Materiais metálicos apresentaram reflexões significativamente mais intensas e dependentes do ambiente quando comparados aos materiais dielétricos.
* **Roughness:** A variação da rugosidade alterou diretamente a nitidez das reflexões, produzindo desde superfícies espelhadas até reflexos altamente difusos.
* **Fresnel:** Foi possível observar o aumento da refletância em ângulos rasantes, comportamento compatível com o modelo físico adotado pelo PBR.
* **HDRI e Iluminação Global:** O uso de imagens HDR permitiu obter iluminação ambiente e reflexões mais realistas do que métodos baseados apenas em fontes de luz artificiais.
* **Tone Mapping:** O operador padrão da Unreal Engine possibilitou adaptar a ampla faixa dinâmica da cena para exibição em monitores SDR, preservando detalhes em regiões claras e escuras.
* **Pós-Processamento:** Bloom, Depth of Field e Chromatic Aberration contribuíram para uma apresentação visual mais próxima da observada em sistemas reais de captura de imagem.

## 📚 Referências
* **PHARR, Matt; JAKOB, Wenzel; HUMPHREYS, Greg.** *Physically Based Rendering: From Theory to Implementation*. 3rd ed. Morgan Kaufmann, 2016.
* **REINHARD, Erik et al.** *High Dynamic Range Imaging: Acquisition, Display and Image-Based Lighting*. 2nd ed. Morgan Kaufmann, 2010.
* **EPIC GAMES.** Unreal Engine Documentation: Physically Based Materials. Disponível em: https://docs.unrealengine.com
* **EPIC GAMES.** Unreal Engine Documentation: HDRI Backdrop. Disponível em: https://docs.unrealengine.com
* **EPIC GAMES.** Unreal Engine Documentation: Post Process Effects. Disponível em: https://docs.unrealengine.com
