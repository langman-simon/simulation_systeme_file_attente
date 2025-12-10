# 1. GENERATION LCG

x\_{n+1} = (a _ x_n + c) mod m
u_n = x_n / m
y_n = floor(10 _ u_n)

# 2. CONDITIONS DE HULL–DOBELL

gcd(c, m) = 1
(a - 1) ≡ 0 (mod p) pour tout p premier divisant m
si 4 | m alors (a - 1) ≡ 0 (mod 4)

# 3. CALCUL DE LA PERIODE

période = index_actuel - index_precedent_de(x)

# 4. TEST DES FREQUENCES (CHI²)

E_i = N / 10
chi2 = Σ( (O_i - E_i)² / E_i )
(df = nb_classes - 1)

# 5. TEST DU POKER (k = 5)

E_type = N_mains \* P_type
chi2 = Σ( (O - E)² / E )

# 6. LOIS DES ARRIVEES (POISSON)

N_ord ~ Poisson(1.5)
N_prio ~ Poisson(0.7)

# 7. LOI DES DUREES DE SERVICE

P(C_i) = r_i / Σ r_j

# 8. PRIORITAIRES ABSOLUS

P(prioritaire_absolu) = 0.30

# 9. COUTS PAR HEURE

# Présence

C_ord = 15
C_prio_rel = 35
C_prio_abs = 45

# Occupation

C_occ_prio = 33
C_occ_ord = 28

# Inoccupation

C_inocc = 18

# Pertes

C_perte_prio = 20
C_perte_ord = 15

# 10. MINUTES -> HEURES

heures = minutes / 60

# 11. COUT TOTAL

C_total = C_presence + C_occupation + C_inoccupation + C_pertes

# VOCABULAIRE MATHEU

Régime continu : on reprend le service interrompu là où on l’a laissé.

FE(nbStations) = a _ nbStations + B _ fileCumulee/tempsSimule
