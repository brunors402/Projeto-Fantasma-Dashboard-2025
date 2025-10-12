source("rdocs/source/packages.R")

# ---------------------------------------------------------------------------- #

#        ______   _____  ________      ________ 
#      |  ____| / ____| |__   __| /\  |__   __|
#     | |__    | (___     | |   /  \    | |   
#    |  __|    \___ \    | |  / /\ \   | |   
#   | |____   ____) |   | |  /____ \  | |   
#  |______   |_____/   |_| /_/    \_\|_|   
#  
#         Consultoria estatística 
#

# ---------------------------------------------------------------------------- #
# ############################## README ###################################### #
# Consultor, favor utilizar este arquivo .R para realizar TODAS as análises
# alocadas a você neste projeto pelo gerente responsável, salvo instrução 
# explícita do gerente para mudança.
#
# Escreva seu código da forma mais clara e legível possível, eliminando códigos
# de teste depreciados, ou ao menos deixando como comentário. Dê preferência
# as funções dos pacotes contidos no Tidyverse para realizar suas análises.
# ---------------------------------------------------------------------------- #
<<<<<<< Updated upstream

##Análise 1

##código pra limpar o banco

library(tidyverse)



g1 <- ggplot(mpg) +
  aes(x = class) +
  geom_bar(fill = "#A11D21") +
  labs(x = "Classe do automóvel", y = "Frequência") +
  theme_estat()

print_quadro_resumo(variavel)












=======
arquivo <- "C:/Users/Usuario/Downloads/relatorio_old_town_road.xlsx"

dados <- read_excel(arquivo, sheet = "relatorio_vendas")

for (aba in c("relatorio_vendas", "infos_vendas", "infos_produtos", "infos_lojas")) {
  cat("\n==== Planilha:", aba, "====\n")
  dados <- read_excel(arquivo, sheet = aba)
  print(names(dados))
  print(head(dados))
}
head(dados)

relatorio_vendas <- read_excel(arquivo, sheet = "relatorio_vendas")
infos_vendas     <- read_excel(arquivo, sheet = "infos_vendas")
infos_produtos   <- read_excel(arquivo, sheet = "infos_produtos")
infos_lojas      <- read_excel(arquivo, sheet = "infos_lojas")

dados <- relatorio_vendas %>%
  left_join(infos_vendas, by = c("SaleID" = "Sal3ID")) %>%
  left_join(infos_produtos, by = c("ItemID" = "Ite3ID")) %>%
  left_join(infos_lojas, by = c("StoreID" = "Stor3ID"))

dados <- dados %>%
  mutate(
    Date = as.Date(Date),
    Ano = year(Date),
    Receita_USD = Quantity * UnityPrice
  )

cotacao <- 5.31
dados <- dados %>%
  mutate(Receita_BRL = Receita_USD * cotacao)

dados_periodo <- dados %>%
  filter(Ano >= 1880 & Ano <= 1889)

receita_media <- dados_periodo %>%
  group_by(Ano) %>%
  summarise(
    Receita_Media_USD = mean(Receita_USD, na.rm = TRUE),
    Receita_Media_BRL = mean(Receita_BRL, na.rm = TRUE),
    .groups = "drop"
  ) %>%
  mutate(
    Receita_Media_USD = round(Receita_Media_USD, 2),
    Receita_Media_BRL = round(Receita_Media_BRL, 2)
  )
print(receita_media)

ggplot(receita_media, aes(x = Ano, y = Receita_Media_BRL)) +
  geom_line(color = "#0072B2", size = 1.2) +
  geom_point(color = "#D55E00", size = 3) +
  labs(
    title = "Receita média das lojas por ano (1880–1889)",
    subtitle = "Valores convertidos para reais (R$)",
    x = "Ano",
    y = "Receita média por loja (R$)"
  ) +
  theme_minimal(base_size = 13)

write_xlsx(receita_media, "receita_media_1880_1889.xlsx")
>>>>>>> Stashed changes
