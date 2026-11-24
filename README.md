# Alerta Bacanga

Protótipo acadêmico (disciplina Ciência, Tecnologia e Sociedade) de um sistema de informação e alerta preventivo de **enchentes e deslizamentos** na **Bacia do Rio Bacanga**, em São Luís/MA.

> ⚠️ Todos os dados de chuva, maré, risco e alertas são **simulados**. Este app não é um canal oficial. Em emergência, ligue para a Defesa Civil (199).

## Funcionalidades
- **Painel**: situação geral da bacia, chuva 1h/24h/72h, maré, nível do rio, saturação do solo e risco por bairro.
- **Previsão de risco**: projeção para as próximas 12h com faixa de incerteza e previsão por bairro.
- **Mapa**: bairros da bacia coloridos pelo nível de risco (inundação, deslizamento ou suscetibilidade).
- **Cenários**: 5 cenários com botão play (dia comum, temporal + maré alta, chuva prolongada, evento extremo e personalizado).
- **Alertas**: emissão automática de alertas, celulares simulados recebendo as mensagens e histórico.
- **Orientações**: o que fazer em cada nível e contatos de emergência.
- **Parâmetros**: fórmula do risco, níveis de alerta e pesos ajustáveis ao vivo.

## Modelo de risco (ilustrativo)
Risco = Perigo × Exposição × Vulnerabilidade

- Perigo de inundação: chuva 1h, acumulado 24h, maré e saturação do solo.
- Perigo de deslizamento: acumulado 72h, acumulado 24h, saturação do solo e chuva 1h.
- Risco do bairro: `R = 100 · H · (0,4 + 0,6·S) · (0,7 + 0,3·V)`
- Níveis: Normal, Observação, Atenção, Alerta e Alerta Máximo.

Os parâmetros são didáticos e **não** são limiares operacionais validados.

## Estrutura
```
index.html      página principal
css/style.css   estilos (cores da Defesa Civil)
js/app.js       simulação, gráficos, mapa e alertas
.nojekyll       evita processamento do Jekyll no GitHub Pages
```

## Como publicar no GitHub Pages
1. Envie todos os arquivos para a raiz de um repositório público.
2. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/(root)`.
3. Acesse `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`.

## Atalhos
- Barra de espaço: play/pausa
- Setas ← →: voltar/avançar uma hora

## Referências
- Pereira (2024): https://doi.org/10.15628/geoconexes.2024.14985
- Castro et al. (2024): https://doi.org/10.26895/geosaberes.v15i0.1352
- Nascimento et al. (ABRHidro): https://anais.abrhidro.org.br/job.php?Job=19370
- CEMADEN, INMET, ANA (HidroWeb), SGB/CPRM
