# cep - c(aisse d') e(pargne) p(arser)

Script pour parser les relevés de compte PDF de la Caisse d'Épargne et obtenir
un CSV contenant 6 colonnes:
- la date d'enregistrement de la transaction par la CE
- le numéro de compte
- le type de transaction:
    - `DEPOT`: dépôt de chèque
    - `TRANSFERT`: virement reçu
    - `CHECK`: chèque émis
    - `BANK`: frais bancaire
    - `DEBIT`: paiement par CB
    - `WITHDRAWAL`: retrait d'espèce
    - `DIRECTDEBIT`: prélèvement
    - `OTHER`: autre opération
- l'intitulé de la transaction
- le crédit (si crédit)
- le débit (si débit)

Le CSV a pour séparateur `;`.

### Installation

Installer le sous-module `pdfminer` si non présent sur la machine.

### Utilisation

```bash
./cep folder
```
avec `folder` un dossier contenant les PDF à parser
